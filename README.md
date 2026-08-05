# atc-ci

CI/CD-Pipeline-Konfiguration für das gesamte A-TownChain-Ökosystem.

## Features (geplant)
- GitHub Actions Workflows für alle Repos
- Rust Test-Matrix (stable/nightly, x86_64-unknown-none/uefi)
- Python Test-Runner
- TypeScript Build & Lint
- Cross-Compilation (UEFI, no_std, std)
- Release-Automation (Tags, Changelogs)
- Kernel QEMU-Test-Harness
- Wiki-Sync-Validation
- Multi-Repo-Orchestrierung

## Struktur
```
.github/workflows/
  kernel-test.yml      # atc-shivacore (cargo test, QEMU)
  kernel-build.yml     # atc-shivacore (x86_64-unknown-none)
  bootloader-build.yml # atc-bootloader (x86_64-unknown-uefi)
  python-test.yml      # atc-backend, atc-gateway, etc.
  frontend-build.yml   # atc-frontend, atc-explorer, atc-ide
  wiki-sync.yml        # Wiki-Sync-Validation
  release.yml          # Tag-based Releases
```

## Status
- Initial: Repo erstellt 05.08.2026

---
Copyright © Michael Wroblewski / A-TownChain-Okosystems. All Rights Reserved.
