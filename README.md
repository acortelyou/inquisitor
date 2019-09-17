# Inquisitor

This multi-container app is intended to help bootstrap an easy and quick off-site statuspage that provides HTTP and DNS monitoring.

## Containers

* postgres - database
* cachet - status page
* cachet-monitor - url monitoring
* nginx-proxy - reverse proxy
* letsencrypt - https
* ddclient - dynamic dns

## Installation

1. set env vars
2. create `/opt/ddclient/ddclient.conf`
3. `docker-compose up -d`
4. setup cachet
5. set `CACHET_TOKEN` env var
6. create `/opt/cachet-monitor/cachet-monitor.yml`
7. `docker-compose restart`
