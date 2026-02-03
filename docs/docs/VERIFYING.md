# How to verify a PQC+ZK transfer (60 seconds)

## What to look for
A PQC+ZK transfer emits:
1) Standard ERC-20 `Transfer(...)` log(s)
2) An additional `ISO20022Transfer(...)` log:
   - includes `isoRefHash` (indexed)
   - includes `isoReference` JSON with metadata (purpose, chainId, token, nonce, etc.)

## BNB example (chainId=56)
Tx:
- https://bscscan.com/tx/0x8d8d99e32f214ec0358c28138f557909e71f81ecebddbbc0e5749b92eee023a4

Check:
- ISO20022Transfer.isoRefHash = 0xA03A0BB4...06AE2
- isoReference.purpose = "PQC AIRDROP"
- isoReference.nonce = 10

## Ethereum example (chainId=1)
Tx:
- https://etherscan.io/tx/0x60022ac15de25d3df59f9c569dea69a04aa36eaffc6f41b44a3b506d4f273a57

Check:
- logs include burn Transfer (to 0x0) + net Transfer (to recipient)
- ISO20022Transfer includes isoRefHash + isoReference JSON

## Note about programVKey
During early testing, program verification keys were rotated while stabilizing the proving pipeline.
The isoReference JSON can include the programVKey used for that specific proof (“proof metadata”).
