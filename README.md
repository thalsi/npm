# NPM


1. What is npm?
  - npm (Node Pakage Manager) is a package manager for the Javascript programming lamguage.
  - npm is the world's largest Software Registry.
  - NPM consists of three main parts:  
    1. Website (npmjs.com)
      - The official npm website allows users to discover, browse, and search for packages.
      - lets users create and manage accounts, as well as publish and manage packages
    2. CLI (Command Line Interface)
        - The npm CLI is a tool used to interact with npm directly from the command line.
    3. Registry
        - The npm registry is a massive public database(online repository) of JavaScript packages

2. Installation
  - NPM comes pre-installed with Node.js.

## Commands

1. Basic npm Commands

| Command	            | Alias	         |                     Description                    |
|:-----------------   |:--------------:|:---------------------------------------------------|
| npm init	          | -	             | Initializes a new project with a package.json file.|
| npm init -y	        | -	             | Initializes a project with default values.         |
| npm install	        | npm i	         | Installs all dependencies listed in package.json.  |
| npm install <pkg>	  | npm i <pkg>	   | Installs a specific package locally to the project.|
| npm uninstall <pkg>	| npm rm <pkg>	 | Removes a package from the project dependencies.   |
| npm update	        | -	             | Updates all packages to their latest version.      |
| npm outdated	      | -	             | Shows outdated packages in the project.            |
| npm run <script>	  | -	             | Runs a script defined in the package.json.         |
| npm start	          | -	             | Runs the start script defined in package.json.     |
| npm stop	          | -	             | Runs the stop script defined in package.json.      |
| npm restart	        | -	             | Restarts a Node.js application.                    |
| npm test	          | -	             | Runs the test script defined in package.json.      |
| npm link	          | -	             | Links a global package as a local dependency.      |

