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

| Command	            | Alias	         |                                                Description                                            |
|:-----------------   |:--------------:|:------------------------------------------------------------------------------------------------------|
| npm install	        | npm i	         | Installs all dependencies listed in package.json.	--save, --save-dev, --no-save, --global, --force   |
| npm install <pkg>	  | npm i <pkg>	   | Installs a specific package locally to the project.	--save, --save-dev, --global, --no-save, --force |
| npm uninstall <pkg>	| npm rm <pkg>	 | Uninstalls a specific package from the project.	--save, --global, --force, --dry-run                 |
| npm update	        | -	             | Updates all packages to the latest version.	--global, --force, --dry-run, --depth                    |
| npm outdated	      | -	             | Lists outdated packages in the project.	--global, --depth, --json, --long                            |
| npm run <script>	  | -	             | Runs a script defined in package.json.	--if-present, --verbose, --silent                              |
| npm start	          | -	             | Runs the start script defined in package.json.	--silent                                               |
| npm test	          | -	             | Runs the test script defined in package.json.	--silent, --verbose                                    |
| npm init	          | -	             | Initializes a new package.json file interactively.	--force, --scope, --yes                            |
| npm init -y	        | -	             | Creates package.json with default values.	--scope, --yes                                             |
| npm link	          | -	             | Links a global package to the current local project.	--global                                         |



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


###### 4. Configuration & Information

| Command	                        | Alias	    | Description	                                                              | Common Flags                        |
|:--------------------------------|:----------|:--------------------------------------------------------------------------|:------------------------------------|
| npm config set <key> <value>	  | -	        | Sets an npm configuration option.	                                        | --global, --location                |
| npm config get <key>	          | -	        | Gets an npm configuration option.	                                        | --global, --location                |
| npm config list	                | -	        | Lists all npm configuration options.	                                    | --json, --global                    |
| npm info <pkg>	                | -	        | Displays metadata and information about a package.	                      | --json, --registry, --silent        |
| npm view <pkg>	                | -	        | Another command for displaying package metadata, similar to npm info.	    | --json, --registry, --silent        |


###### 6. Help & Troubleshooting

| Command	                        | Alias	    | Description	                                                              | Common Flags                        |
|:--------------------------------|:----------|:--------------------------------------------------------------------------|:------------------------------------|
| npm help                        | -         | Displays help information about npm or a specific command.	              | --json, --long, --silent            |
| npm help <cmd>	                | -   	    | Displays help information for a specific npm command.                     | --json, --silent                    |
| npm doctor	                    | -       	| Checks the environment for common issues with npm.	                      | --json, --silent                    |
| npm dedupe	                    | -	        | Dedupe dependencies by optimizing the package tree.	                      | --global, --production, --dry-run   |

###### 7. Flags Overview

| Command	                        | Description	                                                                         | 
|:--------------------------------|:-------------------------------------------------------------------------------------|
| --save	                        | Adds the package to dependencies in package.json (default in npm 5+).                |
| --save-dev	                    | Adds the package to devDependencies in package.json.                                 |
| --save-optional	                | Adds the package to optionalDependencies in package.json.                            |
| --global or -g	                | Installs or manages packages globally.                                               |
| --no-save	                      | Installs the package without adding it to package.json.                              |
| --force or -f	                  | Forces npm to proceed with an action, ignoring potential conflicts.                  |
| --dry-run	                      | Tests the command without actually making any changes.                               |
| --production	                  | Only installs dependencies, excluding devDependencies.                               |
| --silent	                      | Suppresses all output except errors.                                                 |
| --verbose	                      | Provides more detailed output for debugging purposes.                                |
| --depth=<number>	              | Limits the depth of package trees when listing or updating.                          |
| --json	                        | Outputs results in JSON format.                                                      |
| --otp	                          | Provides a one-time password for 2FA actions (publishing, deprecating).              |
| --registry=<url>	              | Specifies the npm registry to use.                                                   |
| --tag=<tag>	                    | Publishes a package under a specific tag (e.g., beta, next).                         |
| `--access=<public	              | restricted>`                                                                         |
| --audit-level=<level>           |	Sets minimum vulnerability level for audit failures (low, moderate, high, critical). |



[ ] https://chatgpt.com/share/67bd6177-4720-800c-9b42-2a301460c181