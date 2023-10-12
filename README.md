# Keystone CMS Turborepo Bug

This is based on the official starter Turborepo.

## How this repo was made

### 1. I created this repo with Turbo Repo's starter project by running:

```sh
npx create-turbo -e basic
```

### 2. Run the following command:

```sh
npx create-turbo@latest
```

### 3. I then added Keystone CMS to `~/apps/keystone` using

```sh
cd apps
npm init keystone-app@latest keystone
```

### 4. I then modified the keystone package.json to have migrate script:

```json
"migrate": "NODE_ENV=development keystone prisma migrate dev"
```

## How to reproduce the bug

```sh
cd apps/keystone # move to keystone directory
npm run migrate # run our new migrate npm command
```

Receive the following output:

```
Error: Prisma Migrate has detected that the environment is non-interactive, which is not supported.
```

---

---

---

## What's inside?

This Turborepo includes the following packages/apps:

### Apps

- `~/apps/next`: Next.js frontend
- `~/apps/keystone`: Keystone CMS backend

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Build

To build all apps and packages, run the following command:

```
npm build
```

### Develop

To develop all apps and packages, run the following command:

```
npm dev
```
