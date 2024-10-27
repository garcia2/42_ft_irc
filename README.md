# ft_irc

**ft_irc** is a project from 42 school focused on building a basic IRC (Internet Relay Chat) server. The goal is to implement an IRC server capable of handling multiple client connections, managing channels, and allowing real-time communication between users.

## Table of Contents
1. [Overview](#overview)
2. [Project Architecture](#project-architecture)
3. [Technologies Used](#technologies-used)
4. [Features](#features)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Author](#author)

## Overview

The **ft_irc** project is an implementation of a simple IRC server based on the RFC 1459 standard. This server allows multiple clients to connect, join channels, send messages, and interact in real time. The project provides experience with network programming, socket management, and handling multiple concurrent connections.

## Project Architecture

- **Socket Management** : Manages incoming and outgoing connections using TCP sockets.
- **Multi-Client Handling** : Uses multiplexing to handle multiple clients simultaneously.
- **Command Parsing** : Interprets and executes IRC commands based on client input.

## Technologies Used

- **C Language** : Core programming language for server implementation
- **POSIX Sockets** : For network communication and connection handling
- **Select System Call** : For multiplexing and managing multiple connections

## Features

1. **Multi-Client Support** : Manages multiple client connections simultaneously.
2. **Channels** : Allows clients to create, join, and leave channels.
3. **User Commands** : Supports basic IRC commands such as `/join`, `/part`, `/nick`, and `/msg`.
4. **Real-Time Messaging** : Enables clients to communicate with each other in real time.

## Installation

To set up `ft_irc`, clone the repository and compile the server program.

```bash
git clone https://github.com/garcia2/42_ft_irc
cd 42_ft_irc
make
```

This will create an executable named `ircserv`.

## Usage

To start the server, run:

```bash
./ircserv <port> <password>
```

- `<port>` : The port number on which the server will listen for client connections.
- `<password>` : The password required for clients to connect.

Clients can connect to the server using an IRC client such as `netcat`, `HexChat`, or `irssi`:

```bash
nc localhost <port>
```

## Author

Project developed by [Nicolas Garcia](https://github.com/garcia2) as part of 42 school.
