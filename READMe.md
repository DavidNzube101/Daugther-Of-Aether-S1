# Daughters of Aether – Local Multiplayer Setup Guide

This guide will help you and a friend set up and play Daughters of Aether locally, using the official UI and server repositories.

---

## Prerequisites
- Node.js (v18+ recommended)
- pnpm (or npm/yarn)
- Git

---

## 1. Clone the Repositories

### Game UI (Frontend)
```
git clone https://github.com/DavidNzube101/DOA-.git doa-ui
```

### Server (Backend)
```
git clone https://github.com/DavidNzube101/DOA-server-.git doa-server
```

---

## 2. Install Dependencies

### In the UI folder:
```
cd doa-ui
pnpm install
```

### In the server folder:
```
cd ../doa-server
pnpm install
```

---

## 3. Configure Environment Variables

### UI (`doa-ui/.env.local`):
```
# Solana devnet RPC
SOLANA_DEVNET_RPC_URL=https://api.devnet.solana.com
GORBAGANA_DEVNET_RPC_URL=https://rpc.gorbagana.wtf
# Program ID (devnet)
DEVELOPMENT_PROGRAM_ID=5RV8MAYjHoSb16VkqjqN5KGX139MULDR6GHuYhxettKT
PRODUCTION_PROGRAM_ID=GAB3CVmCbarpepefKNFEGEUGw6RzcMx9LSGER2Hg3FU2
# Matchmaking server URL
MATCHMAKING_SERVER_URL=http://localhost:4000
```

### Server (`doa-server/.env.local`):
```
# Solana devnet RPC
SOLANA_DEVNET_RPC_URL=https://api.devnet.solana.com
GORBAGANA_DEVNET_RPC_URL=https://rpc.gorbagana.wtf
# Program ID (devnet)
DEVELOPMENT_PROGRAM_ID=5RV8MAYjHoSb16VkqjqN5KGX139MULDR6GHuYhxettKT
PRODUCTION_PROGRAM_ID=GAB3CVmCbarpepefKNFEGEUGw6RzcMx9LSGER2Hg3FU2
# Server authority keypair (keep this secret!)
SERVER_AUTH_KEYPAIR=[]
```

---

## 4. Start the Server

In the `doa-server` directory:
```
node matchmaking.cjs
```

The server will listen on port 4000 by default.

---

## 5. Start the Game UI

In a new terminal, in the `doa-ui` directory:
```
pnpm dev
```

The UI will be available at [http://localhost:3000](http://localhost:3000)

---

## 6. Play with a Friend
- Both players should open [http://localhost:3000](http://localhost:3000) in their browsers (can be on the same machine or LAN).
- Each player connects their Solana wallet (Phantom, Solflare, etc.) on devnet.
- Select a character, stake, and enter the battle!

---

## 7. (Optional) Use Fly.io or Railway for Remote Server
- Deploy the server to [Fly.io](https://fly.io) or [Railway](https://railway.app) for remote play.
- Update `MATCHMAKING_SERVER_URL` in `.env.local` in the UI to point to your deployed server URL.

---

## Troubleshooting
- Make sure both UI and server are running and accessible.
- Ensure wallets are funded with devnet SOL (use a faucet if needed).
- Check environment variables for typos.

---

Enjoy battling in Daughters of Aether!
