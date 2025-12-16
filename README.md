# ZenithPulse

Built for Base

ZenithPulse is a compact repository focused on validating Base network connectivity, wallet onboarding, and RPC-level reads using official Coinbase tooling.

The project is intentionally minimal and serves as a clean signal that Base infrastructure, explorers, and wallet UX are wired correctly.

---

## Networks & Chain Context

Base Mainnet  
- chainId (decimal): 8453  
- Explorer: https://basescan.org  
- RPC endpoint: https://mainnet.base.org  

Base Sepolia  
- chainId (decimal): 84532  
- Explorer: https://sepolia.basescan.org  
- RPC endpoint: https://sepolia.base.org  

---

## What This Repository Demonstrates

Primary file: `app/zenithPulse.ts`

ZenithPulse performs the following:
- Boots an OnchainKit provider scoped to Base
- Exposes wallet connection UI for account access
- Executes Base JSON-RPC reads via Viem:
  - chainId resolution
  - latest block height
  - native ETH balance for a supplied address
- Outputs Basescan explorers for transparent verification

This makes the repository suitable for quick Base readiness checks and integration testing.

---

## Project Layout

- `app/`
  - `zenithPulse.ts`  
    React entry point combining OnchainKit wallet UX with Base RPC reads.

Typical companion files:
- `package.json`
- `tsconfig.json`
- `index.html` / `main.tsx`
- `.env` (optional)

---

## Libraries in Use

- **OnchainKit**  
  Wallet UI components and Base-first primitives  
  https://github.com/coinbase/onchainkit  

- **Viem**  
  Lightweight EVM client used for Base JSON-RPC queries

---

## Setup & Execution

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run the app with a standard React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

---

## Usage Notes

- Base Sepolia is recommended for validation and experimentation
- Mismatched chainId values usually indicate an incorrect wallet network
- Public RPC endpoints are rate-limited and intended for development workflows

---

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- Contract address:  
  https://basescan.org/address/your_adress  
- Contract verification (source code):  
  https://basescan.org/address/your_adress#code  

---

## License

MIT License

---

## Author

GitHub: https://github.com/Damahand

Public contact (email):cannier-births-0n@icloud.com 

Public contact (X): https://x.com/marciltherese

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more reference contracts may be published to Base Sepolia to confirm compatibility.

**Network:** Base Sepolia  
**chainId (decimal):** 84532  
**Explorer:** https://sepolia.basescan.org  

**Contract #1 address:**  
0x8e84c40a185fd600fd60afd30675b2335a4bfb67

Deployment and verification:
- https://sepolia.basescan.org/address/0x8e84c40a185fd600fd60afd30675b2335a4bfb67 
- https://sepolia.basescan.org/0x8e84c40a185fd600fd60afd30675b2335a4bfb67/0#code  

These testnet deployments act as a sandbox for validating Base tooling, account abstraction–related behavior, and read-only onchain operations before promotion to Base Mainnet.

