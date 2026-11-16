# aac-it-tools

A collection of useful browser-based developer and network tools. Notify-TEST

Container image: `corentinth/it-tools:2023.5.14-77f2efc`

## Quick start (docker compose)

```bash
cd deployments/docker_compose
docker compose up -d
```

The compose file expects these external Docker networks (create them once, or adapt `networks:`):

```bash
docker network create services-secured
docker network create services-exposed
docker network create docker-default
```

Data is stored under `/export/docker/<service>/` on the host (see `volumes:`). Hostnames use `example.com`;
the Traefik/auto-dns/homepage labels target the platform this was generated for - adjust or remove them.

## About this repository

`service.yml` is the single source of truth of this service. The files in `deployments/` are
generated from it with the [aac-template-engine](https://github.com/lyndrix-platform/aac-template-engine)
using placeholder values only. This repository is a release snapshot (one commit per release).
