---
title: "Personal server"
date: 2021-12-21T16:39:27+05:30
draft: false
---

Details about my [personal server](https://luna.ovh), mostly for my reference.

---
<!--more-->

I'm running a [Hetzner](https://hetzner.cloud) server running located in Helsinki, FI. Based on personal experience, I would highly recommend them if you are in the market for a server yourself.

The server has 4 cores, 8GB RAM and 160GB SSD storage. It runs Debian 11 (my preferred server distribution thanks to support and release cadence). I use Caddy as a reverse proxy, as I'm too lazy for Nginx. I use Python and BASH scripts to keep things running, and systemd services and cron jobs to run those scripts when necessary. I use Docker containers when possible to avoid dependency hell and isolate the config from the application. This also helps me back up my config files and other data as required.

I share the server with my friend [Silvy](https://github.com/Silveee), who maintains and hosts a few Discord bots for the community of some obscure Flash game (yes, Adobe Flash in 2022, don't ask).

---

The following applications do not require authentication, and can be used by anyone:

- [CloudTube](https://yt.luna.ovh) - YouTube proxy
- [files](https://files.luna.ovh) - file uploads (uses [gossa](https://github.com/pldubouilh/gossa))
- [luna](https://luna.ovh) - server startpage ([repo](https://github.com/yellow404/luna.ovh))
- [send](https://send.luna.ovh) - temporary file sharing
- [speed](https://speed.luna.ovh) - speed test
- [yellow](https://yellow.luna.ovh) - this website ([repo](https://github.com/yellow404/yellow.luna.ovh))

---

The following applications require authentication (contact me if you need access):

- [anime](https://anime.luna.ovh) - media library (uses [Jellyfin](https://jellyfin.org/))
- [files](https://files.luna.ovh/private) - private uploads
- [wireguard](https://files.luna.ovh/private/vpn/Luna.conf) - VPN config (uses [wireguard](http://wireguard.com/))

---

The following applications are for server use:

- [anime metadata](https://metadata.luna.ovh) - uses [Plex](https://plex.tv) and the [Hama](https://github.com/ZeroQI/Hama.bundle) and [Lambda](https://github.com/ZeroQI/Lambda.bundle) plugins to generate .nfo metadata files for media
- [NewLeaf](https://newleaf.luna.ovh) - YouTube data extractor, powers [CloudTube]](https://yt.luna.ovh)
- [torrent client](https://torrent.luna.ovh) - web client to download and upload decentralised files (uses [ruTorrent](https://github.com/Novik/ruTorrent))
- [upload](https://upload.luna.ovh) - read/write access to [files](https://files.luna.ovh), used for uploads