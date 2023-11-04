# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
   parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
   },
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list


# How to set up React Testing Library in Vitest when using Vite. 
1. npm install vitest --save-dev
2. add test script to package.json
3. add simple test - App.test.tsx
4. run `npm run test`
5. add react-testing-library...
6. `npm install jsdom --save-dev
7. modify vite.config.ts
8. add npm react-testing-library `npm install @testing-library/react @testing-library/jest-dom --save-dev`
9. add a test setup file in tests/setup.js - this is where we configure the testing library
10. modify jest.config.js to point to the setup file
11. add a test - App.test.tsx with render(<App />) and expect to find the text "Hello World"
