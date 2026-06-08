# 🎼 MusicBrainz Metadata Plugin

Repository: https://github.com/navidrome/navidrome-plugin-musicbrainz

## Description

Enhance your Navidrome library with rich metadata sourced directly from MusicBrainz, one of the world's largest open music databases. The plugin improves artist, album, and release information, helping keep your collection organized and accurately tagged.

## Features

* Artist metadata enrichment
* Album metadata enrichment
* Release and release group information
* Improved library organization
* Open community-maintained database
* Better metadata accuracy across your collection

## Installation

### Docker

1. Download the latest plugin release.
2. Place the plugin files in your Navidrome plugins directory.
3. Restart the Navidrome container.

### Example Configuration

Enable the MusicBrainz agent:

```yaml
environment:
  ND_AGENTS: "musicbrainz"
```

Or combine it with other metadata providers:

```yaml
environment:
  ND_AGENTS: "musicbrainz,listenbrainz,apple-music,last.fm"
```

## Why Use MusicBrainz?

MusicBrainz is one of the most comprehensive open music databases available. It is maintained by a global community and provides high-quality metadata for artists, albums, releases, recordings, labels, and more.

Using MusicBrainz as a metadata source can improve consistency across your library and help identify missing or incomplete tags.

## Compatibility

* Navidrome (Plugin System)
* Docker deployments
* Linux servers
* Self-hosted music libraries

## Open Source

✅ Yes

## Price

Free
