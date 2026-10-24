# TypeScript AI Template

A TypeScript template for building projects with AI on a solid foundation.

Start with a single `index.ts` and a shared set of strict compiler checks,
lint rules, and formatting conventions to guide both you and your AI coding assistant.

## Features

- **Minimal starting point** — one source file that prints `Hello, World`.
- **Strict TypeScript** — checks for unsafe access, unused code, and inconsistent types.
- **Consistent code quality** — ESLint with type checking, import rules, SonarJS, and Unicorn.
- **Automatic formatting** — Prettier integrated with ESLint.
- **Development workflow** — compilation, automatic restarts, and source maps.
- **Node.js and NestJS compatibility** — ESM and decorator metadata configured in advance.
- **GitHub Actions** — formatting, linting, type checking, and builds on pushes and pull requests.

## Requirements

- Node.js **24+**
- npm **11 or later**

## Quick start

Install dependencies and start development:

```sh
npm ci
npm run dev
```

The entry point is [`src/index.ts`](src/index.ts):

```ts
console.log('Hello, World');
```

Changes in `src/` are compiled automatically. The application restarts after a successful compilation.

To build and run the compiled application:

```sh
npm run build
npm start
```

## Commands

| Command                | Description                                                                      |
| ---------------------- | -------------------------------------------------------------------------------- |
| `npm run dev`          | Watch TypeScript files and restart the application after successful compilation. |
| `npm run build`        | Remove the previous `dist/` output and compile the application.                  |
| `npm start`            | Run `dist/index.js` with source maps enabled. Requires a build first.            |
| `npm run typecheck`    | Check types without emitting JavaScript.                                         |
| `npm run lint`         | Check code with ESLint without modifying files.                                  |
| `npm run lint:fix`     | Apply available ESLint fixes.                                                    |
| `npm run format`       | Format project files with Prettier.                                              |
| `npm run format:check` | Check formatting without modifying files.                                        |
| `npm run check`        | Run formatting, linting, and type checks in sequence.                            |
