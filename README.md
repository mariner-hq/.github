<p align="center">
  <img src="https://github.com/mariner-hq/mariner/blob/2d88d2ed13992628c89ab4eff09488ce5d908c62/web/src/components/mariner-logo/logo.svg" alt="Mariner" width="320" />
</p>

<h3 align="center">Your media. Your server. Your rules, forever.</h3>

<p align="center">
  A self-hosted media server written in Rust.<br/>
  Small, fast, honest about what it costs to run, and free. No Pro tier, ever.
</p>

<p align="center">
  <a href="https://github.com/mariner-hq/mariner">Server</a> ·
  <a href="https://github.com/mariner-hq/mariner/tree/main/docs">Docs</a> ·
  <a href="https://github.com/mariner-hq/mariner/blob/main/CONTRIBUTING.md">Contribute</a> ·
  <a href="https://github.com/mariner-hq/mariner/discussions">Discussions</a>
</p>

---

## Why Mariner

Somewhere along the way, streaming your own files started needing a subscription again. Mariner is a bet that it shouldn't: a media server that's fast, good-looking, and fully free, funded by the people who use it instead of the people who'd like to sell them something.

It's named after the sea I grew up next to and the woman who raised me. It's a legacy project, built to last.

## What makes it different

- **Light.** Rust, no managed runtime. In our own container tests it idles around 10–20 MB of RAM, and it scans a ~6,000-file library in well under a second (scan only, not the full metadata pipeline; method in the benchmark docs).
- **No paywall, ever.** Every feature is free. No bundled API keys, no "free tier." Dual-licensed MIT/Apache-2.0, no CLA.
- **Built for households, not just tinkerers.** Setup wizard, parental controls, guest links, and server-authoritative watch-together that stays in sync for the whole room.
- **Tells you the truth.** Real codec and color data instead of a spinner, and a metadata engine that shows when it's guessing.

## Where it is today

Pre-0.1. The core works and is under daily development; the first tagged release is close.

| | |
|---|---|
| **Works now** | Library scanning, TMDb/TVDb/MusicBrainz metadata, direct play, HLS with hardware transcoding, trickplay, skip intro/credits, offline downloads, multi-user, parental controls, guest sharing, OIDC SSO, watch-together, admin dashboard, web UI, Docker and single-binary builds |
| **Next** | Backup/restore, scheduled jobs, import from Plex/Jellyfin, transcode-reason transparency, 2FA |
| **Ahead** | HDR tone mapping, plugin SDK, native apps, live TV/DVR, on-device AI features (face-recognized home-video archive, a weekly digest with a voice) |

We're not claiming feature parity with Jellyfin or Plex yet. Native apps, plugins, and DVR are real gaps, and the roadmap says so.

## Try it

```bash
docker run -d --name mariner \
  -p 7797:7797 \
  -v /path/to/config:/config \
  -v /path/to/media:/media:ro \
  ghcr.io/mariner-hq/mariner:latest
```

Then open `http://localhost:7797`. The setup wizard finds your folders and starts scanning. Full guide: [deployment docs](https://github.com/mariner-hq/mariner/blob/main/docs/deployment.md).

## Get involved

- **Use it and tell us what breaks.** Real-device streaming reports are the most valuable thing right now.
- **Contribute.** Read [CONTRIBUTING.md](https://github.com/mariner-hq/mariner/blob/main/CONTRIBUTING.md) first (ADR process, tests required, docs stay in sync).
- **Build a client.** The API is OpenAPI-documented and has a getting-started guide.
- **Support it.** A donations link is coming. Mariner stays free either way.

---

<p align="center"><i>Built by one mariner, for the rest of us.</i></p>
