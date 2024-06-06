# Config

The `Config` class in the `Framework\Support\Helpers` namespace provides a static interface to configuration operations using the `ConfigRepository`.

## Methods

### All
`all(): array`

Retrieves the entire configuration array.

- **Returns**: 
    - `array` - The array of configuration values.

### Set
`set(array $keys): void`

Sets multiple configuration values at runtime.

- **Parameters**:
    - `array $keys` - An associative array of configuration keys and their values.
- **Returns**: 
    - `void` - Indicates that the configuration values have been set.

### Get
`get(string $key, $default = null): mixed`

Retrieves the value of a configuration key, with an option for a default value if the key does not exist.

- **Parameters**:
    - `string $key` - The configuration key.
    - `mixed $default` - The default value to return if the key does not exist.
- **Returns**: 
    - `mixed` - The value of the configuration key, or the default value if the key does not exist.

### Has
`has(string $key): bool`

Checks if a configuration key exists.

- **Parameters**:
    - `string $key` - The configuration key.
- **Returns**: 
    - `bool` - True if the configuration key exists, false otherwise.

