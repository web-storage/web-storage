<a href="https://github.com/w3cwebstorage/w3cwebstorage" target="__blank"><img alt="w3cwebstorage" src="https://raw.githubusercontent.com/w3cwebstorage/w3cwebstorage/master/logo.png" width="100" /></a>

# w3cwebstorage - localstorage

## Usage

### Message options

| Property | Description                                                                                                                                                       |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`   | Indicates the type of operation to be performed (Required)                                                                                                        |
| `key`    | String value indicating the identifier of the value in the storage to be manipulated.                                                                             |
| `value`  | Represents the value that is stored in the storage. Supports all data types (int, objects, boolean) but they must be serialized to a string value before storage. |

#### Example usage

##### Get a value from local storage

```js
import { localStorageReducer } from "@w3cwebstorage/w3cwebstorage";

const value = localStorageReducer(window.localStorage, {
  type: "get",
  key: "key"
});
```

##### Set a value to local storage

```js
import { localStorageReducer } from "@w3cwebstorage/w3cwebstorage";

localStorageReducer(window.localStorage, {
  type: "set",
  key: "key",
  value: "value"
});
```

##### Remove a value from local storage

```js
import { localStorageReducer } from "@w3cwebstorage/w3cwebstorage";

const value = localStorageReducer(window.localStorage, {
  type: "remove",
  key: "key"
});
```

##### Clear all values in local storage

```js
import { localStorageReducer } from "@w3cwebstorage/w3cwebstorage";

const value = localstorage(window.localStorage, {
  type: "clear"
});
```