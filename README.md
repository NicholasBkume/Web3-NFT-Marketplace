# OpenD — Decentralized NFT Marketplace

**OpenD** is a decentralized NFT marketplace built on the **Internet Computer Protocol (ICP)**. The project demonstrates a full-stack Web3 architecture where a React/TypeScript frontend communicates with Internet Computer canisters to support NFT creation, ownership, buying, and selling.

## Highlights

- Mint NFTs from the application
- Buy and sell NFTs through decentralized application logic
- Smart-contract-backed ownership and transfers
- Backend canisters hosted on the Internet Computer
- Responsive web interface
- Web3-focused full-stack architecture

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, Webpack |
| Backend | Internet Computer Canisters, Motoko |
| Blockchain | Internet Computer Protocol (ICP) |
| Package manager | npm |
| Local development | DFX SDK |
| Deployment | Internet Computer |

## Architecture

```text
Browser
   │
   ▼
React + TypeScript frontend
   │
   ▼
Internet Computer canister interface
   │
   ▼
Motoko backend canisters
   │
   ▼
ICP network
```

## Prerequisites

Install:

- [DFX SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install/)
- Node.js and npm
- An Internet Computer-compatible identity/wallet when interacting with deployed Web3 functionality

## Run locally

Clone the repository and install dependencies:

```bash
git clone https://github.com/NicholasBkume/Web3-NFT-Marketplace.git
cd Web3-NFT-Marketplace
npm install
```

Start the local Internet Computer replica:

```bash
dfx start --background
```

Deploy the canisters:

```bash
dfx deploy
```

Start the frontend using the project's configured npm script:

```bash
npm start
```

The local application is typically available at:

```text
http://localhost:8080
```

If your local configuration exposes a different port, use the URL reported by the development server.

## Deploy to the Internet Computer

Create or select a DFX identity:

```bash
dfx identity new <identity-name>
dfx identity use <identity-name>
```

Deploy to the Internet Computer main network:

```bash
dfx deploy --network ic
```

After deployment, DFX provides the canister identifiers and URLs needed to access the application.

## Project structure

```text
Web3-NFT-Marketplace/
├── src/                 # Frontend and application source
├── dist/                # Generated build output, when present
├── dfx.json             # Internet Computer configuration
├── package.json         # JavaScript/TypeScript dependencies and scripts
├── webpack.config.js    # Frontend build configuration
├── tsconfig.json        # TypeScript configuration
└── README.md
```

## Development notes

This repository is intended as a Web3/full-stack project and learning portfolio. Before production use, review authentication, authorization, transaction handling, input validation, canister security, and deployment configuration for the current ICP environment.

## Contributing

1. Fork the repository.
2. Create a feature branch:

```bash
git checkout -b feature/your-feature
```

3. Make and test your changes.
4. Commit with a descriptive message:

```bash
git commit -m "feat: describe the change"
```

5. Push your branch and open a pull request.

## License

This project is licensed under the MIT License.