# Functions

This section documents the commonly used functions in the application, providing utility across the Framework.

## Redirection

!!! tip "Using Responses Outside Controllers"
    These functions are mostly used inside of a controller. If used outside of a controller, apply `RedirectResponse` with the `send` method.

### Redirect
`redirect(string|null $route): RedirectResponse`

- **Parameters**:
    - `string|null $route` - The route to redirect to. If null, this parameter is optional; use the 'route' method to set the path.
- **Returns**: 
    - `RedirectResponse` - The response object for redirection.

### Back
`back(): RedirectResponse`

- **Returns**: 
    - `RedirectResponse` - Redirects back to the previous page.

## Response and Request

### Response
`response(mixed|null $content, int $status_code = Response::HTTP_OK, HeaderBag|null $headers = null): Response`

- **Parameters**:
    - `mixed|null $content` - The content of the response. This parameter is optional.
    - `int $status_code` - HTTP status code, default is 200. This parameter is optional.
    - `HeaderBag|null $headers` - HTTP headers. This parameter is optional.
- **Returns**: 
    - `Response` - The response object.
- **Usage**:
    ```php
    <?php

    response()->json(['message' => 'success']);
    ```

### Request
`request(): Request`

- **Returns**: 
    - `Request` - The current request instance.

## Rendering

!!! tip "Rendering Views"
    To use the `view` function for returning raw content, chain the `render` method to it.

### View
`view(string $path, array|null $data = []): View`

- **Parameters**:
    - `string $path` - The path to the view file. This parameter is optional.
    - `array|null $data` - Data to pass to the view. This parameter is optional.
- **Returns**: 
    - `View` - The View instance.

## Navigation

### Resource Path
`resource_path(string|null $path): string`

- **Parameters**:
    - `string|null $path` - The path within the 'resources' directory. This parameter is optional.
- **Returns**: 
    - `string` - The absolute path to the 'resources' directory or its subdirectory.

### Public Path
`public_path(string|null $path): string`

- **Parameters**:
    - `string|null $path` - The path within the 'public' directory. This parameter is optional.
- **Returns**: 
    - `string` - The absolute path to the 'public' directory or its subdirectory.

### Storage Path
`storage_path(string|null $path): string`

- **Parameters**:
    - `string|null $path` - The path within the 'storage' directory. This parameter is optional.
- **Returns**: 
    - `string` - The absolute path to the 'storage' directory or its subdirectory.

### Base Path
`base_path(string|null $path): string`

- **Parameters**:
    - `string|null $path` - The path within the base directory. This parameter is optional.
- **Returns**: 
    - `string` - The absolute path to the base directory or its subdirectory.

### Normalize Path
`normalize_path(string $input): string`

- **Parameters**:
    - `string $input` - The file path to normalize.
- **Returns**: 
    - `string` - The normalized file path with backslashes converted to slashes.

## Session

### Session
`session(string|null $key = null, $value = null)`

- **Parameters**:
    - `string|null $key` - The session key. This parameter is optional.
    - `value (mixed)` - The value to set for the session key. This parameter is optional.
- **Returns**:
    - `Session` - The Session instance if no key is provided.
    - `string` - The session value if a key is provided.
- **Usage**:
    ```php
    <?php

    session('key', 'value');
    session('key');
    ```

### Error
`error(string $key): ?string`

- **Parameters**:
    - `string $key` - The key to retrieve the error.
- **Returns**: 
    - `string|null` - The error message or null if not found.

## Routing 

### Route
`route(string $name, array $parameters = []): ?string`

- **Parameters**:
    - `string $name` - The name of the route.
    - `array $parameters` - The route parameters. This parameter is optional.
- **Returns**: 
    - `string|null` - The URL for the named route with parameters applied.

### Server
`server(string|null $key = null)`

- **Parameters**:
    - `string|null $key` - The server key. This parameter is optional.
- **Returns**:
    - `Server` - The Server instance if no key is provided.
    - `mixed` - The server value if a key is provided.
- **Usage**:
    ```php
    <?php

    server('HTTP_HOST');
    ```

## Form

### Old
`old(string $key, ?string $default = null)`

- **Parameters**:
    - `string $key` - The key to retrieve the previous input value.
    - `string|null $default` - The default value if not found. This parameter is optional.
- **Returns**: 
    - `string` - The previous input value or the default value.

## Configuration

### Config
`config($key = null, $default = null)`

- **Parameters**:
    - `string|array|null $key` - The configuration key or an array of key-value pairs. This parameter is optional.
    - `mixed $default` - The default value if the key is not found. This parameter is optional.
- **Returns**: 
    - `array` - The entire configuration array if no key is provided.
    - `mixed` - The value of the configuration key or the default value.
- **Usage**:
    ```php
    <?php

    config('app.timezone');
    config(['app.timezone' => date_default_timezone_get()]);
    ```

## Debugging

### Dd
`dd(...$message)`

- **Parameters**:
    - `mixed $message` - The variable or message to be dumped.
- **Returns**: 
    - `void` - Dumps the variable or message and dies.

## Container

!!! important "Resolving Classes"
    The `get` function is used to resolve classes from the container. Classes are resolved by their fully qualified class name.

### Get
`get(string $abstract)`

- **Parameters**:
    - `string $abstract` - The fully qualified class name to resolve.
- **Returns**: 
    - `mixed` - An instance of the specified class.
- **Usage**:
    ```php
    <?php

    use App\Models\User;

    get(User::class);
    ```

## URL Generation

### Url 
`url(string|null $path = null, array $parameters)`

- **Parameters**:
    - `string|null $path` - The path for the URL. This parameter is optional.
    - `array $parameters` - Query parameters to include in the URL. This parameter is optional.
- **Returns**: 
    - `UrlGenerator` - The UrlGenerator instance if no path is provided.
    - `string` - The generated URL if a path is provided.
- **Usage**:
    ```php
    <?php

    url('/dashboard', ['search' => 'keywords']);
    ```

### Asset
`asset(string $path): string`

- **Parameters**:
    - `string $path` - The relative path to the asset.
- **Returns**: 
    - `string` - The full URL for the asset.
- **Usage**:
    ```php
    <?php

    asset('css/app.css');
    ```

