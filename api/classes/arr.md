# Arr

The `Arr` class in the `Framework\Support` namespace provides utility methods for array manipulation.

## Methods

### First
`first(array $array, ?callable $callback = null, $default = null): mixed`

Filters the array using the given callback and returns the first result. If no callback is provided, it returns the first element or the default value if the array is empty.

- **Parameters**:
    - `array $array` - The array to filter.
    - `callable|null $callback` - The callback function to filter the array.
    - `mixed $default` - The default value if no matching element is found.
- **Returns**:
    - `mixed` - The first matching element or the default value.

### Where
`where(array $array, callable $callback): array`

Filters the array using the specified callback function.

- **Parameters**:
    - `array $array` - The array to filter.
    - `callable $callback` - The callback function to filter the array.
- **Returns**:
    - `array` - The filtered array.

### Get
`get(array $array, string $key, $default = null): mixed`

Retrieves an item from an array using 'dot' notation. If the key does not exist, the default value is returned.

- **Parameters**:
    - `array $array` - The array from which to retrieve the item.
    - `string $key` - The key in dot notation.
    - `mixed $default` - The default value to return if the key is not found.
- **Returns**:
    - `mixed` - The value corresponding to the key, or the default value if the key is not found.

### Exists
`exists(array $array, string $key): bool`

Checks if the specified key exists in the array.

- **Parameters**:
    - `array $array` - The array to check.
    - `string $key` - The key to check for.
- **Returns**:
    - `bool` - True if the key exists in the array, false otherwise.

### Accessible
`accessible(mixed $value): bool`

Determines if the provided value can be accessed as an array.

- **Parameters**:
    - `mixed $value` - The value to check.
- **Returns**:
    - `bool` - True if the value is array accessible, false otherwise.

### Set
`set(array &$array, string $key, $value): Arr`

Sets a value in an array using 'dot' notation.

- **Parameters**:
    - `array &$array` - The array to modify.
    - `string $key` - The key in dot notation.
    - `mixed $value` - The value to set.
- **Returns**:
    - `Arr` - The instance of the Arr class.

### Has
`has(array $array, string $key): bool`

Checks if a specified key exists in the array and is not null.

- **Parameters**:
    - `array $array` - The array to check.
    - `string $key` - The key to check for.
- **Returns**:
    - `bool` - True if the key exists and is not null, false otherwise.

### Add
`add(array $array, string $key, $value): void`

Adds a value to an array using 'dot' notation if it does not already exist.

- **Parameters**:
    - `array $array` - The array to modify.
    - `string $key` - The key in dot notation.
    - `mixed $value` - The value to add.
- **Returns**:
    - `void` - No return value.

### Push
`push(array &$array, string $key, $value): void`

Pushes a value onto the end of an array segment defined by 'dot' notation.

- **Parameters**:
    - `array &$array` - The array to modify.
    - `string $key` - The key in dot notation.
    - `mixed $value` - The value to push.
- **Returns**:
    - `void` - No return value.

### Except
`except(array $array, $keys): array`

Returns a new array excluding specified keys.

- **Parameters**:
    - `array $array` - The array to filter.
    - `array|string $keys` - The keys to exclude.
- **Returns**:
    - `array` - The filtered array.

### Only
`only(array $array, $keys): array`

Returns a new array including only the specified keys.

- **Parameters**:
    - `array $array` - The array to filter.
    - `array|string $keys` - The keys to include.
- **Returns**:
    - `array` - The filtered array.

### Pluck
`pluck(array $array, $value, string $key = null): array`

Plucks an array of values from an array.

- **Parameters**:
    - `array $array` - The array to pluck from.
    - `string|array $value` - The value(s) to pluck.
    - `string|null $key` - The key to use as the array keys.
- **Returns**:
    - `array` - The plucked array.

### Forget
`forget(array &$array, string $key): array`

Removes an array item from a given key using "dot" notation.

- **Parameters**:
    - `array &$array` - The array to modify.
    - `string $key` - The key in dot notation.
- **Returns**:
    - `array` - The modified array.

### Collapse
`collapse(array $array): array`

Collapses an array of arrays into a single array.

- **Parameters**:
    - `array $array` - The array to collapse.
- **Returns**:
    - `array` - The collapsed array.

### Explode Key
`explode_key(string $key): array`

Explodes a key string into an array of segments using 'dot' notation.

- **Parameters**:
    - `string $key` - The key to explode.
- **Returns**:
    - `array` - The exploded key segments.



