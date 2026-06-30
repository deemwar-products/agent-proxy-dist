# AgentProxy — distribution

Public distribution mirror for **AgentProxy** by [deemwar-products](https://github.com/deemwar-products).
The application source is private; **only prebuilt, checksummed release artifacts** are published here
(as GitHub **Releases**), so the public install paths work without any authentication.

## Install

```bash
# npm (macOS / Linux / Windows)
npm install -g @deemwar-products/agent-proxy

# curl-pipe (macOS / Linux)
curl -fsSL https://agentproxy.deemwar.com/install.sh | bash

# Homebrew (macOS)
brew install deemwar-products/agent-proxy/agentproxy

# Scoop (Windows)
scoop bucket add agent-proxy https://github.com/deemwar-products/scoop-agent-proxy
scoop install agentproxy
```

Then:

```bash
agentproxy setup        # trust the local CA, log in once, start the proxy
agentproxy version
```

## What's here

- **Releases** — per-platform archives (`agentproxy_<version>_<os>_<arch>.{tar.gz,zip}`) + `checksums.txt`,
  published automatically by GoReleaser from the private source repo on each tagged release. The npm
  `postinstall` and the curl installer download + SHA256-verify these.
- This README — the public face of the project.

AgentProxy is a local MITM proxy that masks secrets before they leave your machine, meters token/$ spend
per agent, and adds governance — entirely local, no cloud account. Learn more: https://agentproxy.deemwar.com
