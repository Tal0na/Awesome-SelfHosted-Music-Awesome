# 🍎 Apple Music Metadata Plugin

Repository: https://github.com/navidrome/apple-music-plugin

## Description

This plugin enriches your Navidrome library with artist and album metadata sourced from Apple Music. It can provide biographies, artist images, similar artists, top tracks, and album artwork without requiring an Apple Music subscription or API key.

## Features

* Artist biographies
* Artist images
* Similar artists
* Album artwork
* Top songs

## Installation

### Docker

Download the latest release and place the plugin files inside your Navidrome plugins directory.

Example:

```text
/data/plugins/apple-music
```

Restart Navidrome after installing the plugin.

### Example Configuration

Enable the plugin in your metadata agents list:

```yaml
environment:
  ND_AGENTS: "apple-music"
```

Or combine it with other metadata providers:

```yaml
environment:
  ND_AGENTS: "listenbrainz,apple-music,last.fm"
```

## Open Source

✅ Yes

## Price

Free
