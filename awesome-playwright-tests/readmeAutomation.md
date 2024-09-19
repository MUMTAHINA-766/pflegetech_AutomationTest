
# Creating a new Playwright project

### let's create a new test project.  

## Create a new directory:

```mkdir awesome-playwright-tests```

```cd awesome-playwright-tests```

Then, initialize Playwright:

```npm init playwright@latest```

### The init command will ask a series of prompts. Accept the default answers for the questions:

* Select TypeScript for the project language.
* Select tests as the test directory.
* Say false to adding a GitHub Actions workflow.
* Say true to installing Playwright browsers.

This command will create a bunch of new project files, including:

A ```package.json``` file with the Playwright package dependency
A ```playwright.config.ts``` file with test configurations
A ```tests``` directory with basic example tests
A ```tests-examples``` directory with more extensive example tests

The command will also install the Playwright browser projects: Chromium, Firefox, and WebKit. Beware that browser installation may take several minutes if your Internet connection is slow.

Note: If you are setting up an existing project that has Playwright as a dependency, then you will need to run npm install and then npx playwright install to install Playwright properly.

## Running the tests from the command line

Running tests from UI mode is helpful when developing the app and the tests, but it's not ideal for running tests in a Continuous Integration (CI) system. You can run tests directly from the command line like this:

```npx playwright test```

Tests will take a few seconds to run. Results should look something like this:

Running 78 tests using 4 workers
  78 passed (15.0s)

## To open last HTML report run:

```npx playwright show-report```

This opens the report in a browser. You can filter tests and click on results to view deeper trace. Each results also bears a label for the browser it targeted.

Playwright will automatically run tests in parallel across multiple workers. (You can explicitly set the number of workers it uses as well.) If you look carefully at the console output while tests are running, you will also see that Playwright will automatically run all tests across the three browser projects: Chromium, Firefox, and WebKit.

If you want to run tests against only one browser instead of all browsers, add the --project argument with the name of the browser. For example, to run tests against Chromium only, run:

```npx playwright test --project chromium```

For example:

```npx playwright test tests/example.spec.ts --workers 1 --project chromium```
