# 👑 discord-status.me
Small documentation of my Discord-Rich-Presence API.

> Visit it on: [discord-status.me](https://discord-status.me)

# Table of contents
- [How to setup](#how-to-setup)
- [Examples](#examples)
  - [Activity Object](#activity-object)
    - [Spotify Example](#spotify-example)
    - [VSC Example](#vsc-example)
  - [Emoji Object](#emoji-object)
    - [Animated Example](#animated-example)
    - [Static Example](#static-example)
    - [Default Discord Emoji Example](#default-discord-emoji-example)
- [Public Flags](#public-flags)
- [Status_Image Icons](#status_image-icons)
- [Future Features](#future-features)
# How to setup:
1. Join [discord.gg/bio](https://discord.com/invite/bio)
1. Copy your userID.
1. Visit `https://discord-status.me/raw/:userID`
- > Replace `:userID` with your discord userID

# Examples
1. [discord-status.me/raw/:userID](https://discord-status.me/raw/910213408576659517)
> Below is the scheme of the raw response.
##### Keys marked with * in their name are unpromised values. They might not appear in your request.

```json
{
      "activities": [
        "Activity Object(s)"
      ],
      "custom_status": {
      "created_at": "null || Unix Timestamp",
      "emoji": "null || emojiObject",
      "text": "null || String"
      },
      "device": {
        "desktop": "bool",
        "mobile": "bool",
        "web": "bool",
        "raw": "bool // desktop or mobile or web"
      },
      "spotify": {
        "active": "bool",
        "data": "null || spotifyObject"
      },
      "status": "int",
      "status_image": "String",
      "status_text": "String",
      "user": {
        "avatar": "String",
        "bot": "bool",
        "discriminator": "String",
        "id": "String",
        "public_flags": "int",
        "username": "String"
  }
}
```

### Activity Object

<hr />

#### _Spotify example_
```json
{
      "assets*": {
        "large_image": "https://i.scdn.co/image/ab67616d0000b273f44798b00503b6c57b88406c",
        "large_text*": "HYSTERIA",
        "small_image": "https://discord-status.me/static/images/unknown.png"
      },
      "created_at*": 1658170937294,
      "details*": "HYSTERIA",
      "flags": 48,
      "id": "spotify:1",
      "images": {
        "large_image": "https://i.scdn.co/image/ab67616d0000b273f44798b00503b6c57b88406c",
        "small_image": "https://discord-status.me/static/images/unknown.png"
      },
      "name": "Spotify",
      "party*": {
        "id*": "spotify:910213408576659517"
      },
      "session_id*": "ff5518c34922a079d5acee79de9ae7eb",
      "state*": "WoLRa; zyx",
      "sync_id*": "5ODC2OUMssM7B61walhPJH",
      "timestamps*": {
        "end*": 1658171071350,
        "start*": 1658170936610
      },
      "type*": 2
    }
```

#### _VSC Example:_
```json
{
      "application_id*": "383226320970055681",
      "assets": {
        "large_image": "https://cdn.discordapp.com/app-assets/383226320970055681/603581316352442376.png",
        "large_text*": "Editing a SVELTE file",
        "small_image": "https://cdn.discordapp.com/app-assets/383226320970055681/565945770067623946.png",
        "small_text*": "Visual Studio Code"
      },
      "created_at*": 1658166248756,
      "details*": "Editing Nav.svelte",
      "id*": "89f33982e0aef243",
      "images": {
        "large_image": "https://cdn.discordapp.com/app-assets/383226320970055681/603581316352442376.png",
        "small_image": "https://cdn.discordapp.com/app-assets/383226320970055681/565945770067623946.png"
      },
      "name": "Visual Studio Code",
      "state*": "Workspace: xev.dev",
      "timestamps*": {
        "start*": 1658157199661
      },
      "type*": 0
    }
```

### Emoji Object

<hr />

#### _Animated Example_
```json
{
  "name": "pepestare",
  "value": "http://cdn.discordapp.com/emojis/991887626581840002.gif?size=96&quality=lossless"
}
```

#### _Static Example_
```json
{
  "name": "logo",
  "value": "http://cdn.discordapp.com/emojis/991891535106949171.png?size=96&quality=lossless"
}
```

#### _Default Discord Emoji Example_
```json
{
  "name": ":gear:",
  "value": "https://discord.com/assets/a6d05968d7706183143518d96c9f066e.svg"
}
```

### Public Flags

<hr />

| Value | Shift | Name |
| ----- | ----- | ---- |
| 1 | 1 << 0 | Discord Employee
| 2 | 1 << 1 | Partnered Server Owner
| 4 | 1 << 2 | HypeSquad Events
| 8 | 1 << 3 | Bug Hunter Level 1
| 16 | 1 << 4 | ???
| 32 | 1 << 5 | ???
| 64 | 1 << 6 | House of Bravery
| 128 | 1 << 7 | House of Brilliance
| 256 | 1 << 8 | House of Balance
| 512 | 1 << 9 | Early Supporter
| 1024 | 1 << 10 | Team User
| 2048 | 1 << 12 | System
| 4096 | 1 << 13 | Bug Hunter Level 2
| 8192 | 1 << 14 | ???
| 32768 | 1 << 15 | ???
| 65536 | 1 << 16 | Verified Bot
| 131072 | 1 << 17 | Early Verified Bot Developer

### Status_Image Icons

<hr />

| ID | Status Text | Status Image |
|----|-------------|-------|
| 0 | Offline | ![Offline](https://discord-status.me/static/images/offline.png) |
| 1 | Online | ![Online](https://discord-status.me/static/images/online.png) | 
| 2 | Idle | ![IDLE](https://discord-status.me/static/images/idle.png) | 
| 3 | Do Not Disturb | ![DND](https://discord-status.me/static/images/dnd.png) |

## Future Features
- [ ] Add Public Flag Names
- [ ] Usercards to display in Github README's (Using SVGs)
