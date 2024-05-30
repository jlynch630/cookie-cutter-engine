<!--
 Copyright 2024 John Lynch. All rights reserved.
 Use of this source code is governed by a BSD-style license that can be
 found in the LICENSE file.
-->

# Cookie Cutter Engine

This engine powers automatically answering GDPR, CCPA, and related cookie notices on the web according to user preferences by means of a Web Extension.

## Structure

This repository is split up into two parts:

-   `./engine`: The engine, which handles detecting and handling cookie notices.
-   `./testExtension`: A test Chrome extension which can be used to test changes made to the engine during development.

## Contributing

If you'd like to contribute, great! Please take a look at the [contributor guidelines](./CONTRIBUTING.md) first.

## Building

The engine uses a standard NPM package.json. To build the code, first install the project:

```bash
$ yarn install
```

Then you can create a production build with:

```bash
$ yarn build
```

Or make a dev build and watch for changes with:

```bash
$ yarn watch
```

## Testing

To test the engine, you can make use of the test extension in `./testExtension`. It will automatically build and load the engine.

To install the test extension in Chrome, first build it:

```bash
cookie-engine/testExtension $ yarn install
cookie-engine/testExtension $ yarn build # or `yarn watch`
```

Then, in Chrome:

1. Navigate to `chrome://extensions`
2. Enable the Developer Mode toggle in the top right corner
3. Click "Load unpacked"
4. Navigate to the extension build directory `cookie-engine/testExtension/crx`
