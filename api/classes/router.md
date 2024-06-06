# Router

The `Router` class in the `Framework\Support\Helpers` namespace provides a static interface to routing operations using the `Router` class.

## Methods

### Get
`get(string $uri, $action): ApplicationRouter`

- **Parameters**:
    - `string $uri` - The URI pattern for the route.
    - `array|string $action` - An array representing the controller and method to be called for this route.
- **Returns**: 
    - `ApplicationRouter` - The Router instance.
- **Usage**:
    ```php
    <?php

    Router::get('/user', [UserController::class, 'default']);
    ```

### Post
`post(string $uri, array $action): ApplicationRouter`

- **Parameters**:
    - `string $uri` - The URI pattern for the route.
    - `array $action` - An array representing the controller and method to be called for this route.
- **Returns**: 
    - `ApplicationRouter` - The Router instance.
- **Usage**:
    ```php
    <?php

    Router::post('/user', [UserController::class, 'store']);
    ```

### Routes
`routes(): RouteCollection`

- **Returns**: 
    - `RouteCollection` - The RouteCollection instance containing all registered routes.

