# Anti Minecart Crash

A lightweight Minecraft Paper plugin that helps protect servers from minecart-based crash attempts by limiting the amount of minecarts per chunk.

## Description

Anti Minecart Crash is a simple server protection plugin for Paper/Spigot servers.

The plugin checks how many minecarts already exist inside a chunk. If the configured limit is reached, new minecart spawns or minecart placements in that chunk are cancelled.

This can help reduce lag, entity spam, and possible minecart crash attempts on Minecraft servers.

## Features

- Limits the amount of minecarts per chunk
- Cancels minecart spawning when the limit is reached
- Cancels minecart placement when the limit is reached
- Configurable minecart limit
- Lightweight and easy to use
- No commands needed
- Built with Java and Maven
- Made for Paper/Spigot servers

## How It Works

The plugin listens for minecart-related events.

When a minecart is spawned or placed, the plugin checks the current chunk and counts all existing minecarts inside that chunk.

If the amount of minecarts is equal to or higher than the configured limit, the action is cancelled.

## Configuration

The plugin creates a configuration value for the maximum amount of minecarts allowed per chunk.

Default value:

```yml
max-minecarts_per_chunk: 150
```

You can lower or increase this value depending on your server needs.

Example:

```yml
max-minecarts_per_chunk: 50
```

A lower value gives stronger protection against minecart spam.

## Installation

1. Download or build the plugin `.jar`
2. Put the `.jar` file into your server's `plugins` folder
3. Start or restart your server
4. Open the generated config file
5. Change the minecart limit if needed
6. Restart the server

## Requirements

- Java 17 or newer
- Paper or Spigot server
- Minecraft 1.20 or newer recommended

## Dependencies

This project uses:

- Paper API 1.20.4
- Maven Compiler Plugin
- Maven Shade Plugin

## Build

Clone the repository:

```bash
git clone https://github.com/FilipPikus/Minecraft-Plugin-Anti-Minecart-Crash.git
cd Minecraft-Plugin-Anti-Minecart-Crash
```

Build the plugin with Maven:

```bash
mvn clean package
```

The compiled `.jar` file will be located in the `target` folder.

## Project Structure

```txt
src/main/java        Plugin source code
src/main/resources   Plugin resources such as plugin.yml
pom.xml              Maven project file
LICENSE              Project license
```

## Commands

This plugin does not require any commands.

Protection works automatically after the plugin is installed and enabled.

## Educational Purpose

This project is also useful for learning basic Minecraft plugin development, including:

- Creating Paper plugins
- Registering event listeners
- Listening to entity spawn events
- Listening to player interaction events
- Cancelling events
- Reading configuration values
- Building Java plugins with Maven

## License

This project is licensed under the Apache License 2.0.
