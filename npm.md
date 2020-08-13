---
title: npm
category: JavaScript
layout: 2020/sheet
created: 2020-08-01
---

### Package management

| Command                           | Description                                               |
| ---                               | ---                                                       |
| `npm i`                           | Alias for `npm install`                                   |
| `npm install`                     | Install everything in package.json                        |
| `npm install --production`        | Install everything in package.json, except devDependecies |
| ---                               | ---                                                       |  
| `npm install lodash`              | Install a package                                         |
| `npm install --save-dev lodash`   | Install as devDependency                                  |
| `npm install --save-exact lodash` | Install with exact                                        |


`--save` is the default as of npm@5. Previously, using `npm install` without `--save` doesn't update package.json.

### Install names

| Command                              | Description             |
| ---                                  | ---                     |
| `npm i axios`                        | NPM package             |
| `npm i axios@latest`                 | Specify tag `latest`    |
| `npm i axios@0.19.2`                 | Specify version `0.19.2`|
| `npm i axios@">=0.16.2 <0.19.2"`     | Specify version range   |                   |
| `npm i user/repo`                    | GitHub                  |
| `npm i user/repo#master`             | GitHub                  |
| `npm i github:user/repo`             | GitHub                  |
| `npm i gitlab:user/repo`             | GitLab                  |
| ---                                  | ---                     |
| `npm i /path/to/repo`                | Absolute path           |


### Listing

| Command                 | Description                                                         |
| ---                     | ---                                                                 |
| `npm list` or `npm ls`  | Lists the installed versions of all dependencies in this software   | 
| `npm list -g --depth 0` | Lists the installed versions of all globally installed packages     | 
| `npm view`              | Lists the latest versions of all dependencies in this software      | 
| `npm outdated`          | Lists only the dependencies in this software which are outdated     |

### Updating

| Command             | Description                |
| ---                 | ---                        |
| `npm update`        | Update production packages |
| `npm update --dev`  | Update dev packages        |
| `npm update -g`     | Update global packages     |
| ---                 | ---                        |
| `npm update lodash` | Update a package           |


### Misc features

```bash
# Update npm 
npm install npm@latest -g
```

```bash
# Add someone as an owner
npm owner add USERNAME PACKAGENAME
```

```bash
# remove packages installed globally
npm rm -g <package_name>
```

```bash
# Adds warning to those that install a package of old versions
npm deprecate PACKAGE@"< 0.3.0" "critical bug fixed in v0.3.0"
```

```bash
# update all packages, or selected packages
npm update [-g] PACKAGE
```

```bash
# Check for outdated packages
npm outdated [PACKAGE]
```