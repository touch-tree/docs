# Collection

The `Collection` class in the `Framework\Support` namespace represents a generic collection of items.

## Methods

### All
`all(): array<T>`

Retrieves all items in the collection.

- **Returns**: 
    - `array<T>` - The items in the collection.

### Is Empty
`is_empty(): bool`

Checks if the collection is empty.

- **Returns**: 
    - `bool` - True if the collection is empty, false otherwise.

### Get
`get(string|int $key, T $default = null): T`

Retrieves an item by key from the collection, with an option for a default value if the key does not exist.

- **Parameters**:
    - `string|int $key` - The key of the item to retrieve.
    - `T $default` - The default value if the key does not exist.
- **Returns**: 
    - `T` - The item value or the default value if the key does not exist.

### Set
`set(string|int $key, T $value): Collection<T>`

Sets an item in the collection with the specified key.

- **Parameters**:
    - `string|int $key` - The key of the item to set.
    - `T $value` - The value of the item.
- **Returns**: 
    - `Collection<T>` - The instance of `Collection`.

### Forget
`forget(string|int $key): Collection<T>`

Removes an item from the collection by key.

- **Parameters**:
    - `string|int $key` - The key of the item to remove.
- **Returns**: 
    - `Collection<T>` - The instance of `Collection`.

### Each
`each(callable(T): Collection $callback): Collection<T>`

Applies a callback to each item in the collection.

- **Parameters**:
    - `callable(T): Collection $callback` - The callback function to apply to each item.
- **Returns**: 
    - `Collection<T>` - The instance of `Collection`.

### Map
`map(callable(T): mixed $callback): Collection<T>`

Applies a callback to each item in the collection and returns a new collection with the results.

- **Parameters**:
    - `callable(T): mixed $callback` - The callback function to apply to each item.
- **Returns**: 
    - `Collection<T>` - A new collection with the results of the callback.

### Filter
`filter(callable(T): bool $callback): Collection<T>`

Filters the collection using a callback and returns a new collection containing only the items that passed the filter.

- **Parameters**:
    - `callable(T): bool $callback` - The callback function to use for filtering.
- **Returns**: 
    - `Collection<T>` - A new collection containing only the items that passed the filter.

### Contains
`contains(callable(T): bool $callback): bool`

Checks if the collection contains an item that passes the given condition.

- **Parameters**:
    - `callable(T): bool $callback` - The callback function to use for the condition.
- **Returns**: 
    - `bool` - True if the collection contains an item that passes the condition, false otherwise.

### First
`first(): T|null`

Retrieves the first item in the collection.

- **Returns**: 
    - `T|null` - The first item in the collection or null if the collection is empty.

### Last
`last(): T|null`

Retrieves the last item in the collection.

- **Returns**: 
    - `T|null` - The last item in the collection or null if the collection is empty.

### To Array
`to_array(): array<T>`

Converts the collection to a plain array.

- **Returns**: 
    - `array<T>` - The plain array representation of the collection.


