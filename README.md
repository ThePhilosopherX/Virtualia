# Virtualia

Virtualia is an on-chain platform to highlight academic productions such as articles, translations, courses, and certificates, allowing creators to monetize their content via tokens on the Solana network.

## Repository Structure

- `frontend/`: Web application (React + Vite) integrated with Solana wallets.
- `contracts/`: Program (smart contract) written with Anchor to manage content minting.
- `backend/`: Node.js API responsible for persisting user profiles and certificates in a MongoDB cluster.
- `docs/`: Supplementary documentation about architecture, flows, and references.

## Getting Started

1. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
   
2. **Set up the Anchor environment** (see `docs/backend-setup.md`).
3. **Implement and test the end-to-end flow**  following the development guide ('docs/architecture.md').

### Backend API

1. Create a `.env` file inside `backend/` based on `.env.example` with the MongoDB cluster connection string (`MONGODB_URI`).
2. Install dependencies and start the server:

   ```bash
   cd backend
   npm install
   npm run dev
   ```

3. Use the REST endpoints to create or update profiles (`POST /api/users`), query (`GET /api/users/:walletAddress`), attach new certificates (`POST /api/users/:walletAddress/certificates`), and authenticate users by email (`POST /api/users/auth/login`).


## Current Status

This repository provides a functional skeleton with the essential elements to start the prototype:

- UI with Solana wallet connection, minting form, and local listing of created assets.
- Anchor program that stores academic content metadata on-chain and distributes symbolic rewards in tokens.

From this point, it is possible to evolve toward integrations with decentralized storage, real NFT/SPL Token issuance, and application deployment.


# Virtualia (Portuguese Version)

Virtualia é uma plataforma on-chain para destacar produções acadêmicas como artigos, traduções, cursos e certificados, permitindo que criadores monetizem seus conteúdos via tokens na rede Solana.

## Estrutura do repositório

- `frontend/`: Aplicação web (React + Vite) com integração a carteiras Solana.
- `contracts/`: Programa (smart contract) escrito com Anchor para gerenciar a mintagem de conteúdos.
- `backend/`: API Node.js responsável por persistir perfis de usuários e certificados em um cluster MongoDB.
- `docs/`: Documentação complementar sobre arquitetura, fluxos e referências.

## Começando

1. **Instale as dependências do frontend**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
2. **Configure o ambiente Anchor** (veja `docs/backend-setup.md`).
3. **Implemente e teste o fluxo ponta a ponta** seguindo o guia de desenvolvimento (`docs/architecture.md`).

### Backend API

1. Crie um arquivo `.env` dentro de `backend/` baseado em `.env.example` com a string de conexão do cluster MongoDB (`MONGODB_URI`).
2. Instale as dependências e inicie o servidor:

   ```bash
   cd backend
   npm install
   npm run dev
   ```

3. Utilize os endpoints REST para criar ou atualizar perfis (`POST /api/users`), consultar (`GET /api/users/:walletAddress`), anexar novos certificados (`POST /api/users/:walletAddress/certificates`) e autenticar usuários pelo e-mail (`POST /api/users/auth/login`).

## Estado atual

Este repositório traz um esqueleto funcional com os elementos essenciais para iniciar o protótipo:

- UI com conexão a carteira Solana, formulário de mint e listagem local dos assets criados.
- Programa Anchor que armazena metadados on-chain de conteúdos acadêmicos e distribui recompensas simbólicas em tokens.

A partir deste ponto é possível evoluir para integrações com storage descentralizado, emissão real de NFTs/SPL Tokens e publicação da aplicação.
