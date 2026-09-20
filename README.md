# Baikal

> TOS 7 application package for **Baikal** — platform integration only.
> The application itself is provided by the upstream project, unmodified.

## Overview

Lightweight CalDAV and CardDAV server for calendar and contact synchronisation.

上游项目 / Upstream: <https://sabre.io/baikal/>
上游许可证 / License: **GPL-3.0**

## Features

- CalDAV calendar server
- CardDAV contacts server
- Works with native iOS / Android / desktop clients
- Web-based administration

## Installation

1. Requirements: TOS 7.0+ and Docker Engine (install from the TOS App Center)
2. Install from the TOS App Center
3. Open the app and complete initial configuration

## Usage

1. Access URL: `http://${ip}:18804`
2. Default credentials: see upstream documentation
3. Key settings: see upstream documentation

## Permissions

| Permission | Rationale |
|---|---|
| Network: port 18804 | Web UI access |
| File system: `/Volume*/DockerAppData/shh4-baikal/` | Application data persistence |
| User: shh4baikal | Isolated non-root service execution |

## Configuration

See `config.ini` for platform metadata; see `docker-compose.yml` for runtime configuration.

## Ports

| Port | Protocol | Purpose |
|---|---|---|
| 18804 | TCP | Web UI (Baikal) |

## Support

- Documentation: https://sabre.io/baikal/
- Issue tracker: https://sabre.io/baikal//issues
- Community: https://sabre.io/baikal/

## Security & Compliance

- **License**: GPL-3.0 — full text in [`LICENSE`](./LICENSE)
- **Attribution**: see [`NOTICE`](./NOTICE)
- **Privacy Policy**: see [`PRIVACY.md`](./PRIVACY.md)
- **Vulnerability scan**: `trivy-report.txt` attached to each Release (HIGH/CRITICAL must be 0)
- Runs as a non-root dedicated user; no privileged mode, no host network

## Changelog

### v1.0.1 (2026-09-20)
- Compliance update: added LICENSE / NOTICE / PRIVACY materials,
  declared upstream license inside the package, added container healthcheck

### v1.0.0
- Initial release

## License

**GPL-3.0** — this packaging repository is distributed under the same license as the
upstream project. Full text: [`LICENSE`](./LICENSE).
