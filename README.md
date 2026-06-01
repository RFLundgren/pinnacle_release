# Pinnacle Releases

This repository hosts Windows release artifacts for **Pinnacle**.

Pinnacle is a desktop application for:
- AI-generated photo descriptions and keywords
- Immich library sync and metadata enrichment
- duplicate review workflows
- smart albums and metadata-driven search

## Which file should I download?

Choose one installer:

- `Pinnacle-<version>-x64-setup.exe`
  - for most Windows PCs with Intel or AMD processors
- `Pinnacle-<version>-arm64-setup.exe`
  - for Windows on ARM devices
- `Pinnacle-<version>-setup.exe`
  - combined installer containing both architectures

For most users, the best choice is the architecture-specific installer:
- x64 PC: `Pinnacle-<version>-x64-setup.exe`
- ARM64 PC: `Pinnacle-<version>-arm64-setup.exe`

## Why are there 3 installer files?

There are three installer files because the release includes:

1. an **x64-only** installer
2. an **ARM64-only** installer
3. a **combined** installer that supports both architectures

The architecture-specific installers are smaller and are the preferred downloads when you know the target machine type.

The combined installer exists mainly for updater and distribution compatibility.

## What are the `.blockmap` files?

The `.blockmap` files are **auto-update metadata** used by Electron's updater.

They are not installers and most users do not need to download them manually.

They help the updater:
- detect file changes efficiently
- support differential update downloads
- validate release artifacts during update operations

## What is `latest.yml`?

`latest.yml` is the Windows update manifest used by the packaged app to discover the newest available release from GitHub Releases.

It tells the updater:
- the latest version
- which installer files exist
- file sizes and hashes

## Private beta note

Current Windows builds are signed with a **self-signed certificate** for private beta testing.

That means:
- they are suitable for controlled testing
- they are **not** publicly trusted like a commercial code-signing certificate
- some systems may require trust/import steps for the certificate

## Source code

Source code lives in the main project repository:

- [RFLundgren/Pinnacle](https://github.com/RFLundgren/Pinnacle)

