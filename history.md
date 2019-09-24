# My Progress with the tutorial

Ideally to build this app before rewriting angularJS

## resources

- commit [history](https://github.com/EmbraceLife/angular-phonecat/commits/master)
- online tutorial [page](https://docs.angularjs.org/tutorial)

## Setup

- fork https://github.com/angular/angular-phonecat.git
- git clone --depth=16 https://github.com/EmbraceLife/angular-phonecat.git
- git remote add upstream https://github.com/angular/angular-phonecat.git
- simply run `npm install`, but having too many errors
- keep reading to install properly

**Notice**

The chrome launcher installation caused many error, I removed it from the package.json file and reinstalled the latest version. Meanwhile, I did the same to firefox-launcher although it didn't cause any problem.

```json
"karma-chrome-launcher": "^2.2.0",
"karma-firefox-launcher": "^1.1.0",
```

run `npm install --save-dev karma-chrome-launcher karma-firefox-launcher` and then the latest version I installed are:

```json
"karma-chrome-launcher": "^3.1.0",
"karma-firefox-launcher": "^1.2.0"
```

## run scripts

### key components installed 

- Http-Server - simple local static web server
- Karma - unit test runner
- Protractor - end-to-end (E2E) test runner

### scripts needed during development

- `npm start`: Start a local development web server.(OK)
- `npm test`: Start the Karma unit test runner. (OK)
- `npm run protractor`: Run the Protractor end-to-end (E2E) tests (can't find angular on localhost page at the moment) 
- `npm run update-webdriver`: Install the drivers needed by Protractor (OK)

### `npm start`

**Why running with a web server**?

- Most browsers don't allow JS to make server request directly, with a server, it is allowed(?).

**How to change web address and port number**?

- To serve the web app on a different IP address or port, edit the "start" script within package.json. 
- You can use -a to set the address and -p to set the port. 
- You also need to update the baseUrl configuration property in e2e-test/protractor.conf.js.

### `npm test`

App code and test code are located together side by side.

**what does `npm test` do?**

- Open up instances of the Chrome and Firefox browsers and connect them to Karma.
- Execute all the unit tests in these browsers.
- Report the results of these tests in the terminal/command line window.
- Watch all the project's JavaScript files and re-run the tests whenever any of these change.

**`npm test` issues**

- run with success
- jasmine needs update, as 'Setting specFilter directly on Env' in the future version, and recommend to use `specFilter` in `configure` (problem to be dealt later)

### Running E2E Tests

**why?**

- We use E2E (end-to-end) tests to ensure that the application as a whole operates as expected.
- E2E tests are designed to *test the whole client-side application*, in particular that the *views are displaying and behaving correctly*. 
- It does this by **simulating real user interaction with the real application running in the browser**.

**Protractor?**

- The angular-phonecat project is configured to use Protractor to run the E2E tests for the application.
- Protractor relies upon a set of drivers to allow it to interact with the browser. 
- You can install these drivers by running `npm run update-webdriver`
- You don't have to manually run this command. Our npm scripts are configured so that it will be automatically executed as part of the command that runs the E2E tests.

**How?**

- `npm start` in one terminal window
- in another terminal window: `npm run protractor`

**What does protractor do?**

Protractor will read the configuration file at e2e-tests/protractor.conf.js. This configuration file tells Protractor to:

- Open up a Chrome browser and connect it to the application.
- Execute all the E2E tests in this browser.
- Report the results of these tests in the terminal/command line window.
- Close the browser and exit.

It is good to *run the E2E tests whenever you make changes to the HTML views or want to check that the application as a whole is executing correctly*.

It is very common to *run E2E tests before pushing a new commit of changes to a remote repository*.

### update dependencies

- `npm run update-deps` works with "some-package": "1.2.x" alike
- to go beyond the specified range, just change the range to "1.3.x" for example, and run `npm run update-deps`


### solutions to common issues 

go to the final section of this [page](https://docs.angularjs.org/tutorial)