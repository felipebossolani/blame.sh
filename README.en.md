<p align="center">
  <img src="logo.png" alt="blame.sh" width="120">
</p>

<h1 align="center">blame.sh</h1>

<p align="center">An excuse generator for devs who need to explain the unexplainable.</p>

<p align="center"><a href="README.md">Versao em Portugues</a></p>

## About

**blame.sh** is an excuse generator for developers. Pick who's asking, pick what broke, and get three excuses in different tones: technical, vague, and dramatic.

The project started as a joke, but with the kind of structure every dev respects: no frameworks, no dependencies, no excuses (ironically).

## How it works

1. Pick the **persona** (who's listening: tech lead, PM, client...)
2. Pick the **situation** (what happened: deploy broke, bug in production, giant PR...)
3. Click `./blame.sh` and get three excuses, each in a different tone

All excuses are pre-written in JSON and served without any API calls. Everything runs in the browser.

## Stack

Vanilla HTML, CSS, and JavaScript. A single page, zero external dependencies (besides the JetBrains Mono font via Google Fonts). Works in any modern browser.

## Running locally

Open the `index.html` file in your browser. No build, bundler, or server required.

## Author

Built by [Felipe Bossolani](https://github.com/felipebossolani).
