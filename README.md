# Jest Selenium BrowserStack 

1. `cd jest-selenium-browserstack`
2. Replace `YOUR_BROWSERSTACK_USERNAME` with BrowserStack username and `YOUR_BROWSERSTACK_KEY` with BrowserStack key in files inside `test/` directory
3. Run selected tests (see scripts section below) and/or modify source

## Scripts

### Local tests

Run Jest Selenium tests locally with:

```bash
yarn test:local
```

### Manual tests

Connect with BrowserStack manually:

```bash
~/.browserstack/BrowserStackLocal --key [YOUR_BROWSERSTACK_KEY] --folder $(pwd)
```

and then run tests with:

```bash
yarn test:manual
```

### Automate tests

Just execute:

```bash
yarn test:automate
```

And see tests automatically connecting and running on BrowserStack.

### Parametrized tests

To run tests against browser and OS specified as command execution arguments use:

```bash
BROWSER=chrome OS=Windows yarn test:parametrized
```

### Sequential tests

Here is how you may run tests for multiple browsers in one call,
adjust configuration in `./test/config.json` and run:

```bash
yarn test:sequential
```

### Other scripts available

```bash
yarn build
```

For building tested code from `src/` directory.

```bash
yarn clean
```

To remove `lib/` directory generated with `build` script.

```bash
yarn lint
```

Runs Eslint on files inside `src/` directory.

---

