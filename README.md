# Playwright Deno Starter

This is a Playwright starter project using Deno 2.

## Requirements

1. [Deno](https://deno.com/) >= 2.1.9

## Setup the application

1. Install Deno's dependencies
   ```
   deno install
   ```
2. Install Playwright's dependencies
   ```
   ./playwright.sh install-deps
   ```
3. Install Chromium browser
   ```
   ./playwright.sh install chromium
   ```

## Run the tests

1. Run the tests
   ```
   ./playwright.sh test --project=chromium
   ```
2. Show test report
   ```
   ./playwright.sh show-report
   ```

## Clean up files

```
./clean.sh
```

## Troubleshoot

1. `Error: Request to timed out after 30000ms` error while installing Chromium browser
   1. Go to `./node_modules/.deno/playwright-core@1.50.0/node_modules/playwright-core/lib/utils/network.js` file
   2. Modify timeout value in `const NET_DEFAULT_TIMEOUT = exports.NET_DEFAULT_TIMEOUT = 30_000;` line
