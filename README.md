# angular-playground
angular 


### Angular CLI commands:


```bash
>ng help
Available Commands:
add:  Adds support for an external library to your project.
analytics Configures the gathering of Angular CLI usage metrics. See https://angular.io/cli/usage-analytics-gathering.
build (b): Compiles an Angular app into an output directory named dist/ at the given output path. Must be executed from within a workspace directory.
deploy: Invokes the deploy builder for a specified project or for the default project in the workspace.
config: Retrieves or sets Angular configuration values in the angular.json file for the workspace.
doc (d): Opens the official Angular documentation (angular.io) in a browser, and searches for a given keyword.
e2e (e): Builds and serves an Angular app, then runs end-to-end tests using Protractor.
extract-i18n (i18n-extract, xi18n): Extracts i18n messages from source code.
generate: (g) Generates and/or modifies files based on a schematic.
help: Lists available commands and their short descriptions.
lint (l): Runs linting tools on Angular app code in a given project folder.
new (n): Creates a new workspace and an initial Angular application.
run: Runs an Architect target with an optional custom builder configuration defined in your project.
serve (s): Builds and serves your app, rebuilding on file changes.
test (t): Runs unit tests in a project.
update: Updates your application and its dependencies. See https://update.angular.io/
version (v): Outputs Angular CLI version.
```

##### Install Angular CLI:
```bash
npm install -g @angular/cli
```


##### Create new project:

```bash
ng new angular-project-name
```


##### Install a package:
```bash
ng add @angular/material
```
or
```bash
npm install @angular/material
```

###### ng add vs npm install:

*npm install* will only install the package.

*ng add* will not only install the package, but also bring configurations in angular.json and other files for some packages. It doesn't bring modifications all the time, because some packages don't need to be configured. 

You can compare the installation process between 
*ng add @angular/material* vs *npm install @angular/material*
*ng add @angular/pwa* vs *npm install @angular/pwa* 


When you need to uninstall a package, you can only use *npm uninstall*, because there is not ng command for uninstallation. You need to revert the modifications made in angular.json and other files manually when you use *ng add* in the installation.


##### Analytics

```bash
ng analytics
```

##### Get or set configurations in angular.json 

```bash
ng config
```

##### Update Angular version

```bash
>ng update
The installed local Angular CLI version is older than the latest stable version.
Installing a temporary version to perform the update.
Installing packages for tooling via npm.
Installed packages for tooling via npm.
Using package manager: 'npm'
Collecting installed dependencies...
Found 32 dependencies.
    We analyzed your package.json, there are some packages to update:

      Name                               Version                  Command to update
     --------------------------------------------------------------------------------
      @angular/cdk                       10.2.7 -> 11.0.1         ng update @angular/cdk
      @angular/cli                       10.2.0 -> 11.0.2         ng update @angular/cli
      @angular/core                      10.2.3 -> 11.0.2         ng update @angular/core
      @angular/material                  10.2.7 -> 11.0.1         ng update @angular/material
```

To update project's angular vesion:
```bash
>ng update @angular/core @angular/cli
```

You can check : https://update.angular.io/ to see how to upgrade your angular project.

##### Generate component, service etc

```bash
>ng generate --help
Shows a help message for this command in the console.
--interactive
When false, disables interactive input prompts.

Available Schematics:
  Collection "@schematics/angular" (default):
    appShell
    application
    class
    component
    directive
    enum
    guard
    interceptor
    interface
    library
    module
    pipe
    resolver
    service
    serviceWorker
    webWorker
```

##### Build angular project

```bash
ng build
```

##### Build and server angular project

```bash
ng serve
```

##### Linting

```bash
ng lint
```

##### Test

```bash
ng test
```

##### End to end test

```bash
ng e2e
```


#### What is tsconfig.json?

tsconfig.json: TypeScript compiler configuration

#### What is PWA?

PWA (Progressive Web App)

#### What is Polyfill?

A polyfill is a piece of code (usually JavaScript on the Web) used to provide modern functionality on older browsers that do not natively support it.

For example, a polyfill could be used to mimic the functionality of a text-shadow in IE7 using proprietary IE filters, or mimic rem units or media queries by using JavaScript to dynamically adjust the styling as appropriate, or whatever else you require.

The reason why polyfills are not used exclusively is for better functionality and better performance. Native implementations of APIs can do more and are faster than polyfills. For example, the Object.create polyfill only contains the functionalities that are possible in a non-native implementation of Object.create.

Other times, polyfills are used to address issues where browsers implement the same features in different ways. The polyfill uses non-standard features in a certain browser to give JavaScript a standards-compliant way to access the feature. Although this reason for polyfilling is very rare today, it was especially prevalent back in the days of IE6 and Netscape where each browser implemented JavaScript very differently. The 1st version of JQuery was an early example of a polyfill. It was essentially a compilation of browser-specific workarounds to provide JavaScript developers with a single common API that worked in all browsers. At the time, JavaScript developers were having major problems trying to get their website to work across all devices because there was such a discrepancy between browsers that the website might have to be programmed radically differently and have a much different user interface based upon the user's browser. Thus, the JavaScript developer had access to only a very tiny handful of JavaScript APIs that worked more-or-less consistently across all browsers. Using a polyfill to handle browser-specific implementations is less common today because modern browsers mostly implement a broad set of APIs according to standard semantics.

