
# React TypeScript Prettier Boilerplate

This project is a boilerplate for setting up a React + TypeScript environment with good practices and essential tools. It uses **Vite** as the build tool, **Prettier** for formatting, **ESLint** for linting, **Husky** for git hooks, and **Lint-staged** to run linting tasks on staged files.

## Features

- **React** and **TypeScript** integration
- **Vite** for fast development and bundling
- **ESLint** with TypeScript and React plugins for linting
- **Prettier** with custom configuration for code formatting
- **Husky** for git hooks to enforce code quality
- **Lint-staged** for running linting and formatting on staged files only

## Installation

### Prerequisites
Make sure you have **Node.js** and **npm** installed. You can download them from [nodejs.org](https://nodejs.org/).

### Setup
1. Install dependencies:
   ```bash
   npm install
   ```

2. Install **Husky** and set up git hooks:
   ```bash
   npm run prepare
   ```
   This will install Husky and configure the pre-commit hook to run lint-staged.

## Available Scripts

In the project directory, you can run:

### `npm run dev`

Starts the Vite development server. Open [http://localhost:5173](http://localhost:5173) to view the app.

### `npm run build`

Builds the project for production using **TypeScript** and **Vite**.

### `npm run lint`

Runs ESLint on the entire project to check for linting errors.

### `npm run lint:fix`

Runs ESLint and automatically fixes linting errors where possible.

### `npm run format`

Formats the entire project using Prettier according to the configuration.

### `npm run preview`

Preview the production build of the app.

## Prettier Configuration

Prettier is configured to format your code with the settings such as:

- No semicolons
- Single quotes for strings
- Trailing commas where possible
- Indentation with 2 spaces
- Max line width of 100 characters
- Sorting and organizing imports
- Formatting JSX attributes

It also uses up-to-date plugins. The `.prettierrc.js` file contains the detailed configuration.

**NOTE:** You can uncomment tailwind plugin if you want to use it. If so, you have to install this package by npm:
   ```bash
      npm install prettier-plugin-tailwindcss --save-dev
   ```

## ESLint Configuration

ESLint is set up with the following rules:

- TypeScript and React specific rules
- Rules for better code quality and best practices, including preventing unused variables, ensuring consistent code style and catching common errors

The `eslint.config.js` file contains the detailed configuration.

## Husky and Lint-staged

- Husky ensures that before each commit, lint-staged will run and lint/format staged files to enforce code quality.
- Lint-staged is configured to run **ESLint** and **Prettier** on the appropriate files.

## License

This project is licensed under the MIT License - see [Wiki](https://en.wikipedia.org/wiki/MIT_License) for details.
