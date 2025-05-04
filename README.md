# 🧠 WALLET AI

## The Future of Web3 Wallets — Powered by Natural Language & Account Abstraction

**WALLET AI** is revolutionizing how users interact with blockchain. With a **built-in AI assistant**, **passkey-based authentication**, and full support for **ERC-4337 account abstraction**, it enables seamless, intuitive, and secure blockchain experiences — all in one click.

No mnemonic phrases. No gas fees to worry about. Just simple, fast, and secure access to decentralized finance, NFTs, and dApps — directly from your browser or Telegram.

---

## 🧩 Why WALLET AI?

> "Usability meets decentralization"

We believe blockchain should be accessible to everyone — not just developers. That’s why we’re building WALLET AI: to make interacting with Web3 as easy as typing a message.

By removing technical barriers and offering powerful new capabilities through AI and account abstraction, we are paving the way for true mass adoption.

---

## 🧩 Key Features

- ✅ Built-in AI assistant for natural language-based transactions
- ✅ Account Abstraction via ERC-4337 (supports EntryPoint v0.6)
- ✅ Passkey-based secure identity (no mnemonics)
- ✅ Seamless integration with Telegram Mini Apps
- ✅ WalletConnect support for plug-and-play dApp interaction
- ✅ Smart account creation & gas-efficient deployment
- ✅ Paymaster & Bundler setup for gasless transactions

---

---

## 🔗 Seamless dApp Integration via WalletConnect

WALLET AI supports all decentralized applications out-of-the-box through **WalletConnect integration**:

- 🔐 **Plug-and-play compatibility** – No developer changes required
- 📱 **Consistent UX** across DeFi, NFTs, and Web3 apps
- 🌐 **Instant connection** via QR code or deep link

Whether you're swapping tokens, minting NFTs, or playing games, WALLET AI makes it feel as smooth as traditional Web2 apps.

---

## 💬 WALLET AI Agent: Your Blockchain Assistant

Say goodbye to multiple apps and complex interfaces. With the **AI Agent**, just type what you want to do — like “Approve USDC for Uniswap” or “Bridge ETH to Arbitrum” — and let WALLET AI handle the rest.

🧠 Powered by cutting-edge NLP models trained on blockchain semantics, this agent transforms casual user input into precise, secure smart contract interactions.

---

## 🔐 Secure by Design: Passkey-Based Authentication

WALLET AI eliminates private keys and seed phrases entirely. Instead, it uses **WebAuthn-based passkeys** for maximum security and ease of use.

### How It Works:

1. **Passkey created locally** – Generated on your device or stored in your password manager.
2. **Never exposed** – WALLET AI never sees or stores your passkey.
3. **Biometric or PIN verification** – Authorize actions using Face ID, Touch ID, or device PIN.
4. **Signature handled securely** – Browser APIs ensure cryptographic operations happen safely.

### Benefits:

- 👻 No phishing risk
- 🔒 No need to store recovery phrases
- 🛡️ Device-bound security (e.g., Apple Secure Enclave, Android Keystore)

---

## 🏗️ Smart Accounts: Deployed When Needed

WALLET AI leverages **ERC-4337 account abstraction** to provide programmable, flexible wallets that adapt to user behavior.

### Smart Account Advantages:

- 🧮 **Deterministic addresses** – Share your wallet address before deployment
- ⚡ **On-demand deployment** – Only pay gas fees when you first transact
- 🔄 **Gas-efficient** – Save costs by avoiding unused contracts
- 🤖 **Programmable logic** – Enable future features like batch transactions, social recovery, and more

---

## 📦 Live Contract Addresses (Pharos chain)

| Contract            | Address                                                                                                                 |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **EntryPoint v0.6** | [0xE61707900f200140f5D64fa7bA740299127c2517](https://pharosscan.xyz/address/0xE61707900f200140f5D64fa7bA740299127c2517) |
| **Paymaster**       | [0xF12977Ff3F3260C36774ae47bd85Ca08D4878533](https://pharosscan.xyz/address/0xF12977Ff3F3260C36774ae47bd85Ca08D4878533) |
| **P256R1 Verifier** | [0xb30001fBD7aD144348C6c0739e8fF5339a49b845](https://pharosscan.xyz/address/0xb30001fBD7aD144348C6c0739e8fF5339a49b845) |
| **Account Factory** | [0x589013711Ea4243407602ccc5529f75c0334cd81](https://pharosscan.xyz/address/0x589013711Ea4243407602ccc5529f75c0334cd81) |

🔗 [Watch Demo Video](https://youtu.be/jQ8ez_tX0-0)

---

## 📲 Available On

- 🌐 **Web Version** – Access WALLET AI instantly from any browser
- 💬 **Telegram Mini App** – Use inside Telegram Desktop/Web without downloads

---

## 🛠️ Project Structure

```
wallet-ai/
├── docker/ # Rundler (bundler) & Paymaster services
│ └── paymaster/ # Custom Paymaster logic and binaries
├── frontend/ # Web interface
├── contracts/ # Smart contracts (EntryPoint, Account Factory)
├── README.md # Project overview and setup guide
```

---

## ▶️ Getting Started Locally

### 1. 🔧 Prerequisites

Ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Foundry](https://foundry.paradigm.xyz/) (for contract deployments)
- Node.js >= 18.x + pnpm (`npm install -g pnpm`)

---

### 2. 🐳 Start Bundler & Paymaster

Navigate to the `docker` directory and start the services using Docker Compose:

```bash
cd docker
docker-compose up -d
```

This starts:

- **Rundler**: ERC-4337 Bundler on port `4338`
- **Paymaster**: Local service on port defined in `.env` (e.g., `3001`)

> Ensure your `.env` has `BUILDER_PRIVATE_KEY` and `PAYMASTER_PORT`.

---

### 3. 💻 Run Frontend

Go to the frontend folder and start the development server:

```bash
cd frontend
pnpm dev --port=4337
```

Visit: `http://localhost:4337`  
You can now interact with **Wallet AI** through the browser UI.

---

### 4. 🏗️ Deploy Contracts (Optional)

If deploying a new EntryPoint or Account Factory (e.g., on testnet):

```bash
cd contracts
forge script DeployEntryandFactory --rpc-url <your_rpc_url> --private-key <your_private_key> --broadcast
```

Update configuration files with deployed contract addresses if needed.

---

### 5. 🧪 Test Functionality

- Connect to any dApp via **WalletConnect**
- Use the **AI assistant** to send funds or interact with protocols

---

## 📦 Environment Variables

Create a `.env` file inside `docker` and `paymaster` directories:

```env
# .env
BUILDER_PRIVATE_KEY=your_private_key_here
PAYMASTER_PORT=3001
```

> Never commit your private keys!

---

## 🌐 Supported Chains

| Chain        | Chain ID | EntryPoint Address                           |
| ------------ | -------- | -------------------------------------------- |
| Pharos chain | 5002     | `0x2ae470412F8b53E263C8F967E9679e4830a2643A` |

---

## 🤝 Contributing

We welcome contributions from the community! Fork this repo, create a feature branch, and submit a PR.
