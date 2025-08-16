# Foundry Merkle Airdrop

A sample project for deploying and interacting with a Merkle-based airdrop smart contract using [Foundry] . It uses Merkel-based technique to search required data from the list with better optimization compared to for loop.

## Features

- Merkle tree-based airdrop contract
- Automated deployment and claim scripts
- Local testing with Anvil
- Example usage of `cast` and `forge` commands

## Getting Started


### Setup

```sh
# Install dependencies
forge install

# Start local node
anvil
```

### Deploy Contracts

```sh
forge script script/DeployMerkleAirdrop.s.sol:DeployMerkleAirdrop --rpc-url http://localhost:8545 --private-key <PRIVATE_KEY> --broadcast
```

### Generate Input Data

```sh
forge script script/GenerateInput.s.sol
```

### Claim Airdrop

```sh
forge script script/Interact.s.sol:ClaimAirdrop --rpc-url http://localhost:8545 --private-key <CLAIMER_PRIVATE_KEY> --broadcast
```

### Check Token Balance

```sh
cast call <TOKEN_ADDRESS> "balanceOf(address)" <ADDRESS> --rpc-url http://localhost:8545
```

## Environment Variables

Create a `.env` file for sensitive data:

```
PRIVATE_KEY=your_private_key
SEPOLIA_RPC_URL=https://...
```



