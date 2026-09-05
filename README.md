# Cabiir

Cabiir is a shared travel registration workspace for the Hargeisa and Jidda teams. Both dashboards use the same Express API and MongoDB collections.

## Setup

1. Copy `backend/.env.example` to `backend/.env` and set `MONGODB_URI` to your MongoDB connection string.
2. Set `JWT_SECRET` and separate Hargeisa/Jidda usernames and passwords in `backend/.env`.
3. Run `npm install --prefix frontend` and `npm install --prefix backend`.
4. Run `npm run dev:full` from the project root for the Vite frontend and Express API together.

The frontend is available at `http://localhost:5173` and the API at `http://localhost:5000`.

On first startup, the backend seeds the configured Hargeisa and Jidda manager accounts if their usernames do not already exist. Passwords are stored as bcrypt hashes and never returned by the API.

## Available API routes

Each of `/api/cumrah`, `/api/hajj`, and `/api/visitors` supports `GET`, `POST`, `GET /:id`, `PUT /:id`, and `DELETE /:id`. The manager profile image uses `PUT /api/manager/profile` with a multipart `profile` file field.

`npm run build` type-checks and builds the frontend. `npm --prefix backend run check` validates backend syntax.
# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend enabling type-aware lint rules by installing `oxlint-tsgolint` and editing `.oxlintrc.json`:

```json
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "plugins": ["react", "typescript", "oxc"],
  "options": {
    "typeAware": true
  },
  "rules": {
    "react/rules-of-hooks": "error",
    "react/only-export-components": ["warn", { "allowConstantExport": true }]
  }
}
```

See the [Oxlint rules documentation](https://oxc.rs/docs/guide/usage/linter/rules) for the full list of rules and categories.
