# Web Store
The frontend for Phoenix/Brackets web store.

## Code Guardian
[![<app> build verification](https://github.com/aicore/web-store/actions/workflows/build_verify.yml/badge.svg)](https://github.com/aicore/web-store/actions/workflows/build_verify.yml)

<a href="https://sonarcloud.io/summary/new_code?id=aicore_web-store">
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=alert_status" alt="Sonar code quality check" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=security_rating" alt="Security rating" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=vulnerabilities" alt="vulnerabilities" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=coverage" alt="Code Coverage" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=bugs" alt="Code Bugs" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=reliability_rating" alt="Reliability Rating" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=sqale_rating" alt="Maintainability Rating" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=ncloc" alt="Lines of Code" />
  <img src="https://sonarcloud.io/api/project_badges/measure?project=aicore_web-store&metric=sqale_index" alt="Technical debt" />
</a>

# Commands available

## Building
Since this is a pure JS template project, build command just runs test with coverage.
```shell
> npm install   // do this only once.
> npm run build
```

## Linting
To lint the files in the project, run the following command:
```shell
> npm run lint
```
To Automatically fix lint errors:
```shell
> npm run lint:fix
```

# Dependency updates
  We use Rennovate for dependency updates: https://blog.logrocket.com/renovate-dependency-updates-on-steroids/
  * By default, dep updates happen on sunday every week.
  * The status of dependency updates can be viewed here if you have this repo permissions in github: https://app.renovatebot.com/dashboard#github/aicore/template-nodejs
  * To edit rennovate options, edit the rennovate.json file in root, see https://docs.renovatebot.com/configuration-options/
  Refer 
  
# Code Guardian
Several automated workflows that check code integrity are integrated into this template.
These include:
1. GitHub actions that runs build/test/coverage flows when a contributor raises a pull request
2. [Sonar cloud](https://sonarcloud.io/) integration using `.sonarcloud.properties`
   1. In sonar cloud, enable Automatic analysis from `Administration
      Analysis Method` for the first time ![image](https://user-images.githubusercontent.com/5336369/148695840-65585d04-5e59-450b-8794-54ca3c62b9fe.png)

## IDE setup
SonarLint is currently available as a free plugin for jetbrains, eclipse, vscode and visual studio IDEs.
Use sonarLint plugin for webstorm or any of the available
IDEs from this link before raising a pull request: https://www.sonarlint.org/ .

SonarLint static code analysis checker is not yet available as a Brackets
extension.

## Internals
### Testing framework: Mocha , assertion style: chai
 See https://mochajs.org/#getting-started on how to write tests
 Use chai for BDD style assertions (expect, should etc..). See move here: https://www.chaijs.com/guide/styles/#expect

### Mocks and spies: sinon
 if you want to mock/spy on fn() for unit tests, use sinon. refer docs: https://sinonjs.org/

### Note on coverage suite used here:
we use c8 for coverage https://github.com/bcoe/c8. Its reporting is based on nyc, so detailed docs can be found
 here: https://github.com/istanbuljs/nyc ; We didn't use nyc as it do not yet have ES module support
 see: https://github.com/digitalbazaar/bedrock-test/issues/16 . c8 is drop replacement for nyc coverage reporting tool
