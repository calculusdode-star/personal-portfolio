# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Workflow

**Build**
```bash
npm run build
```

**Test**
```bash
npm test
```

**Lint**
```bash
npm run lint
```

## Codebase Architecture

**Core Components**
1. Service Layer - Handles business logic and API integrations
   - Key files: `src/services/`, `api/endpoints/`
2. Domain Models - Persistent data schemas and relationships
   - Key files: `src/domain/`, `database/schema/`
3. Infrastructure - Configuration, caching, and queue management
   - Key files: `src/config/`, `.env` files

**Cross-Cutting Components**
- Authentication - Found in `src/auth/services` and middleware
- Monitoring - Logging in `src/logging/` and metrics in `src/monitoring/`

**Tech Stack**
- Programming Language: [language] (deduced from files like `package.json` or `Cargo.toml`)
- Build Tool: Webpack/Vite/NPM scripts
- Database: [SQL/NoSQL name] with migration folder `src/database/`, `prisma/schema.prisma`
- Testing Framework: Jest/Mocha (for JS/TS) or Rust's `cargo test`

## Development Tools

**CLI Commands**
1. Start dev server: `npm start` or `cargo watch --run`
2. Run test coverage: `npm run coverage` (creates `coverage/` folder)
3. Run linter: `eslint` (JS/TS) or `rustc --borrow-check` for safety checks

**IDE Setup**
- Use: [IDE name] with [plugin names]
- Recommended extensions: [extension names]

## Deployment Process

1. Build release: `npm run build:prod`

## Key Files
- `package.json` - Main project configuration
- `tsconfig.json` or `webpack.config.js` - Build configuration
- `vite.config.js` - Vite build configuration
- `src/` - Source code directory
- `tests/` - Test files