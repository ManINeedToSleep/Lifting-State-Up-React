# Lifting State Up in React

> A simple React application demonstrating state sharing between components using the "lifting state up" pattern.

**Topics:** react typescript vite state-management hooks useState component-communication react19

This React application demonstrates the concept of "lifting state up" in React - a pattern where state is moved from child components to their parent to share state between multiple components.

## Project Overview

The application contains a simple counter example where:
- State is managed in the parent `App` component 
- Two instances of the `Counter` component share the same state
- When one counter is incremented or decremented, the other counter reflects the same value

## Features

- Built with React 19 and TypeScript
- Uses React's useState hook for state management
- Demonstrates the key React concept of lifting state up
- Modern Vite-based build system

## Getting Started

### Prerequisites

- Node.js (version 16 or higher recommended)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone [repository-url]
```

2. Install dependencies
```bash
npm install
```

3. Run the development server
```bash
npm run dev
```

## Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview the production build

## Technologies Used

- React 19
- TypeScript
- Vite
- ESLint

## Project Structure

```
/
├── public/            # Static assets
├── src/
│   ├── components/    # Reusable components
│   │   └── Counter.tsx
│   ├── App.tsx        # Main application component
│   └── main.tsx       # Application entry point
└── package.json       # Project dependencies and scripts
```

## Learning Resources

For more information on "lifting state up" in React, check:
- [React Documentation on Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
