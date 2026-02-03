# How to Verify (2 minutes)

1) Open a demo transaction from docs/DEMO_TXS.md (Etherscan/BscScan).
2) Scroll to: “Transaction Receipt Event Logs”.
3) Confirm:
   - Standard `Transfer(from,to,value)` event exists (wallet/DEX compatibility).
   - `ISO20022Transfer(...)` exists for the PQC/ZK path.
4) In `ISO20022Transfer`, review:
   - `isoRefHash` (indexed topic)
   - `isoReference` JSON (purpose, chainId, token, programVKey, owner, nonce, etc.)
