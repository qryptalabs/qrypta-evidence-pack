# Deployments (BNB + Ethereum)

> Same token contract address deployed on both networks.

## BNB Smart Chain (chainId=56)
- Token (QRYP): 0x5266fe1aD9B035d0ED6142f1A70e9D6F102c8153
- Token page: https://bscscan.com/token/0x5266fe1ad9b035d0ed6142f1a70e9d6f102c8153
- SP1 Gateway (BNB): 0x940467b232cAD6A44FF36F2FBBe98CBd6509EFf2
- Proof system: Groth16 (SP1)

## Ethereum Mainnet (chainId=1)
- Token (QRYP): 0x5266fe1aD9B035d0ED6142f1A70e9D6F102c8153
- Token page: https://etherscan.io/address/0x5266fe1ad9b035d0ed6142f1a70e9d6f102c8153
- SP1 Gateway (ETH): 0x397A5f7f3dBd538f23DE225B51f532c34448dA9B
- Proof system: Groth16 (SP1)

## programVKey note (testing vs canonical)
During early testing we rotated program verification keys to stabilize the proving pipeline.
The ISO20022Transfer.isoReference JSON may include a programVKey as proof metadata for that specific proof.
For canonical values, read them from the on-chain contract configuration (Read Contract / constructor args).
