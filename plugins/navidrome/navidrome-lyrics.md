# 📜 Navidrome Lyrics Plugin

Repository: https://github.com/J0R6IT0/navidrome-lyrics-plugin

## Description

Automatically fetches, stores, and manages song lyrics from multiple online sources for use with Navidrome and compatible Subsonic clients. The plugin supports both plain and synchronized lyrics, making it easier to follow along with your music while listening.

## Features

* Multiple lyrics providers
* Automatic lyric fetching
* Embedded lyrics support
* Synchronized (LRC) lyrics support
* Local lyrics file support
* Lyrics caching and storage
* Compatible with Navidrome and Subsonic clients

## Installation

### Docker

1. Download the latest plugin release.
2. Place the plugin files in your Navidrome plugins directory.
3. Restart the Navidrome container.

### Example Configuration

Enable the lyrics plugin in your lyrics priority list:

```yaml
environment:
  ND_LYRICSPRIORITY: ".lrc,nd-lyrics"
```

This configuration prioritizes local `.lrc` files before querying the Navidrome Lyrics Plugin.

## Supported Sources

The plugin can retrieve lyrics from multiple providers, improving coverage and increasing the chances of finding lyrics for tracks in your library.

Depending on the provider, both plain text and synchronized lyrics may be available.

## Compatibility

* Navidrome (Plugin System)
* Docker deployments
* Linux servers
* Subsonic-compatible clients
* LRC-enabled music players

## Open Source

✅ Yes

## Price

Free
