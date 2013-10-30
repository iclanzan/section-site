# Basic Usage

The `section` terminal command is made available upon installation which is used to generate and serve static websites.

The most common way is to execute the command without any options.

```
$ section
```
In this case a website will be generated into `./output` from the current directory and served from `http://localhost:8000`. While the server is running changes made in this directory will cause the website to be regenerated and changes reflected to all connected clients.

## Available options

### `--base`

Specify an alternate base directory. This will generate a site from a directory other than the current working directory.


### `--output`

The site will be generated from the current directory and into the specified output directory.


### `--url`

Specify a URL for your website. This will be made available to the layout template.


### `--config`

Specify a configuration file. This overrides the configuration file in the current directory if present.


### `--port`

Change the default port of `8000` for serving generated websites.


### `--help`

This will print all available options and subcommands.
