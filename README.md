# Savvy-Plus-V1

This project is built according to the [MEAN](https://en.wikipedia.org/wiki/MEAN_\(software_bundle\)) full-stack.

Additional frameworks / libraries: [UI-Bootstrap](https://angular-ui.github.io/bootstrap/), [Auth0](https://auth0.com/).

Other tools: [TypeScript](http://www.typescriptlang.org/), [Gulp](http://gulpjs.com/).

## Getting Started

To get you started you can simply clone this repository and install the dependencies:

__Prerequisites:__ you need Node.js 4.2.x installed.

1. Clone / Download the repo. SourceTree is recommended to easily working with Git, you can download the SourceTree app from [here](https://www.sourcetreeapp.com/).
2. Install dependencies: ```npm install```
3. Launch Application: ```npm start```

__Other commands__
* Run tests: ```npm test```
* Run static analysis linter: ```gulp tslint``` 

**Tested on:** Node.js 4.2.x

## Contributing to Cymplar-App

As a developer, here are the guidelines we would like you to follow:

 - [Coding Rules](#rules)
 - [Issues and Bugs](#issue)
 - [Submission Guidelines](#submit-issue)
 
### <a name="rules"></a>Coding Rules
To ensure consistency throughout the source code, keep these rules in mind as you are working:

* We follow the JavaScript Style guides from [Airbnb](https://github.com/airbnb/javascript) and
  [Google](https://google.github.io/styleguide/javascriptguide.xml).
* We follow the Style guide for Angular from [John Papa](https://github.com/johnpapa/angular-styleguide).
* We follow the [LIFT Principle](https://github.com/johnpapa/angular-styleguide#application-structure-lift-principle) for Structuring our Application: "_Structure your app such that you can Locate your code quickly, Identify the code at a glance, keep the Flattest structure you can, and Try to stay DRY. The structure should follow these 4 basic guidelines._
  _Why LIFT?: Provides a consistent structure that scales well, is modular, and makes it easier to increase developer efficiency by finding code quickly. Another way to check your app structure is to ask yourself: How quickly can you open and work in all of the related files for a feature?_".
* All features or bug fixes **should be tested** by one or more specs (unit-tests).
* At last but not at least, we follow three principles: [KISS](https://en.wikipedia.org/wiki/KISS_principle), [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself), [SOLID](https://en.wikipedia.org/wiki/SOLID_\(object-oriented_design\)), 

#### Directory Layout

```
client/                 --> all of the source files for the front-end application
  bootstrap.ts            --> entry-point file for the front-end application
  index.html              --> app layout file (the main html template file of the app)
  index.scss              --> app style file (the main scss file of the app - use it for common styles)
  system.config.js        --> configuration for the module loader
  components/             --> all app specific modules
    contacts/               --> Sample module for the app with sub-routing
    navbar/                 --> main menu of the app
  core/                   --> Only transversal code goes here
    dto.ts                  --> DTOs or domain classes for the app
    util.ts                 --> Common utility classes for thr app
karma.conf.js           --> config file for running unit tests with Karma
```

#### Use a TypeScript-aware editor to view / edit the code.
* [Visual Studio Code](https://code.visualstudio.com/)
* [Atom](https://atom.io/) with [TypeScript plugin](https://atom.io/packages/atom-typescript)
* [Webstorm](https://www.jetbrains.com/webstorm/download/)
* [Sublime Text](http://www.sublimetext.com) with [Typescript plugin](https://github.com/Microsoft/Typescript-Sublime-plugin#installation)

### <a name="issue"></a>Found an Issue?
If you find a bug in the source code or a mistake in the documentation, you can help by
[submitting an issue](#submit-issue) to our [GitHub Repository][github]. Even better, you can
[submit a Pull Request](#submit-pr) with a fix.

### <a name="submit-issue"></a>Submitting an Issue
If your issue appears to be a bug, and hasn't been reported, open a new issue.
Providing the following information will increase the chances of your issue being dealt with quickly:

* **Overview of the Issue** - if an error is being thrown a non-minified stack trace helps
* **Motivation for or Use Case** - explain why this is a bug for you
* **Browsers and Operating System** - is this a problem with all browsers?
* **Related Issues** - has a similar issue been reported before?
* **Suggest a Fix** - if you can't fix the bug yourself, perhaps you can point to what might be
  causing the problem (line of code or commit).
  
### <a name="submit-pr"></a>Submitting a Pull Request (PR)
Before you submit your Pull Request (PR) consider the following guidelines:

* Search [GitHub](https://github.com/Neulinet/cymplar-app/pulls) for an open or closed PR
  that relates to your submission. You don't want to duplicate effort.
* Make your changes in a new git branch:

     ```shell
     git checkout -b my-fix-branch master
     ```

* Create your patch, **including appropriate test cases**.
* Follow our [Coding Rules](#rules).
* Run the full App test suite, as described in the [developer documentation][dev-doc],
  and ensure that all tests pass.
* Commit your changes using a descriptive commit message that follows our
  [commit message conventions](#commit). Adherence to these conventions
  is necessary because release notes are automatically generated from these messages.

     ```shell
     git commit -a
     ```
  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

* Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

* In GitHub, send a pull request to `cymplar-app:develop`.
* If we suggest changes then:
  * Make the required updates.
  * Re-run the test suites to ensure tests are still passing.
  * Rebase your branch and force push to your GitHub repository (this will update your Pull Request):
    ```shell
    git rebase master -i
    git push -f
    ```

That's it! Thank you for your contribution!

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the develop branch:

    ```shell
    git checkout develop -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your develop with the latest upstream version:

    ```shell
    git pull --ff upstream develop
    ```
