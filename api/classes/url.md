# Url

The `Url` class in the `Framework\Support\Helpers` namespace provides a static interface to URL generation operations using the `UrlGenerator` class.

## Methods

### To

`public static function to(string $path, array $parameters = [], bool $absolute = true): string`

- **Parameters**:
    - `string $path` - The path to the resource.
    - `array $parameters` - Query parameters to include in the URL. This parameter is optional.
    - `bool $absolute` - Whether to exclude the host from the generated URL. This parameter is optional.
- **Returns**: 
    - `string` - The generated absolute URL.
- **Usage**: 
    ```php
    <?php

    Url::to('/user/details', ['id' => 1]);
    ```

### Route

`public static function route(string $name, array $parameters = [], bool $absolute = true): string`

- **Parameters**:
    - `string $name` - The name of the route.
    - `array $parameters` - Parameters to substitute into the route URI. This parameter is optional.
    - `bool $absolute` - Whether to generate an absolute URL (including scheme and host). This parameter is optional.
- **Returns**: 
    - `string` - The generated URL.
- **Usage**:
    ```php
    <?php

    Url::route('user.details', ['id' => 1]);
    ```

### Full
`public static function full(): string`

- **Returns**: 
    - `string` - The full base URL for the application. Returns the relative path if 'app.url' is not set.

### Current
`public static function current(): string`

- **Returns**: 
    - `string` - The current URL.
