# Multi-project setup for Ionic apps with root `package.json` and common `node_modules`

- Root `package.json`, `tsconfig.json`, etc. to manage common settings & dependencies
- Works correctly with JetBrains IDEs *(WebStorm, IDEA, PyCharm, GoLand, etc.)*
- Project level `package.json` to overrider/add project specific settings & dependencies

## Purpose & benefits of multi-project workspace

- Consistent configuration across multiple projects

- Quick refactoring across multiple projects
  <br>
  *(e.g. renaming method in library with instant refactoring of all dependent projects)*

- Quicker to pull & setup due to single `node_modules` so you don't need to install same packages multiple times

- Quicker & easy to update common dependencies

## Top level structure

    📁 node_modules
    📂 projects
      📂 apps
        📂 ang1 (angular app)
           ...
        📂 ionic1 (first Ionic app)
           📄 package.json
           ...
        📂 ionic2 (second Ionic app)
           📄 package.json
           ...
      📂 libs
         📂 lib1
           📄 package.json
           ...
         📂 lib2
           📄 package.json
           ...
    📄 angular.json
    📄 ionic.config.json
    📄 package.json
    📄 tsconfig.json
    📄 tslint.json

## Credits & references

- Initial idea for this setup is taken from this article:
  https://devdactic.com/ionic-multi-app-shared-library/

- Ionic documentation
  https://beta.ionicframework.com/docs/cli/configuration#multi-app-projects

- Angular multiple projects workspace 
  https://angular.io/guide/file-structure#multiple-projects
