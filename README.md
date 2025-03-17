# Decentralized Multiplayer Lottery Smart Contract

## Overview
This project is a **blockchain-powered multiplayer lottery system** built using **Solidity**. The smart contract ensures fairness, transparency, and automation by managing ticket purchases, winner selection, and prize distribution without intermediaries. It leverages **Chainlink VRF** for secure random number generation and **Chainlink Automation** for automatic execution.

## Features
- **Trustless Lottery System**: Fully decentralized and transparent.
- **Automated Winner Selection**: Uses Chainlink VRF for randomness.
- **Periodic Draws**: Executes automatically via Chainlink Automation.
- **Secure Fund Management**: Ensures proper prize distribution.

## Technologies Used
- **Solidity (0.8.19)**
- **Chainlink VRF** for verifiable randomness
- **Chainlink Automation** for upkeep execution
- **Ethereum/Polygon/Any EVM-compatible blockchain**
- **Foundry** for development and testing

## Contract Details
- **Entrance Fee**: Users must send a minimum amount of ETH to participate.
- **Raffle State**: The contract operates in `OPEN` and `CALCULATING` states.
- **Winner Selection**: A verifiable random winner is chosen using Chainlink VRF.
- **Automatic Execution**: Chainlink Automation triggers the lottery draw at set intervals.

## How It Works
1. Users enter the lottery by sending ETH.
2. The contract accumulates participants.
3. At a predefined interval, Chainlink Automation triggers winner selection.
4. Chainlink VRF provides a random number.
5. The contract picks a winner and transfers the prize.
6. The lottery resets for the next round.

## Installation
1. Clone the repository:
   ```bash
   https://github.com/0x-Mrcoder/Lottery.git
   cd raffle-contract
   ```
2. Install Foundry:
   ```bash
   curl -L https://foundry.paradigm.xyz | bash
   foundryup
   ```
3. Compile the contract:
   ```bash
   forge build
   ```
4. Run tests:
   ```bash
   forge test
   ```
5. Deploy to a testnet:
   ```bash
   forge script script/Deploy.s.sol --rpc-url <YOUR_RPC_URL> --private-key <YOUR_PRIVATE_KEY> --broadcast
   ```

## Usage
- To enter the raffle, send ETH to the contract.
- Check the winner using the `getRecentWinner` function.
- Use Chainlink Automation to trigger execution.

## License
This project is licensed under the **MIT License**.

## Author
Developed by **Usman Umar (@MrCoder)**.

