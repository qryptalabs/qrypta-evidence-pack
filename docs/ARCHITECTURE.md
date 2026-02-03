# Architecture (high level)

## Dual-mode transfers
1) Standard mode:
- user calls `transfer(to, amount)`
- emits `Transfer(from, to, amount)`

2) PQC+ZK mode:
- wallet/prover builds a bound message: chainId, token, to, amount, nonce, deadline, paymentRefHash
- user signs with PQC off-chain
- prover generates a Groth16 proof (SP1)
- contract verifies proof on-chain via SP1 gateway
- token executes transfer and emits:
  - standard `Transfer(...)`
  - `ISO20022Transfer(..., isoRefHash, isoReference JSON)`
