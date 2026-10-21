# David Tenreiro

[![Marquee SVG](https://marquee.datf.net/?width=850&duration=55000&content=++++%E2%80%A2++++DAVID+TENREIRO++++%E2%80%A2++++PHP+%E2%80%A2+PYTHON+%E2%80%A2+C/C%2b%2b+%E2%80%A2+GO+%E2%80%A2+JAVASCRIPT+%E2%80%A2+SVELTE+%E2%80%A2+CI/CD+%E2%80%A2+GITHUB%20ACTIONS%20AND%20TEMPLATES+%E2%80%A2+DOCKER+%E2%80%A2+LINUX+%E2%80%A2+BASH+%E2%80%A2+VIM)](https://github.com/datf)

Software engineer focused on systems programming, lightweight container tooling, network proxies, and developer automation. I build tools with minimal runtime overhead, automated CI/CD pipelines, and practical self-hosted solutions for home automation and developer velocity.

---

## Home Assistant

All add-ons can be installed by adding this custom repository to your Home Assistant Add-on Store:  
**[`https://github.com/datf/hassio-addons`](https://github.com/datf/hassio-addons)**

* **[Caddy Custom (`hassio-caddy-custom`)](https://github.com/datf/hassio-caddy-custom)**  
  A modern, TLS-ready HTTP server and reverse proxy add-on for Home Assistant running Caddy 2.
  - **Dynamic Plugin Builds via xcaddy**: Compiles custom Caddy plugins (e.g. Cloudflare DNS, DuckDNS, custom middleware) directly inside the add-on using an integrated S6-overlay builder service—no custom Dockerfiles or manual builds required.
  - **Build Caching**: Tracks configured plugins, Go, and Caddy versions; builds only when changes are detected and activates the updated binary on container restart.

* **[Dante to WireGuard (`app-dante-to-wireguard`)](https://github.com/datf/app-dante-to-wireguard)**  
  Exposes a WireGuard VPN tunnel as a local SOCKS4/SOCKS5 proxy port on your network.
  - **Client-Free VPN Routing**: Routes traffic from local devices, scripts, or browsers through WireGuard without requiring VPN software on individual client devices.
  - **Profile Rotation & Fail-Safe Routing**: Sequentially rotates through multiple WireGuard configs (`wg0.conf`, `wg1.conf`, ...) on restart, binds proxy egress strictly to the VPN interface to prevent IP leaks, and clamps MTU to prevent packet stalls.

* **[Dante SOCKS Proxy (`app-dante`)](https://github.com/datf/app-dante)**  
  A robust SOCKS4/SOCKS5 forward proxy server running natively inside Home Assistant.
  - **Flexible Routing**: Supports custom `sockd.conf` routing rules and automated system-level credential provisioning for authenticated proxying.

---

## Containers

* **[adb-runner](https://github.com/datf/adb-runner)**  
  An ultra-lightweight (<20 MB) container image providing the latest Android Debug Bridge (`adb`).
  - **Minimal Footprint**: Replaces bulky Android SDK command-line tools and Java runtime dependencies with a clean Alpine-based container.
  - **Multi-Arch & Auto-Updating**: Pre-built for `linux/amd64` and `linux/arm64`. Automatically tracks upstream Alpine package updates via Renovate and GitHub Actions.
  - **Zero Host Pollution**: Ideal for wireless debugging, sideloading APKs, and headless CI/CD execution without local SDK installations.

* **[copier-runner](https://github.com/datf/copier-runner)**  
  A self-contained, Alpine-based container environment for [Copier](https://github.com/copier-org/copier) project templating.
  - **Integrated Toolchain**: Bundles Python 3, pip, Node.js, pnpm, and Git to execute template lifecycle hooks out of the box.
  - **Permission Handling**: Matches host UID/GID and mounts local directories so generated files retain correct ownership on the host.

---

## Systems & Go

* **[webos-discover](https://github.com/datf/webos-discover)**  
  A fast CLI tool in Go to discover and inspect LG webOS Smart TVs on local networks.
  - **Dual-Protocol Discovery**: Scans local subnets concurrently using mDNS (`zeroconf`) and SSDP/SDDP queries.
  - **Zero-Auth Hardware & OS Inspection**: Extracts hardware model, friendly name, MAC, UDN, and firmware, mapping internal LG codenames against an embedded database of 70+ webOS releases (2014–present) to identify consumer marketing versions and release years. Also supports authenticated SSAP WebSocket queries.

* **[SVG Marquee Generator (`svgmarquee`)](https://github.com/datf/svgmarquee)**  
  A dynamic Go service that generates seamlessly looping, animated SVG marquees for GitHub READMEs—powering the header banner above.
  - Automated [GitHub Actions](https://github.com/datf/svgmarquee/blob/main/.github/workflows/main.yml) pipelines with test verification and automated [release binary](https://github.com/datf/svgmarquee/releases) packaging.

---

## Web & Mods

* **[Calc LLC](https://github.com/datf/calc-llc)**  
  An interactive Svelte SPA deployed on [GitHub Pages](https://datf.github.io/calc-llc) calculating optimal gameplay strategies for Coal LLC using dynamic programming.
  - Features automated [CI](https://github.com/datf/calc-llc/blob/master/.github/workflows/ci.yml) and [CD](https://github.com/datf/calc-llc/blob/master/.github/workflows/deploy.yml) pipelines with [integration tests](https://github.com/datf/calc-llc/blob/master/src/lib/optimizer.test.js), containerized development environments (Podman/Docker), and Husky pre-commit checks.

* **Rocket League [Mods](https://github.com/datf/SpectatorReplaySkip) & [BakkesMod Plugin Template V2](https://github.com/datf/BakkesmodPluginTemplateV2)**  
  C++ modding boilerplate and automation for Rocket League.
  - A repository template configured with MSBuild SDK tooling, project boilerplate, and automated GitHub Actions workflows releasing specification-compliant zip packages.
