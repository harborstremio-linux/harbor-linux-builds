# Harbor for Linux

Official Linux builds of [Harbor](https://github.com/harborstremio/harbor), built from its upstream source tags by GitHub Actions.

<p align="center">
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115"><strong>Download beta</strong></a>
  ·
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/latest"><strong>Download stable</strong></a>
  ·
  <a href="https://github.com/harborstremio/harbor"><strong>Harbor upstream</strong></a>
</p>

> **x86_64 only.** Choose the package that fits your distribution below. Every package download below follows the current [beta release](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115).

> **Beta is recommended.** Harbor development currently moves through the beta channel; stable releases are less frequent and can lag behind the current beta version.

## Install beta

### Arch Linux

Install the recommended beta package from the AUR. Updates arrive through your usual AUR helper.

```bash
paru -S harbor-stremio-beta-bin
```

Replace `paru` with `yay` if that is your helper.

### Ubuntu 24.04

Install the beta package repository for automatic updates.

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/harborstremio/harbor-beta/setup.deb.sh' | sudo -E bash
sudo apt install harbor-beta
```

[Download the latest .deb directly instead →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115)

### Fedora 44

Install the beta package repository for automatic updates.

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/harborstremio/harbor-beta/setup.rpm.sh' | sudo -E bash
sudo dnf install harbor-beta
```

[Download the latest .rpm directly instead →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115)

### Flatpak

[Download the latest .flatpak →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115)

```bash
flatpak install --user ./Harbor_*.flatpak
```

### AppImage (experimental)

[Download the latest .AppImage →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115)

```bash
chmod +x Harbor_*.AppImage
./Harbor_*.AppImage
```

For automatic updates, open the downloaded AppImage with [Gear Lever](https://github.com/mijorus/gearlever) and choose **Integrate**.

A portable x86_64 build using Tauri's experimental AppImage bundler, pending [upstream PR #12491](https://github.com/tauri-apps/tauri/pull/12491).

## Verify a download

Each release includes a SHA-256 checksum file for the core package assets. [Get SHA256SUMS from the current beta →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115)

```bash
sha256sum -c SHA256SUMS-*.txt
```

## Stable releases

Stable packages follow upstream Harbor release tags. They are published less frequently and may be behind the recommended beta channel.

- [Download the latest stable release](https://github.com/harborstremio-linux/harbor-linux-builds/releases/latest)
- Arch Linux: [`harbor-stremio-bin`](https://aur.archlinux.org/packages/harbor-stremio-bin)

```bash
paru -S harbor-stremio-bin
```

The stable and beta AUR packages conflict: they install the same Harbor application, so install one channel at a time.

## How it works

Beta is the primary channel. Each beta release is built from an exact `beta-branch` commit and published once per Harbor version; later commits with the same version do not create another release. Stable releases follow upstream Harbor release tags and can be behind beta. Releases provide `.deb`, `.rpm`, Flatpak, and an experimental AppImage bundle. Flatpak and AppImage build separately, so either can fail without blocking the core packages or the AUR update.

These are official Harbor Linux builds. The workflow and exact upstream source ref for each build are visible in the [Actions tab](https://github.com/harborstremio-linux/harbor-linux-builds/actions).

## Package repository hosting

<a href="https://cloudsmith.com"><img alt="OSS hosting by Cloudsmith" src="https://img.shields.io/badge/OSS%20hosting%20by-cloudsmith-blue?logo=cloudsmith&amp;style=flat-square" /></a>

Package repository hosting is graciously provided by [Cloudsmith](https://cloudsmith.com).
