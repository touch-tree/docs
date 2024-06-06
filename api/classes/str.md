# Str

The `Str` class in the `Framework\Support` namespace provides utility methods for string manipulation.

## Methods

### Finish
`finish(string $value, string $suffix): string`

Appends the given suffix to the string if it does not already end with it.

- **Parameters**:
    - `string $value` - The original string.
    - `string $suffix` - The suffix to be appended.
- **Returns**: 
    - `string` - The modified string.

### Start
`start(string $value, string $prefix): string`

Appends the given prefix to the string if it does not already start with it.

- **Parameters**:
    - `string $value` - The original string.
    - `string $prefix` - The prefix to be appended.
- **Returns**: 
    - `string` - The modified string.

### Limit
`limit(string $value, int $limit = 100): string`

Limits the number of characters in the string to a specified maximum.

- **Parameters**:
    - `string $value` - The original string.
    - `int $limit` - The maximum number of characters.
- **Returns**: 
    - `string` - The truncated string.

### Wrap
`wrap(string $value, string $prefix, ?string $suffix = null): string`

Wraps the given string with the specified prefix and suffix. If the suffix is null, the prefix is used as the suffix.

- **Parameters**:
    - `string $value` - The original string.
    - `string $prefix` - The prefix to prepend.
    - `string|null $suffix` - The suffix to append. If null, the prefix is used.
- **Returns**: 
    - `string` - The wrapped string.

### Ends With
`ends_with(string $haystack, $needles): bool`

Determines if the string ends with any of the specified substrings.

- **Parameters**:
    - `string $haystack` - The string to search in.
    - `string|string[] $needles` - The substring(s) to search for.
- **Returns**: 
    - `bool` - True if the string ends with any of the specified substrings, false otherwise.

### Starts With
`starts_with(string $haystack, $needles): bool`

Determines if the string starts with any of the specified substrings.

- **Parameters**:
    - `string $haystack` - The string to search in.
    - `string|string[] $needles` - The substring(s) to search for.
- **Returns**: 
    - `bool` - True if the string starts with any of the specified substrings, false otherwise.

### Append
`append(string $value, $append): string`

Appends the given values to the string.

- **Parameters**:
    - `string $value` - The original string.
    - `array|string $append` - The value(s) to append.
- **Returns**: 
    - `string` - The modified string.

