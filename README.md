# commitlint ES Module Bug Reproduction
Reproduction of conventional-changelog/commitlint bug with ES modules.

**Steps to reproduce**
1) Clone and install this repository
2) Create some file, add to git, and commit the change
3) Observe the following error:

```
(node:27380) Warning: require() of ES modules is not supported.
require() of [FULL PATH REDACTED]/commitlint-esm-bug-repro/commitlint.config.js from
[FULL PATH REDACTED]/commitlint-esm-bug-repro/node_modules/cosmiconfig/node_modules/import-fresh/index.js
is an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which
defines all .js files in that package scope as ES modules.
Instead rename commitlint.config.js to end in .cjs, change the requiring code to use import(), or remove
"type": "module" from [FULL PATH REDACTED]/commitlint-esm-bug-repro/package.json.
```
