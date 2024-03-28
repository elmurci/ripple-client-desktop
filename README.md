# Desktop Client

## Install Dependencies

- Fork and clone the ripple-client-desktop repository 
- Run `npm install`
- Download [nw.js](https://github.com/nwjs/npm-installer)

## Build

- In the ripple-client-desktop repository, make a copy of the `config_example.js` file and name it `config.js`
- Run `gulp` in your command line for development

- Run `gulp packages` in your command line for the production ready client
- Your desktop client is in the `packages/RippleAdminConsole` directory

### Note
- There are breaking changes in the c++ API when using node version 4. You should use node version 0.12.
- The current package.json is intended to pull directly from the develop branch of ripple-lib. You may need to clone the ripple-lib respository into node_modules/ripple-lib and then run npm install in the cloned ripple-lib repository.
- In order to fix an issue in `ripple-lib` caused by `rippled` not returning the `fee_ref` field in the ledger subscription stream when the amendment `XRPFees` is active, we need to [patch](patches) `ripple-lib`.
This can be done with the help of the `patch-package` library (executed post-install).
