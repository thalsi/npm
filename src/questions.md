## Questions

1. What is npm?
2. What is npm’s package.json?
3. What is npm’s package-lock.json?
4. What are the differences between “npm install” and “npm ci”?
5. What are the differences in installing conflicting peer dependencies with “force” flag vs “legacy-peer-deps” flag?
6. What will happen if we add type=module section into package.json?
7. What are devDependencies?
8. What are the local paths?
9. What are the scoped names and how they are installed?
10. What is the .npmrc file?
11. What are the Pre & Post Scripts?


1. What is npm?
    - NPM is a package manager for Node.js 

2. What is npm's package.json?
    - package.json is a configuration file used in node.js and javascript to manage project dependencies, scripts, metadata, configuration settings, and dependency information.

3. What is npm’s package-lock.json?
    - The package-lock.json is an automatically generated file in Node.js projects that locks down the exact versions of all dependencies (and their sub-dependencies) installed in your project.

4. How to Add Custom Scripts to package.json?
     -  These 4 scripts can be run without run: start, test, stop, restart

| Script Name | Use `npm run`? | Example                           |
| ----------- | -------------- | --------------------------------- |
| `start`     | ❌ optional     | `npm start` or `npm run start`    |
| `test`      | ❌ optional     | `npm test` or `npm run test`      |
| `build`     | ✅ required     | `npm run build`                   |
| `custom`    | ✅ required     | `npm run format`, `npm run clean` |

```
{
  "scripts": {
    "start": "node index.js",
    "build": "echo Building...",
    "test": "echo Run tests here",
    "lint": "eslint .",
    "format": "prettier --write \"src/**/*.{ts,js,html,css}\""
  }
}

example Scripts
"scripts": {
  "start": "ng serve",
  "build": "ng build --configuration production",
  "test": "ng test",
  "lint": "ng lint",
  "format": "prettier --write \"src/**/*.{ts,html,scss}\"",
  "analyze": "webpack-bundle-analyzer dist/stats.json",
  "clean": "rimraf dist/ && rimraf .angular/cache",
  "prepare": "husky install"
}

```

5. Understand lifecycle scripts (prepare, install)?
| Script Name      | When It Runs                                                                             |
| ---------------- | ---------------------------------------------------------------------------------------- |
| `preinstall`     | Before `npm install` starts                                                              |
| `install`        | After `npm install` finishes                                                             |
| `postinstall`    | After `install` completes (even in CI)                                                   |
| `preuninstall`   | Before uninstalling a package                                                            |
| `postuninstall`  | After uninstall                                                                          |
| `prepare`        | Runs on `npm install` AND before `npm publish`, `npm pack`, or `git push` if using husky |
| `prepublishOnly` | Only before `npm publish`                                                                |
| `prepack`        | Before packaging the module                                                              |
| `postpack`       | After packaging                                                                          |
