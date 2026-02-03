# Demo Transactions (Mainnet)

## BNB Smart Chain (BSC)

### Normal transfer (ERC20/BEP20)
- Tx: <PUT_BSC_NORMAL_TX>
  - What to check: `Transfer` event

### PQC/ZK transfer (with ISO20022 metadata event)
- Tx: 0x8d8d99e32f214ec0358c28138f557909e71f81ecebddbbc0e5749b92eee023a4
  - What to check:
    - `Transfer` event
    - `ISO20022Transfer` event (isoRefHash + isoReference JSON)

- Tx: 0x9ee9b055498916c9729cfc0a2e665426fd4e376b44f9338f977279ce7b77173b
  - What to check:
    - `ISO20022Transfer` event indicates “Quantum Transfer ZK” in `isoReference`

## Ethereum Mainnet

### Normal transfer (ERC20)
- Tx: 0x884f7885cc8ffa21a7018ec6bbcc16580825e8e04865d6c1f4bf9508e440a813
  - What to check:
    - `Transfer` to burn address (if burn is enabled)
    - `Transfer` to recipient

### PQC/ZK transfer (with ISO20022 metadata event)
- Tx: 0x60022ac15de25d3df59f9c569dea69a04aa36eaffc6f41b44a3b506d4f273a57
  - What to check:
    - `ISO20022Transfer`: amountGross/amountNet/burnAmount + isoRefHash + isoReference JSON
