# Agentic Wallet Kit

A polished starter repo for the **DeFi Developer Challenge – Agentic Wallets for AI Agents**.

## What this repo includes

- A clean Next.js dashboard for the demo story
- API routes to create and run agent wallets
- Programmatic Solana wallet creation with `Keypair.generate()`
- Devnet airdrop flow for fresh agent wallets
- Demo SPL token minting for each agent
- Policy-based transaction checks before signing
- Basic local persistence for agents and action logs
- `SKILLS.md` for agent-readable capabilities
- A written deep dive in `docs/deep-dive.md`

## Why this angle is stronger than a basic wallet demo

A lot of entries will likely show a wallet and one transaction.
This repo is shaped around a better judge experience:

1. Create agent wallets programmatically
2. Fund them on devnet
3. Let the agent run a scripted action
4. Show an approved transaction
5. Show a blocked transaction before signing

That last step matters because it makes security visible.

## Local setup

1. Install dependencies

```bash
npm install
```

2. Copy environment variables

```bash
cp .env.example .env.local
```

3. Start the app

```bash
npm run dev
```

4. Open the app

```bash
http://localhost:3000
```

## Suggested live demo flow

- Click **Create agent** two or three times
- Run a scenario for one agent
- Explain that the backend creates a wallet in code
- Show the airdrop event on devnet
- Show SPL minting for the agent
- Show the approved SOL transfer
- Point out the blocked transfer that exceeded the spend cap

## Important note

This is a strong starter, not a finished production wallet. Before final submission, tighten:

- key storage
- explorer links in the UI
- richer logs
- better transaction status polling
- protocol-specific interaction instead of only the demo flow
- deployment and public demo URL

## What to improve before submission

- Replace file-based storage with a proper datastore or encrypted vault
- Add WebSocket subscriptions for live balance updates
- Add a dedicated devnet protocol interaction beyond token minting
- Record a short walkthrough video
- Publish the repo publicly

## File map

```text
app/
  api/agents/create/route.ts
  api/agents/run/route.ts
  globals.css
  layout.tsx
  page.tsx
components/
  dashboard.tsx
lib/
  agents.ts
  policy.ts
  solana.ts
  store.ts
  types.ts
docs/
  deep-dive.md
README.md
SKILLS.md
```
