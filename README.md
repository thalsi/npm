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

###### 1. Basic npm Commands

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



###### 2. Package Management

| Command	                      | Alias	          |                     Description                         |      Common Flags                |
|:------------------------------|:---------------:|:--------------------------------------------------------|----------------------------------|
| npm list	                    | npm ls	        | Lists installed packages.	                              |--global, --depth, --json, --long |
| npm list -g                   | npm ls -g	      | Lists globally installed packages.	                    |--depth, --json, --long           |
| npm install --global <pkg>    |	npm i -g <pkg>	| Installs a package globally.	                          |--force, --no-save, --dry-run     |
| npm uninstall --global <pkg>  |	npm rm -g <pkg>	| Uninstalls a global package.	                          |--force, --dry-run                |
| npm prune		                  | -               | Removes extraneous packages not listed in package.json.	|--production                      |
| npm cache clean --force		    | -               | Clears npm’s cache.	                                    |--force, --global, --offline      |
| npm rebuild		                | -               | Rebuilds native addons of installed packages.	          |--global, --build-from-source     |



###### 3. Versioning & Publishing

| Command	                        | Alias	    | Description	                                                | Common Flags                            |
|:--------------------------------|:----------|:------------------------------------------------------------|:----------------------------------------|
| npm version <update>	          | -	        | Bumps the package version (patch, minor, major).	          | --force, --no-git-tag-version, --preid  |
| npm publish	                    | -	        | Publishes the package to the npm registry.	                | --tag, --access, --dry-run, --otp       |
| npm deprecate <pkg> <message>	  | -	        | Marks a package or version as deprecated.	                  | --otp                                   |
| npm unpublish <pkg>	            | -	        | Removes a package from the npm registry (within 72 hours).	| --force, --otp                          |
| npm login	                      | -	        | Authenticates a user with npm registry credentials.	        | --registry, --scope, --auth-type        |
| npm logout    	                | -	        | Logs out a user from the npm registry.	                    | --registry, --scope                     |


###### 4. Auditing & Security

| Command	                        | Alias	    | Description	                                                              | Common Flags                        |
|:--------------------------------|:----------|:--------------------------------------------------------------------------|:------------------------------------|
| npm audit           	          | -	        | Audits project for security vulnerabilities.                              | --json, --production, --audit-level |
| npm audit fix                   | -         | Automatically fixes security vulnerabilities.                             | --force, --only, --dry-run          |
| npm audit fix --force           | -         | Forces npm to fix vulnerabilities even if it results in breaking changes. | --only, --dry-run                   |
