<p align="center">
  <picture>
    <source srcset="./assets/icon-dark.svg" media="(prefers-color-scheme: dark)">
    <source srcset="./assets/icon-light.svg" media="(prefers-color-scheme: light)">
    <img src="./assets/icon-light.svg" alt="IT-Tools icon" width="128">
  </picture>
</p>

<h1 align="center">aac-it-tools</h1>

<p align="center">Deployment definition for IT-Tools, a set of browser-based tools for developers and IT staff.</p>

<p align="center">
  <a href="https://github.com/CorentinTh/it-tools"><img alt="Upstream" src="https://img.shields.io/badge/upstream-CorentinTh%2Fit--tools-blue"></a>
  <a href="https://hub.docker.com/r/corentinth/it-tools"><img alt="Image" src="https://img.shields.io/badge/image-corentinth%2Fit--tools-2496ED"></a>
  <a href="https://github.com/CorentinTh/it-tools/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/badge/license-GPL--3.0-green"></a>
</p>

## About

IT-Tools is a collection of useful tools for developers and people working in IT. Everything runs in the browser, so input data is processed client-side. The collection covers encoding and decoding, hashing and generators, formatting and conversion, network helpers and more.

Key features:

- Large set of small, single-purpose tools in one web UI
- Runs entirely in the browser, no backend required

## Upstream

- Project: [github.com/CorentinTh/it-tools](https://github.com/CorentinTh/it-tools)
- Homepage: [it-tools.tech](https://it-tools.tech)
- Image: `corentinth/it-tools` (Docker Hub), tag `2023.5.14-77f2efc`

## Quick start (Docker Compose)

This service does not require any external Docker networks.

```bash
docker compose up -d
```

No secrets are defined for this service, so no `.env` file is needed.

## Configuration

| Variable | Default | Description |
|---|---|---|
| `SERVICE_IMAGE_TAG` | `CHANGE_ME` | Image tag of `corentinth/it-tools` |
| `SERVICE_DOMAIN_NAME` | `CHANGE_ME` | Domain name the service is published under |
| `TZ` | `Europe/Berlin` | Time zone |
| `PUID` / `PGID` | `1000` | User and group IDs |
| `SERVICE_RESTART_POLICY` | `always` | Container restart policy |

Ports:

| Name | Container port | Protocol | External port |
|---|---|---|---|
| web | 80 | TCP | 28587 |

Volumes:

| Name | Container path | Description |
|---|---|---|
| `data` | `/data` | Persistent data for IT-Tools |

## Deploy with App-as-Code

The deployment files are rendered from `service.yml` by the App-as-Code template engine. Do not edit rendered output by hand; change `service.yml` instead. Releases are published under [github.com/app-as-code/aac-it-tools](https://github.com/app-as-code/aac-it-tools).

## Credits and license

- IT-Tools is developed by the upstream project maintainers and licensed under GPL-3.0. The license belongs to the upstream project.
- This repository contains only the deployment definition for the service.
- Icon: see [assets/ICON_SOURCE.md](assets/ICON_SOURCE.md).
