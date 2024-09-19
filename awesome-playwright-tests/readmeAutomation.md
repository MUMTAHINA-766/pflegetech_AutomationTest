
Creating a new Playwright project
If you haven't already done so as part of tutorial preparations, let's create a new test project. Create a new directory:

mkdir awesome-playwright-tests
cd awesome-playwright-tests
Then, initialize Playwright:

npm init playwright@latest
The init command will ask a series of prompts. Accept the default answers for the questions:

Select TypeScript for the project language.
Select tests as the test directory.
Say false to adding a GitHub Actions workflow.
Say true to installing Playwright browsers.
This command will create a bunch of new project files, including:

A package.json file with the Playwright package dependency
A playwright.config.ts file with test configurations
A tests directory with basic example tests
A tests-examples directory with more extensive example tests
The command will also install the Playwright browser projects: Chromium, Firefox, and WebKit. Beware that browser installation may take several minutes if your Internet connection is slow.

Note: This tutorial was developed with Playwright 1.36.1. Things might change in future versions.

Note: If you are setting up an existing project that has Playwright as a dependency, then you will need to run npm install and then npx playwright install to install Playwright properly.
