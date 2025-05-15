# 🧬 Chainlink CCIP Cross-Chain Messaging Example

This is a simple implementation of **cross-chain messaging** using [Chainlink's CCIP (Cross-Chain Interoperability Protocol)](https://chain.link/ccip).  
It demonstrates sending a string message (`"Hello World"`) from a **Sender contract** deployed on **Avalanche Fuji** to a **Receiver contract** deployed on **Ethereum Sepolia**.

---

## 🔧 Tech Stack

- Solidity ^0.8.24
- Chainlink CCIP v1.5.1
- Remix IDE (for deployment & testing)
- Ethereum Sepolia Testnet (Receiver)
- Avalanche Fuji Testnet (Sender)

---

## 📌 How It Works

### 1. **Receiver Contract**
- Inherits `CCIPReceiver`
- Listens for incoming messages via CCIP
- Stores the last received message and sender details

### 2. **Sender Contract**
- Sends a message via CCIP
- Requires funding with LINK (for cross-chain fee payment)
- Takes three inputs:
  - Destination chain selector
  - Receiver contract address
  - Message to send (as a string)

---

### ✅ Prerequisites:
- Wallet with test ETH on Sepolia & AVAX on Fuji
- Some test LINK tokens on Avalanche Fuji (to pay CCIP fees)
- Remix IDE connected to both networks via MetaMask or wallet of choice

---

## 🧠 Learnings

- CCIP removes the need for custom bridges
- Uses Chainlink’s decentralized oracle network for secure delivery
- Great entry point for building cross-chain dApps
