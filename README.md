# Backend Template (NestJS + Prisma)

A production-ready, scalable backend starter template built with **NestJS**, **Prisma ORM**, **PostgreSQL**, and modern development tooling.

---

## 🚀 Features

- **Framework**: [NestJS](https://nestjs.com/) (Modular, scalable architecture)
- **Database & ORM**: [Prisma ORM](https://www.prisma.io/) with PostgreSQL support
- **Configuration**: `@nestjs/config` for environment variable management
- **Observability**: `@nestjs/observe` integration for APM, tracing, and logging
- **Linter & Formatter**: [Oxlint](https://oxc.rs/) (high-performance linting) & [Prettier](https://prettier.io/)
- **Testing**: [Vitest](https://vitest.dev/) for blazing fast unit and E2E tests
- **Module System**: Pure ECMAScript Modules (ESM) support

---

## 📁 Project Structure

```text
├── prisma/
│   ├── schema.prisma      # Database schema definitions
│   └── ...
├── src/
│   ├── prisma/            # Prisma service & module
│   ├── app.controller.ts  # Base health-check controller
│   ├── app.module.ts      # Root application module
│   ├── app.service.ts     # Root application service
│   └── main.ts            # Application bootstrap entrypoint
├── test/                  # E2E test files
├── .env.example           # Example environment configuration
├── package.json
└── tsconfig.json
```

---

## 🛠️ Getting Started

### 1. Prerequisites

- [Node.js](https://nodejs.org/) (v20+ recommended)
- [PostgreSQL](https://www.postgresql.org/) database (local or cloud like Supabase / Neon)

### 2. Environment Setup

Clone the project and copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

Update your database credentials and configuration in `.env`:

```env
PORT=8000
NODE_ENV="development"
DATABASE_URL="postgresql://user:password@localhost:5432/mydb?schema=public"

OBSERVE_APP_KEY="your-observe-key"
OBSERVE_APP_SECRET="your-observe-secret"
OBSERVE_SERVICE_ID="backend"
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Database Setup & Prisma Client

Generate Prisma Client and apply migrations:

```bash
npx prisma generate
npx prisma db push
```

---

## 🏃 Running the Application

```bash
# Development mode with watch
npm run start:dev

# Production build
npm run build

# Start production server
npm run start:prod
```

Once running, visit [http://localhost:8000](http://localhost:8000) to verify the health check endpoint.

---

## 🧪 Testing & Quality

```bash
# Run unit tests (Vitest)
npm run test

# Run tests in watch mode
npm run test:watch

# Run E2E tests
npm run test:e2e

# Run linter (Oxlint)
npm run lint

# Format code (Prettier)
npm run format
```

---

## 📄 License

This project is licensed under the MIT License.
