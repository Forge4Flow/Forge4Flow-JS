# Warrant ES Module

Use [Warrant](https://warrant.dev/) as an ES module.

## Installation

Use `npm` to install the Warrant module:

```sh
npm install @warrantdev/warrant-js
```

## Usage
Import the Warrant client and pass your API key to the constructor to get started:
```js
import {Client as WarrantClient} from "@warrantdev/warrant-js";

const warrant = new WarrantClient('prod_f5dsKVeYnVSLHGje44zAygqgqXiLJBICbFzCiAg1E=');
```

### `isAuthorized(userUUID, permissionName)`

This function returns a `Promise` that resolves with `true` if the user with the specified `userUUID` has been granted the permission with the specified `permissionName` and `false` otherwise.

```js
import {Client as WarrantClient} from "@warrantdev/warrant-js";

const warrant = new WarrantClient('prod_f5dsKVeYnVSLHGje44zAygqgqXiLJBICbFzCiAg1E=');

//
// Example Scenario:
// An e-commerce website where Store Owners can edit their own Store's info
//
if (warrant.isAuthorized(userSession.userId, "edit_stores")) {
    // Carry out logic to allow user to edit a Store
}
```

We’ve used a random API key in these code examples. Replace it with your
[actual publishable API keys](https://app.warrant.dev) to
test this code through your own Warrant account.

For more information on how to use the Warrant API, please refer to the
[Warrant API reference](https://docs.warrant.dev).

## TypeScript support

This package includes TypeScript declarations for Warrant.

Note that we may release new [minor and patch](https://semver.org/) versions of
`@warrantdev/warrant-js` with small but backwards-incompatible fixes to the type
declarations. These changes will not affect Warrant itself.

## Warrant Documentation

- [Warrant Docs](https://docs.warrant.dev/)