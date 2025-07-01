<img src="cover.png"/>

## Daughters of Aether – Project Overview & Setup Guide

Daughters of Aether is a real-time Web3 PvP arena game built on Solana, featuring:
- 3D character selection and battles
- On-chain staking and rewards
- Real-time matchmaking and multiplayer combat
- A modern, animated UI with wallet integration

## Play the Game

Try the live game here: [https://daughter-of-aether.vercel.app/](https://daughter-of-aether.vercel.app/)

---

## Project Structure

This project is split into three main repositories:

- **Frontend UI:** [github.com/DavidNzube101/DOA-](https://github.com/DavidNzube101/DOA-)
  - Nuxt 3 + Vue 3 + Three.js game client
  - Wallet connection, 3D arena, matchmaking, and battle UI
  - **See the README in this repo for detailed setup and environment variable instructions.**

- **Backend Server:** [github.com/DavidNzube101/DOA-server-](https://github.com/DavidNzube101/DOA-server-)
  - Node.js + Socket.IO matchmaking and battle state server
  - Handles contract calls, player state, and auto-resolution
  - **See the README in this repo for deployment, environment, and security notes.**

- **Solana Smart Contract:** [github.com/DavidNzube101/DOA-Contract](https://github.com/DavidNzube101/DOA-Contract)
  - Anchor-based Solana program for battles, staking, and resolution
  - **See the README in this repo for build, deploy, and customization instructions.**

---

## Game Overview

- **Connect your Solana wallet** (Phantom, Solflare, Backpack, etc.)
- **Select a character** and stake tokens to enter the arena
- **Matchmaking** pairs you with another player in real time
- **Battle in a 3D arena** with health, mana, and special moves
- **Winner takes all**: the total stake pool is awarded to the victor
- **All results are settled on-chain** for transparency and fairness

---

## Local Setup

If you want to run Daughters of Aether locally (for development, testing, or hacking):

1. **Clone each repository:**
   - [Frontend UI](https://github.com/DavidNzube101/DOA-)
   - [Backend Server](https://github.com/DavidNzube101/DOA-server-)
   - [Solana Contract](https://github.com/DavidNzube101/DOA-Contract)

2. **Follow the setup guides in each repo:**
   - Each repository contains a detailed README with environment variables, build steps, and troubleshooting.
   - The UI and server can be run locally with Node.js and pnpm.
   - The contract can be deployed to Solana devnet or Gorbagana testnet (see contract README for advanced deployment).

3. **Configure your environment:**
   - Set up `.env` files as described in each repo.
   - Fund your wallets with devnet SOL or GOR as needed.

4. **Start the backend, then the frontend, and play!**

---

## Need Help?
- Each repo README covers common issues and troubleshooting.
- For advanced contract deployment or customization, see the contract repo.
- For live support, open an issue in the relevant repository.

---

Enjoy battling in Daughters of Aether!
