# File

The `File` class in the `Framework\Support\Helpers` namespace provides a static interface to file system operations using the `Filesystem` service.

## Methods

### Files
`files(string $directory, $extension = []): array`

Retrieves files from a directory matching a specific extension. If no extension is specified, it returns all files.

- **Parameters**:
    - `string $directory` - The directory path.
    - `string|array|null $extension` - The extension(s) to filter by. If null, returns all files.
- **Returns**:
    - `array<SplFileInfo>` - An array of files.
- **Usage**:
    ```php
    <?php

    File::files('/path/to/directory', 'php');
    ```

### All Files
`all_files(string $directory, bool $recursive = true): array`

Retrieves all files and directories within a directory, optionally including subdirectories recursively.

- **Parameters**:
    - `string $directory` - The directory path.
    - `bool $recursive` - Whether to include subdirectories recursively.
- **Returns**:
    - `array<SplFileInfo>` - An array of files and directories.

### Put
`put(string $file_path, string $content): bool`

Writes content to a file.

- **Parameters**:
    - `string $file_path` - The path to the file.
    - `string $content` - The content to write to the file.
- **Returns**:
    - `bool` - True if the content was successfully written to the file, false otherwise.

### Directories
`directories(string $directory): array`

Retrieves directories within a specified directory.

- **Parameters**:
    - `string $directory` - The directory path.
- **Returns**:
    - `array` - An array of directory paths.

### Get
`get(string $file_path): string|false`

Retrieves the contents of a file.

- **Parameters**:
    - `string $file_path` - The path to the file.
- **Returns**:
    - `string|false` - The contents of the file, or false on failure.

### Exists
`exists(string $path): bool`

Checks if a file or directory exists.

- **Parameters**:
    - `string $path` - The path to the file or directory.
- **Returns**:
    - `bool` - True if the file or directory exists, false otherwise.

### Make Directory
`make_directory(string $directory): bool`

Creates a directory.

- **Parameters**:
    - `string $directory` - The directory path to create.
- **Returns**:
    - `bool` - True on success, false on failure.

### Has Extension
`has_extension(SplFileInfo $file, $extension): bool`

Checks if a file has a specific extension.

- **Parameters**:
    - `SplFileInfo $file` - The file object.
    - `string|array $extension` - The extension(s) to check against.
- **Returns**:
    - `bool` - True if the file has the specified extension, false otherwise.

### Delete
`delete($paths): bool`

Deletes one or multiple files or directories.

- **Parameters**:
    - `string|array $paths` - The path(s) to the file(s) or directory(s) to delete.
- **Returns**:
    - `bool` - True if all paths were successfully deleted, false otherwise.

### Delete Directory
`delete_directory(string $directory): bool`

Recursively deletes a directory.

- **Parameters**:
    - `string $directory` - The directory to delete.
- **Returns**:
    - `bool` - True if successfully deleted, false otherwise.

