# Daughters of Aether – Advanced Local Setup Manual

Welcome to the **Daughters of Aether** advanced setup guide! This manual is for developers and power users who want full control over every aspect of the game—customizing, running, and hacking on the frontend, backend, and smart contract components.

---

## Project Overview

Daughters of Aether is a real-time Web3 PvP arena game built on the **Gorbagana testnet**. It features:
- 3D character selection and battles
- On-chain staking and rewards
- Real-time matchmaking and multiplayer combat
- Modern, animated UI with wallet integration

This guide will help you set up and customize every part of the project locally.

---

## Repository Structure

The project is split into three main repositories:

- **Frontend UI:**
  - Nuxt 3 + Vue 3 + Three.js game client
  - Wallet connection, 3D arena, matchmaking, and battle UI
  - [Frontend GitHub Repo](https://github.com/DavidNzube101/DOA-)

- **Backend Server:**
  - Node.js + Socket.IO matchmaking and battle state server
  - Handles contract calls, player state, and auto-resolution
  - [Backend GitHub Repo](https://github.com/DavidNzube101/DOA-server-)

- **Gorbagana Smart Contract:**
  - Anchor-based Solana program for battles, staking, and resolution
  - [Contract GitHub Repo](https://github.com/DavidNzube101/DOA-Contract)

---

## Advanced Local Setup

### 1. Clone Each Repository

Clone the three main repositories to your local machine:

```bash
git clone https://github.com/DavidNzube101/DOA-.git        # Frontend
cd DOA-
git clone https://github.com/DavidNzube101/DOA-server-.git # Backend
cd ..
git clone https://github.com/DavidNzube101/DOA-Contract.git # Smart Contract
```

### 2. Install Dependencies

For each repo, install dependencies using [pnpm](https://pnpm.io/):

```bash
cd DOA-         # or DOA-server-, or DOA-Contract
yarn install    # or pnpm install
```

### 3. Configure Environment Variables

Each repository requires its own `.env` file. Refer to the README in each repo for the required variables and example files. Common variables include:
- Solana network and program IDs
- Backend server URLs and ports
- CORS origins
- Wallet and contract configuration

### 4. Fund Your Wallet

- Use [faucet.gorbagana.wtf](https://faucet.gorbagana.wtf) to get GOR testnet tokens.
- Configure your wallet (Backpack or Phantom recommended) for Gorbagana testnet.

### 5. Build and Run Each Component

**Backend Server:**
```bash
cd DOA-server-
pnpm install
pnpm start   # or: node matchmaking.cjs
```

**Frontend UI:**
```bash
cd DOA-
pnpm install
pnpm dev     # for development mode
# or
pnpm build && pnpm preview   # for production mode
```

**Smart Contract:**
- See the [DOA-Contract README](https://github.com/DavidNzube101/DOA-Contract) for build, deploy, and customization instructions.

### 6. Connect and Play

- Start the backend server first, then the frontend UI.
- Open your browser to the frontend's local address (usually [http://localhost:3000](http://localhost:3000)).
- Connect your wallet, stake, and play!

---

## Customization & Development

- **Frontend:** Modify UI, 3D assets, wallet logic, and game flow in the Nuxt/Vue project.
- **Backend:** Tweak matchmaking, battle logic, and contract calls in the Node.js server.
- **Contract:** Extend or change on-chain logic in the Anchor program (Rust).

Refer to each repo's README for advanced configuration, environment variables, and troubleshooting.

---

## Need Help?
- Each repository contains a README with detailed setup, environment, and troubleshooting info.
- For issues or questions, open an issue in the relevant GitHub repository.

---

**Project Home:** [https://github.com/DavidNzube101/DOA-](https://github.com/DavidNzube101/DOA-)

Enjoy building and customizing your own Daughters of Aether experience!
