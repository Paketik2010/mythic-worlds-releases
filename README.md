# Mythic Worlds Releases

Public, binary-only distribution channel for Mythic Worlds.

This repository contains only signed update manifests and documentation. Installers, model packs, and media packs are attached to GitHub Releases. Application source code, source maps, environment files, private keys, API secrets, and build credentials are intentionally excluded.

## Update channels

- `manifests/app/stable.json` — signed Tauri application updates.
- `manifests/channel/stable.json` — independently versioned application, model, and media components.

Every application artifact is verified by the Tauri updater signature. Model and media archives are verified inside the Rust client using both a minisign signature and SHA-256 before extraction.

## Security

The signing private key is stored outside this repository. A compromised mirror cannot publish an accepted package without the private key. GitHub is only the delivery layer; it is not the root of trust.
