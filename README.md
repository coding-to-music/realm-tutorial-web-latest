# Realm Web and GraphQL Tutorial

Follow along at https://docs.mongodb.com/realm/tutorial/web-graphql/

# This repo was created using this command, using the final branch

```java
git clone git@github.com:mongodb-university/realm-tutorial-web.git
```

## Installation

```java
npm install
```

Output

```java
added 1977 packages, and audited 1978 packages in 23s

102 packages are looking for funding
  run `npm fund` for details

146 vulnerabilities (128 moderate, 17 high, 1 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
```

npm run start

```java
npm run start
```

Output

```java
> task-tracker@0.1.0 start
> react-scripts start


There might be a problem with the project dependency tree.
It is likely not a bug in Create React App, but something you need to fix locally.

The react-scripts package provided by Create React App requires a dependency:

  "eslint": "^6.6.0"

Don't try to install it manually: your package manager does it automatically.
However, a different version of eslint was detected higher up in the tree:

  /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint (version: 8.6.0)

Manually installing incompatible versions is known to cause hard-to-debug issues.

If you would prefer to ignore this check, add SKIP_PREFLIGHT_CHECK=true to an .env file in your project.
That will permanently disable this message but you might encounter other issues.

To fix the dependency tree, try following the steps below in the exact order:

  1. Delete package-lock.json (not package.json!) and/or yarn.lock in your project folder.
  2. Delete node_modules in your project folder.
  3. Remove "eslint" from dependencies and/or devDependencies in the package.json file in your project folder.
  4. Run npm install or yarn, depending on the package manager you use.

In most cases, this should be enough to fix the problem.
If this has not helped, there are a few other things you can try:

  5. If you used npm, install yarn (http://yarnpkg.com/) and repeat the above steps with it instead.
     This may help because npm has known issues with package hoisting which may get resolved in future versions.

  6. Check if /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint is outside your project directory.
     For example, you might have accidentally installed something in your home folder.

  7. Try running npm ls eslint in your project folder.
     This will tell you which other package (apart from the expected react-scripts) installed eslint.

If nothing else helps, add SKIP_PREFLIGHT_CHECK=true to an .env file in your project.
That would permanently disable this preflight check in case you want to proceed anyway.
```

Was still getting the above error so I added the following to a .env file

```java
SKIP_PREFLIGHT_CHECK=true
```

Run

```java
npm run start
```

Still getting warnings

```java
Compiled with warnings.

./src/index.js
Failed to load plugin 'flowtype' declared in 'BaseConfig » /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/react-scripts/node_modules/eslint-config-react-app/index.js': Package subpath './lib/rules/no-unused-expressions' is not defined by "exports" in /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint/package.json

./src/App.js
Failed to load plugin 'flowtype' declared in 'BaseConfig » /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/react-scripts/node_modules/eslint-config-react-app/index.js': Package subpath './lib/rules/no-unused-expressions' is not defined by "exports" in /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint/package.json

./src/serviceWorker.js
Failed to load plugin 'flowtype' declared in 'BaseConfig » /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/react-scripts/node_modules/eslint-config-react-app/index.js': Package subpath './lib/rules/no-unused-expressions' is not defined by "exports" in /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint/package.json

./src/TaskApp.js
Failed to load plugin 'flowtype' declared in 'BaseConfig » /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/react-scripts/node_modules/eslint-config-react-app/index.js': Package subpath './lib/rules/no-unused-expressions' is not defined by "exports" in /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint/package.json

./src/RealmApp.js
Failed to load plugin 'flowtype' declared in 'BaseConfig » /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/react-scripts/node_modules/eslint-config-react-app/index.js': Package subpath './lib/rules/no-unused-expressions' is not defined by "exports" in /mnt/volume_nyc1_01/realm-tutorial-web-latest/node_modules/eslint/package.json
```

The above errors may have gone away

This is visible on port 3000 although I can't log in or register a new account

![image](https://user-images.githubusercontent.com/3156358/151671206-a5531ebb-e68f-4bc7-8dbd-069c636a831c.png)

## Troubleshooting

- Be sure to **check the logs in Realm UI** for more information as well as the console in your app.
- Be sure to **deploy your changes** in the Realm UI.

## Issues & Pull Requests

If you find an issue or have a suggestion, please let us know using the feedback
widget on the [docs site](http://docs.mongodb.com/realm/tutorial).

This repo is automatically derived from our main docs repo. If you'd like to
submit a pull request -- thanks! -- please feel free to do so at
https://github.com/mongodb/docs-realm/ (see the tutorial/ subdirectory).
