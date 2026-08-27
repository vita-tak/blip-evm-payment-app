# Blip Payment

A decentralized peer-to-peer payment application on Ethereum.
Stablecoin transfers with a guardian approval system that requires
explicit approval before incoming payments are accepted. Deployed to Polygon Amoy.

## How it works

Users can send stablecoin payments directly to recipients. Recipients can optionally configure guardians;
trusted addresses that must approve incoming payments before funds
are released. This gives users control over what they receive,
without relying on a central intermediary.

## Key Features

**Peer-to-peer stablecoin payments** on EVM chains

**Guardian system** — require approval before accepting payments

**Non-custodial** — funds handled by contracts, never a central party

**Privy authentication** — seamless wallet and social login

## Tech Stack

Deployed to Polygon Amoy. [View contract on Polyscan](https://amoy.polygonscan.com/address/0x70bf1cA32Bf17bd05C014E80cAb4bf770a2c3E6B)

| Layer | Technology |
|---|---|
| Smart Contracts | Solidity, Foundry |
| Frontend | Next.js, React, wagmi, viem, TanStack Query, Tailwind CSS |
| Backend | NestJS, TypeScript, Prisma, PostgreSQL, Privy |
| Auth | Privy |
| Tools | Docker, Git |

## Getting Started

### Prerequisites
Foundry installed, Node.js 18+, PostgreSQL running locally

### Contracts
```bash
cd contracts
forge install
forge build
forge test
```

### Backend
```bash
cd backend
cp .env.example .env
pnpm i
npx prisma migrate dev
pnpm run dev
```

### Frontend
```bash
cd frontend
pnpm i
pnpm run dev
```

### Docker
```bash
docker-compose up
```
