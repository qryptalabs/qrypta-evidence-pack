# Demo Transactions (Normal vs PQC+ZK)

## BNB Smart Chain (chainId=56)

Normal transfer:
- https://bscscan.com/tx/0x53b59055eaff9103d6ba34d9b381312064b51e6f623c215c248e5568f232cbc0

PQC+ZK demo (shows ISO20022Transfer event):
- https://bscscan.com/tx/0x8d8d99e32f214ec0358c28138f557909e71f81ecebddbbc0e5749b92eee023a4

Evidence (from ISO20022Transfer in the tx above):
- from: 0x4954ceD99591fB8b7291Fa239F4C3Ef1C27289B8
- to:   0x904CD528167f7400198F95C7fE2ca70b2eDC503c
- amountGross: 120.0 QRYP
- amountNet:   120.0 QRYP
- burnAmount:  0
- isoRefHash:  0xA03A0BB43BC2FC85B29E4213A37ABC4E69C1F8AD7ED5E9A303E02D6A9CD06AE2
- isoReference JSON includes:
  - purpose: "PQC AIRDROP"
  - chainId: 56
  - token: 0x5266fe1ad9b035d0ed6142f1a70e9d6f102c8153
  - nonce: 10
  - programVKey (proof metadata): 0x0049b846e38aa48aa52ffe48bb40032ea99afbfc8abde9c8130267c2585f870e

## Ethereum Mainnet (chainId=1)

Normal transfer:
- https://etherscan.io/tx/0x884f7885cc8ffa21a7018ec6bbcc16580825e8e04865d6c1f4bf9508e440a813

PQC+ZK transfers:
- https://etherscan.io/tx/0x60022ac15de25d3df59f9c569dea69a04aa36eaffc6f41b44a3b506d4f273a57
- https://etherscan.io/tx/0xf40b3665f19c9d1df309d203e2026f280d617fc6d1488763040c045de141a259
