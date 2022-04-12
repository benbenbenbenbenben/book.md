oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @book.md/cli
$ bmd COMMAND
running command...
$ bmd (--version)
@book.md/cli/0.0.0 linux-x64 node-v16.13.2
$ bmd --help [COMMAND]
USAGE
  $ bmd COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`bmd hello PERSON`](#bmd-hello-person)
* [`bmd hello world`](#bmd-hello-world)
* [`bmd help [COMMAND]`](#bmd-help-command)
* [`bmd plugins`](#bmd-plugins)
* [`bmd plugins:install PLUGIN...`](#bmd-pluginsinstall-plugin)
* [`bmd plugins:inspect PLUGIN...`](#bmd-pluginsinspect-plugin)
* [`bmd plugins:install PLUGIN...`](#bmd-pluginsinstall-plugin-1)
* [`bmd plugins:link PLUGIN`](#bmd-pluginslink-plugin)
* [`bmd plugins:uninstall PLUGIN...`](#bmd-pluginsuninstall-plugin)
* [`bmd plugins:uninstall PLUGIN...`](#bmd-pluginsuninstall-plugin-1)
* [`bmd plugins:uninstall PLUGIN...`](#bmd-pluginsuninstall-plugin-2)
* [`bmd plugins update`](#bmd-plugins-update)

## `bmd hello PERSON`

Say hello

```
USAGE
  $ bmd hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/benbenbenbenbenben/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `bmd hello world`

Say hello world

```
USAGE
  $ bmd hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `bmd help [COMMAND]`

Display help for bmd.

```
USAGE
  $ bmd help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for bmd.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.12/src/commands/help.ts)_

## `bmd plugins`

List installed plugins.

```
USAGE
  $ bmd plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ bmd plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `bmd plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ bmd plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ bmd plugins add

EXAMPLES
  $ bmd plugins:install myplugin 

  $ bmd plugins:install https://github.com/someuser/someplugin

  $ bmd plugins:install someuser/someplugin
```

## `bmd plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ bmd plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ bmd plugins:inspect myplugin
```

## `bmd plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ bmd plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ bmd plugins add

EXAMPLES
  $ bmd plugins:install myplugin 

  $ bmd plugins:install https://github.com/someuser/someplugin

  $ bmd plugins:install someuser/someplugin
```

## `bmd plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ bmd plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ bmd plugins:link myplugin
```

## `bmd plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ bmd plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bmd plugins unlink
  $ bmd plugins remove
```

## `bmd plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ bmd plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bmd plugins unlink
  $ bmd plugins remove
```

## `bmd plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ bmd plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bmd plugins unlink
  $ bmd plugins remove
```

## `bmd plugins update`

Update installed plugins.

```
USAGE
  $ bmd plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
