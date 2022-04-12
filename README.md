# npm
 - what is npm ?  NPM  is a package managar for javascpit.  
 - it is the largest online package manager repository.

## 1. package.json
 - npm init or npm init -y
 - A standard Node.js project contains a file called package.json.
 - It is a JSON manifest file which holds all of the relevant data to the app.
 - `package.json` only tracks top-level dependencies for the project.
1. want to publish
 - name, author, license, description — Important if you want to publish your repository.

2. Version
  - If you are maintaining an open-source npm package, you should update it according to the semantic conventions. 3.7.2– 3 is the major version, 7 is the minor version, and 2 is the patch.
3. Scripts 
     - Here we put out project’s scripts: building, testing, linting, deploying, etc.
     - Each project can have custom-made scripts adapted for a unique use-case
     - Custom scripts can be added and used by developers to enhance development capabilities
     - For example, executing end-to-end tests in a specific directory.

4. dependencies
- Required for building the project. 
- A dependency is a library that a project needs to function effectively.

5. DevDependencies
- DevDependencies are the packages a developer needs during development.
- The dependencies needed only for the development of the project but not for building it.

## package-lock.json
- package-lock.json is generated automatically for any operations where npm modifies either the node_modules tree, or package.json. It describes the exact tree that was generated, such that subsequent installs can generate identical trees. This is used to save an exact copy of the packages to ensure that the program works the same on different machines.
## node_modules
- When you run npm install, npm installs the required packages into your project root directory in a folder called node_modules.
## commands

0. npm init 
 * command:- npm init 
 * flag:- -y

1. npm install 
  * command:- npm i
  * command:-  install <package> 
  * flags: - -S is the same as --save, and -D is the same as --save-dev

2. npm uninstall 
  * command:- npm uninstall <package>
  * command:- npm un

3. npm update
  * flags: -g
  * command:
  - npm update <package>
  * command:- npm up

4. npm -l
  - dispay full usage info.

5. npm outdated
 - installed packages are currently outdated.

6. npm remove
 - uninstall the pakage.json

7. npm audit 
 - npm audit is a built-in security feature, that scans your project for security vulnerabilities.

8. npm cache clean --force
- The errors are categorized as:
- Random errors
- Permission errors
- No space
- Version control error
- Invalid JSON 

9. npm ci 
 - There is a package-lock.json 
 - The project must have an existing package-lock.json
 - It will never write to package.json or any of the package-locks: installs are essentially frozen.

## reference
- [The Complete Guide To Npm ](https://medium.com/analytics-vidhya/the-complete-guide-to-npm-ac52fbc43f6c)
