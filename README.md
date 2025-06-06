# WebSearch Selenium Plugin

Add-on for the Web Search extension that provides the web browsing capabilities without the need for Extras API.

## How to install

> This plugin will not work in Termux or any ARM64 Linux (Raspberry Pi, etc). See [this issue](https://github.com/SillyTavern/SillyTavern-WebSearch-Selenium/issues/1).

1. Before you begin, make sure you set a config `enableServerPlugins` to `true` in the config.yaml file of SillyTavern.

2. Open a terminal in your SillyTavern directory, then run the following:

```bash
cd plugins
git clone https://github.com/SillyTavern/SillyTavern-WebSearch-Selenium
```

3. Restart the SillyTavern server. Then choose "Selenium Plugin" as a source in the Web Search extension UI.

## Configuration

The plugin can be configured using [environment variables](https://dev.to/pizofreude/environment-variables-a-comprehensive-guide-34dg) before startup:

### Choose a preferred browser

`SILLYTAVERN_SELENIUM_BROWSER` (string) - sets the browser to be used. Default: `chrome`.

Possible values (case-sensitive!):

* `chrome`
* `firefox`
* `safari`
* `MicrosoftEdge`

A chosen browser must be available and installed on your machine.

### Run in headless mode

* `SILLYTAVERN_SELENIUM_HEADLESS` (boolean) - launches browser in the headless (no visible GUI) mode. Default: `true`.

### Save debug pages

* `SILLYTAVERN_SELENIUM_DEBUG` (boolean) - save the HTML of search result pages to a temp directory. Default: `false`.

## How to build

Clone the repository, then run `npm install`.

```bash
# Debug build
npm run build:dev
# Prod build
npm run build
```

## License

AGPLv3

### Note

This repository redistributes the official Selenium Manager binaries, which are under an Apache-2.0 license.

You can find them here: [selenium_manager_artifacts](https://github.com/SeleniumHQ/selenium_manager_artifacts)
