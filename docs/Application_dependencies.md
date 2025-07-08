This project includes both frontend and backend applications with their own dependencies and a shared root-level configuration.

## Root-Level
- **Scripts:** Contains commands for test, build, and deploy for both apps.
- **Dependencies:** None, acts as orchestrator.

## Backend (udagram-api)
- **Runtime:** Node.js 14
- **Main Dependencies:**
  - Express
  - Sequelize (PostgreSQL ORM)
  - AWS SDK
  - Bcryptjs (password hashing)
  - JSON Web Token (authentication)
- **Dev Dependencies:**
  - TypeScript
  - ESLint
  - ts-node-dev

  ## Frontend (udagram-frontend)
  - **Runtime:** Angular 8, Ionic
  - **Main Dependencies:**
    - Angular core packages
    - Ionic UI framework
    - RxJS
  - **Dev Dependencies:**
    - Angular CLI
    - TypeScript
