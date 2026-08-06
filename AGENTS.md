# AGENTS.md

## Repository overview
- This repository is a Next.js App Router quickstart for creating and using Crossmint wallets.
- The app authenticates users with Crossmint Auth, creates a wallet on login, and shows wallet balances, activity, and transfer flows.

## Stack
- Next.js 15
- React 19
- TypeScript with `strict` mode enabled
- Tailwind CSS 4
- `@crossmint/client-sdk-react-ui`

## Common commands
- Install dependencies: `pnpm install`
- Start local dev server: `pnpm dev`
- Build for production: `pnpm build`
- Lint: `pnpm lint`

## Environment
- Copy `.env.template` to `.env` before local development.
- Required: `NEXT_PUBLIC_CROSSMINT_API_KEY`
- Optional: `NEXT_PUBLIC_CHAIN` (defaults to `solana` in `/home/runner/work/wallets-quickstart/wallets-quickstart/app/providers.tsx`)
- Never commit real API keys or other secrets.

## Important files
- `/home/runner/work/wallets-quickstart/wallets-quickstart/app/layout.tsx` wires global fonts, providers, and analytics.
- `/home/runner/work/wallets-quickstart/wallets-quickstart/app/providers.tsx` sets up Crossmint providers and wallet creation behavior.
- `/home/runner/work/wallets-quickstart/wallets-quickstart/app/page.tsx` switches between the landing page and authenticated dashboard.
- `/home/runner/work/wallets-quickstart/wallets-quickstart/components/` contains the UI for dashboard, balances, activity, transfers, and auth actions.
- `/home/runner/work/wallets-quickstart/wallets-quickstart/lib/utils.ts` contains shared utilities like the `cn` class name helper.

## Conventions
- Use the `@/` path alias for local imports.
- Keep components in TypeScript/TSX and follow the existing semicolon + double-quote style.
- Add `"use client";` to components that rely on React hooks, browser APIs, or Crossmint client hooks.
- Prefer extending the existing provider and component structure instead of introducing new app-wide patterns.
- Keep styling inline with existing Tailwind utility usage unless there is a strong reason to extract it.

## Validation guidance
- For code changes, run `pnpm lint` and `pnpm build` when the affected area warrants it.
- There is no dedicated test suite in the repository today, so linting and building are the primary validation steps.
