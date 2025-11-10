# Todo App (React + Vite)

A small Todo application built with React and Vite. This project demonstrates a simple todo list using context, localStorage persistence, and Tailwind-style utility classes for layout.

## Features

- Add, edit, delete todos
- Toggle todo completion (stored in localStorage)
- Simple context-based state management (`TodoContext`)

## Tech stack

- React
- Vite
- Tailwind-style utility classes (project already uses Tailwind class names)

## Prerequisites

- Node.js (v16+ recommended)
- npm (or yarn)
- Git (optional, for pushing to a remote)

## Quick start (Windows PowerShell)

Clone the repo (if you haven't already):

```powershell
git clone https://github.com/USERNAME/REPO.git
cd "Todo App"
```

Install dependencies and run the dev server:

```powershell
npm install
npm run dev
```

Open the shown local URL (usually http://localhost:5173) in your browser.

## Available scripts

- `npm run dev` — start the dev server (Vite)
- `npm run build` — produce a production build
- `npm run preview` — locally preview the production build
- `npm run lint` — run eslint across the project

## Project structure (important files)

- `src/App.jsx` — main app and provider wiring
- `src/components/TodoForm.jsx` — form to add new todos
- `src/components/TodoItem.jsx` — single todo row, edit/delete/toggle
- `src/context/TodoContext.js` — context provider and hooks
- `index.html`, `vite.config.js`, `package.json` — project config

## How to use the app

1. Open the app in your browser.
2. Use the input field to type a todo and press Add.
3. Click the pencil button to edit (if not completed). Click the checkbox to toggle complete. Click ❌ to delete.
4. Todos are saved to `localStorage` and will persist across page reloads.

## Committing your changes (Git)

If you edit files and want to push changes to GitHub, run these commands in PowerShell (replace values where needed):

```powershell
git add -A
git commit -m "Describe your changes"
git push origin main
```

If `git` isn't recognized, install Git for Windows from https://git-scm.com/download/win and restart your terminal.

## Troubleshooting

- If you see an import/export error (e.g. "does not provide an export named ..."), check that components using `export default` are imported as default imports (no braces):

```js
// correct for default export
import TodoForm from './components/TodoForm.jsx'

// incorrect for default export
// import { TodoForm } from './components/TodoForm.jsx'
```

- If the dev server doesn't start, confirm Node/npm versions and that dependencies installed without errors.

## Contributing

If you'd like to add features or fixes:

1. Create a new branch: `git checkout -b feat/your-feature`
2. Make changes and commit logically
3. Push and open a PR to the `main` branch

## License

Choose a license for your project (e.g. MIT) or keep it private.

---

If you want, I can also:

- Add a CONTRIBUTING.md and a simple CODE_OF_CONDUCT
- Wire up Tailwind config / ensure Tailwind is installed and configured
- Add a small test or CI workflow

Tell me which of those you'd like next.

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
