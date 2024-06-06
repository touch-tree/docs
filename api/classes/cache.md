# Cache

The `Cache` class in the `Framework\Support\Helpers` namespace provides a static interface to cache operations using the `CacheRepository`.

## Methods

### Get
`get(string $key, $default = null): mixed`

Retrieves an item from the cache by its unique identifier. Returns the item's value or a default value if the item is not found.

- **Parameters**:
    - `string $key` - The unique identifier for the cached item.
    - `mixed $default` - The default value to return if the item is not found in the cache.
- **Returns**:
    - `mixed` - The cached item value or the default value if the item is not found.

### Put
`put(string $key, $value, int $ttl): void`

Stores an item in the cache with a specified time-to-live (TTL).

- **Parameters**:
    - `string $key` - The unique identifier for the cached item.
    - `mixed $value` - The value to be stored in the cache.
    - `int $ttl` - The time-to-live for the cached item in seconds.
- **Returns**:
    - `void` - Indicates that the item has been stored.

### Has
`has(string $key): bool`

Checks if an item exists in the cache.

- **Parameters**:
    - `string $key` - The unique identifier for the cached item.
- **Returns**:
    - `bool` - True if the item exists in the cache, false otherwise.

### Forget
`forget(string $key): bool`

Removes an item from the cache.

- **Parameters**:
    - `string $key` - The unique identifier for the cached item to be removed.
- **Returns**:
    - `bool` - True if the item was successfully removed, false otherwise.

### Increment
`increment(string $key, int $value = 1): int|bool`

Increments the value of an item in the cache.

- **Parameters**:
    - `string $key` - The unique identifier for the cached item.
    - `int $value` - The value to increment the cached item by.
- **Returns**:
    - `int|bool` - The new value of the cached item or false on failure.

### Decrement
`decrement(string $key, int $value = 1): int|bool`

Decrements the value of an item in the cache.

- **Parameters**:
    - `string $key` - The unique identifier for the cached item.
    - `int $value` - The value to decrement the cached item by.
- **Returns**:
    - `int|bool` - The new value of the cached item or false on failure.

### Clear
`clear(): void`

Clears all entries from the cache.

- **Returns**:
    - `void` - Indicates that all entries have been cleared from the cache.

