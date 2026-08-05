# ATC-CI — Continuous Integration

CI/CD-Pipeline für A-TownChain OS — Build, Test, Deploy über alle 70 Repos.

## Pipeline
```
┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐
│  Push/PR │──→│  Build   │──→│  Test    │──→│  Deploy  │
└──────────┘   └──────────┘   └──────────┘   └──────────┘
                   │              │              │
                   ▼              ▼              ▼
              ┌────────┐    ┌────────┐    ┌──────────┐
              │ Lint   │    │ Unit   │    │ Staging  │
              │ Format │    │ E2E    │    │ Mainnet  │
              │ Type   │    │ Coverage│   │ Testnet  │
              └────────┘    └────────┘    └──────────┘
```

## Workflows
| Workflow | Trigger | Description |
|----------|---------|-------------|
| `build.yml` | push/PR | Build all modules |
| `test.yml` | push/PR | Run unit + integration tests |
| `lint.yml` | push/PR | Code formatting + type checks |
| `release.yml` | tag | Create release artifacts |
| `deploy-testnet.yml` | main push | Deploy to Testnet |
| `nightly.yml` | schedule | Full audit + nightly build |

## Matrix
- **OS:** Ubuntu 22.04, macOS 14, Windows 11
- **Rust:** stable, beta, nightly
- **Python:** 3.11, 3.12, 3.13
- **Node:** 20, 22

## Verwandte Repos
- Alle 70 Repos nutzen diese CI-Konfiguration

[agent: aurora-base44-superagent-6a2756186106d6f0fbb105b5]
