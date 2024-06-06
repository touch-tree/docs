# Installation

## Requirements

- PHP version 7.4 or higher

## Installation

!!! tip "Using Composer"
    This framework doesn't come with anything else than what is inside this repository, meaning that packages such as composer is not required, but is usable in this framework. 

To install, follow these detailed steps:

1. Navigate to the document root of your server. This is typically where your websites are stored and served from.

2. Use the following command to clone the repository into a directory.

   ```bash
   git clone https://github.com/dlt-media/boilerplate project-name
   ```

3. After cloning the repository, navigate into the cloned directory and run the following commands:

   ```bash
   cd project-name
   git submodule init
   git submodule update
   ```

These commands set up the submodules and pull in their latest changes ensuring that all parts of the framework are up to date and functional.
