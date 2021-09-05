[![RuneJS Discord Server](https://img.shields.io/discord/678751302297059336?label=RuneJS%20Discord&logo=discord)](https://discord.gg/5P74nSh)


![RuneJS](https://i.imgur.com/pmkdSfc.png)

# @runejs/core

Core logging, networking, compression, encryption, and additional buffer functionality for RuneJS applications.

### @runejs/core
* `logger` is exported as a singleton Pino logging wrapper, offering the following functions:
    * `logger.info(...messages)`
    * `logger.debug(...messages)`
    * `logger.warn(...messages)`
    * `logger.error(...messages)`
    * `logger.fatal(...messages)`
    * `logger.trace(...messages)`
* Ability to set the Pino logging date/time formatting function via `setLoggerTimeFn(Pino.TimeFn)`
* Ability to set the Pino logging pretty print config value via `setLoggerPrettyPrint(boolean)`
* Setting of _all_ Pino logging options via `setLoggerOptions(Pino.LoggerOptions)`

### @runejs/core/buffer
* `ByteBuffer` is the main export.
  * Node `Uint8Array` wrapper with additional utility functions.
  * Unified configurable `get` and `put` methods to easily move bytes within the buffer.
  * Int24, Smart, Long and String type support.
  * Big endian, little endian, and mixed endian support.
  * Bit access through `openBitBuffer()`, `putBits()`, and `closeBitBuffer()`

### @runejs/core/net
* `SocketServer`
  * Handles connections made to a RuneJS socket server.
* `SocketServer.launch(serverName, hostName, port, connectionHandlerFactory)`
  * Spins up a new Node Socket server with the specified host and port.
* `ServerConfigOptions`
  * Options for a configured Socket server, imported using the `parseServerConfig()` function.

### @runejs/core/compression
* Exported class `Gzip` handles Gzip compression and decompression.
* Exported class `Bzip2` handles Bzip2 compression and decompression.

### @runejs/core/encryption
Provides XTEA encryption and decryption functionality, as well as a key file loader.
* Exported as class `Xtea`
