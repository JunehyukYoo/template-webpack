# Webpack Template Starter

This repository provides a clean and modular setup for modern JavaScript projects using **Webpack**. It supports development and production builds, and includes support for deploying to GitHub Pages via `dist/`.

## 📁 Project Structure

```
.
├── dist/                  # Compiled production files (generated)
├── node_modules/          # Installed dependencies
├── src/                   # Source code (HTML, JS, CSS)
│   └── template.html      # HTML template used by HtmlWebpackPlugin
│   └── index.js           # Entry point for app logic and bundling
├── .gitignore             # Ignores node_modules and dist from Git
├── .prettierignore        # Add files to ignore while formatting here
├── package.json           # Project metadata and scripts
├── eslint.config.mjs      # eslint configuration
├── webpack.common.js      # Shared Webpack config
├── webpack.dev.js         # Dev-specific Webpack config
├── webpack.prod.js        # Prod-specific Webpack config
├── README.md              # You're here!
```

## ⚙️ Scripts

Defined in `package.json`:

```json
"scripts": {
  "build": "webpack --config webpack.prod.js",
  "dev": "webpack serve --open --config webpack.dev.js",
  "deploy": "git subtree push --prefix dist origin gh-pages",
  "lint": "eslint 'src/**/*.{js,jsx}'",
  "format": "prettier --write 'src/**/*.{js,jsx,css,html}'"
}
```

### 🔧 Script Breakdown:

| Command          | Description                                                                                  |
|------------------|----------------------------------------------------------------------------------------------|
| `npm run build`  | Builds the project for production. Output goes to the `/dist` folder.                         |
| `npm run dev`    | Runs the development server at `http://localhost:8080/` and opens the browser.               |
| `npm run deploy` | Deploys `/dist` to the `gh-pages` branch using Git Subtree.                                  |
| `npm run lint`   | Runs ESLint v9 on your source code to check for code quality and potential issues.             |
| `npm run format` | Formats your code using Prettier for consistent styling.                                      |

## 🔍 Linting and Formatting

This project now includes **ESLint v9** for linting and **Prettier** for code formatting. To ensure that your code remains both error-free and well-formatted, the following packages have been added:

- **ESLint v9:** Checks your code for common errors and enforces coding standards.
- **Prettier:** Automatically formats your code to maintain a consistent style.
- **eslint-config-prettier:** Disables ESLint rules that might conflict with Prettier, so you only see issues that require your attention.

### How to Use:

1. **Lint Your Code:**  
   Run the following command to check your source code for issues:
   ```bash
   npm run lint
   ```
   To check a specific file, you can instead run the build-in command:
   ```bash
   npx eslint FILENAME.js
   ```

2. **Format Your Code:**  
   Automatically format your code using Prettier by running:
   ```bash
   npm run format
   ```
   To check or format (write to) a file, you can instead run the build-in commands (respectively):
   ```bash
   npx prettier --check FILENAME.js
   npx prettier --write FILENAME.js
   ```


3. **Configuration Files:**  
   You can adjust ESLint and Prettier settings by editing the configuration files (typically `.eslintrc.json` or `.eslintrc.js` for ESLint, and `.prettierrc` or `prettier.config.js` for Prettier) in your project root.

## ✅ Setup Instructions

1. **Clone the repo:**

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Start development server:**

   ```bash
   npm run dev
   ```

4. **Build for production:**

   ```bash
   npm run build
   ```

5. **Deploy to GitHub Pages (optional):**

   Make sure your repo has a `gh-pages` branch and run:

   ```bash
   npm run deploy
   ```

## 📦 What’s Included

- ✅ Webpack 5
- ✅ Dev server with live reload
- ✅ Source maps
- ✅ Production optimization (minified JS/CSS)
- ✅ HTML template integration via `HtmlWebpackPlugin`
- ✅ GitHub Pages deployment via `subtree push`
- ✅ ESLint v9 integration for linting
- ✅ Prettier for consistent code formatting
- ✅ `.gitignore` set up for `node_modules` and `dist`

## 🧠 Notes

- The actual source code goes in the `src/` folder.
- You can modify `src/template.html` and `src/index.js` to kick off your project.
- Use the `webpack.common.js`, `webpack.dev.js`, and `webpack.prod.js` files to customize your build process.

## 📝 License

This project is a boilerplate/template and is free to use under the [MIT License](LICENSE).
