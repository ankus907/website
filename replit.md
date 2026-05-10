# Workspace

## Overview

APRA Projects / BuildCo — 3D construction company website built with React, Three.js, and Tailwind CSS. Dark industrial brutalist theme with high-vis orange accents. Features a 3D animated hero section with WebGL (CSS fallback), scroll animations via Framer Motion, and sections for About, Services, Projects, Stats, Process, Clients/Team, and Contact.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **Frontend**: React + Vite + Tailwind CSS v4
- **3D**: Three.js + @react-three/fiber + @react-three/drei
- **Animations**: Framer Motion
- **Routing**: Wouter
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Artifacts

- **builder-website** (`artifacts/builder-website/`) — Main website at `/`
  - Hero3D section with WebGL 3D scene + CSS fallback
  - About, Stats, Services, Process, Projects, Clients sections
  - Navbar with mobile hamburger menu
  - Footer with contact info and regional offices

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
