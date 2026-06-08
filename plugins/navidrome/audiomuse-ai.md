# 🤖 AudioMuse AI Plugin

Repository: https://github.com/NeptuneHub/AudioMuse-AI-NV-plugin

## Description

AudioMuse AI brings advanced music discovery and recommendation features to Navidrome. By analyzing your music library and listening patterns, it helps surface similar artists, discover overlooked tracks, and generate personalized recommendations tailored to your collection.

## Features

* AI-powered music recommendations
* Discovery based on your music library
* Similar artist suggestions
* Personalized listening insights
* Enhanced music exploration
* Integration with Navidrome metadata agents

## Installation

### Docker

1. Download the latest plugin release from the repository.
2. Place the plugin files in your Navidrome plugins directory.
3. Restart the Navidrome container.

### Example Configuration

Enable the plugin in your metadata agent list:

```yaml
environment:
  ND_AGENTS: "audiomuseai,listenbrainz,apple-music,deezer,last.fm"
```

For best results, place `audiomuseai` near the beginning of the agent list so recommendations and metadata enhancements are prioritized.

## Compatibility

* Navidrome (Plugin System)
* Docker deployments
* Linux servers
* Self-hosted music libraries

## Open Source

✅ Yes

## Price

Free
