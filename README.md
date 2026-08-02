# Harbor for Linux

Official Linux builds of [Harbor](https://github.com/harborstremio/harbor), built from its upstream source tags by GitHub Actions.

<p align="center">
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116"><strong>Download beta</strong></a>
  ·
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/latest"><strong>Download stable</strong></a>
  ·
  <a href="https://github.com/harborstremio/harbor"><strong>Harbor upstream</strong></a>
</p>

> **x86_64 only.** Choose the package that fits your distribution below. Every package download below follows the current [beta release](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116).

> **Beta is recommended.** Harbor development currently moves through the beta channel; stable releases are less frequent and can lag behind the current beta version.

## Install beta

### <img src="https://cdn.simpleicons.org/archlinux/1793D1" width="20" height="20" align="absmiddle" alt="" /> Arch Linux

Install the recommended beta package from the AUR. Updates arrive through your usual AUR helper.

```bash
paru -S harbor-stremio-beta-bin
```

Replace `paru` with `yay` if that is your helper.

---

### <img src="https://cdn.simpleicons.org/ubuntu/E95420" width="20" height="20" align="absmiddle" alt="" /> Ubuntu 24.04

Install the beta package repository for automatic updates.

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/harborstremio/harbor-beta/setup.deb.sh' | sudo -E bash
sudo apt install harbor-beta
```

[Download the latest .deb directly instead →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116)

---

### <img src="https://cdn.simpleicons.org/fedora/51A2DA" width="20" height="20" align="absmiddle" alt="" /> Fedora 44

Install the beta package repository for automatic updates.

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/harborstremio/harbor-beta/setup.rpm.sh' | sudo -E bash
sudo dnf install harbor-beta
```

[Download the latest .rpm directly instead →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116)

---

### <img src="https://cdn.simpleicons.org/flatpak/4A90D9" width="20" height="20" align="absmiddle" alt="" /> Flatpak

Install Harbor Beta from [<img src="https://flatpark.org/logo.svg" width="18" height="18" align="absmiddle" alt="" /> FlatPark](https://flatpark.org/) for automatic updates.

```bash
flatpak --user remote-add --if-not-exists flatpark https://dl.flatpark.org/flatpark.flatpakrepo
flatpak --user remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak --user install flatpark site.harbor.Harbor.Beta
```

FlatPark provides the current beta channel. Flathub support will follow when stable Harbor releases become the main focus again.

Prefer not to add FlatPark? [Download the latest .flatpak bundle instead →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116)

```bash
flatpak install --user ./Harbor_*.flatpak
```

---

### <img src="https://avatars.githubusercontent.com/u/16617932?s=200&amp;v=4" width="20" height="20" align="absmiddle" alt="" /> AppImage (experimental)

[Download the latest .AppImage →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116)

```bash
chmod +x Harbor_*.AppImage
./Harbor_*.AppImage
```

For automatic updates, open the downloaded AppImage with [Gear Lever](https://github.com/mijorus/gearlever) and choose **Integrate**.

A portable x86_64 build using Tauri's experimental AppImage bundler, pending [upstream PR #12491](https://github.com/tauri-apps/tauri/pull/12491).

## Verify a download

Each release includes a SHA-256 checksum file for the core package assets. [Get SHA256SUMS from the current beta →](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.116)

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
