# Harbor for Linux

Unofficial Linux builds of [Harbor](https://github.com/harborstremio/harbor), built from its upstream source tags by GitHub Actions.

<p align="center">
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115"><strong>Download beta</strong></a>
  ·
  <a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/latest"><strong>Download stable</strong></a>
  ·
  <a href="https://github.com/harborstremio/harbor"><strong>Harbor upstream</strong></a>
</p>

> **x86_64 only.** Choose the package that fits your distribution below. Every package download below follows the current [beta release](https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115).

> **Beta is recommended.** Harbor development currently moves through the beta channel; stable releases are less frequent and can lag behind the current beta version.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><img src="https://cdn.simpleicons.org/archlinux/1793D1" width="20" height="20" align="absmiddle" alt="" /> Arch Linux</h3>
      <p>Install the recommended beta package from the AUR. Updates arrive through your usual AUR helper.</p>
      <p><a href="https://aur.archlinux.org/packages/harbor-stremio-beta-bin"><strong>Open harbor-stremio-beta-bin on AUR →</strong></a></p>
      <pre><code>paru -S harbor-stremio-beta-bin</code></pre>
      <p><sub>Replace <code>paru</code> with <code>yay</code> if that is your helper.</sub></p>
    </td>
    <td width="50%" valign="top">
      <h3>
        <img src="https://cdn.simpleicons.org/debian/A81D33" width="20" height="20" align="absmiddle" alt="" />
        <img src="https://cdn.simpleicons.org/ubuntu/E95420" width="20" height="20" align="absmiddle" alt="" />
        <img src="https://cdn.simpleicons.org/linuxmint/87CF3E" width="20" height="20" align="absmiddle" alt="" />
        Debian, Ubuntu &amp; Mint
      </h3>
      <p><a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115"><strong>Download the latest .deb →</strong></a></p>
      <pre><code>cd ~/Downloads
sudo apt install ./Harbor_*.deb</code></pre>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>
        <img src="https://cdn.simpleicons.org/fedora/51A2DA" width="20" height="20" align="absmiddle" alt="" />
        <img src="https://cdn.simpleicons.org/opensuse/73BA25" width="20" height="20" align="absmiddle" alt="" />
        Fedora &amp; openSUSE
      </h3>
      <p><a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115"><strong>Download the latest .rpm →</strong></a></p>
      <p><strong>Fedora</strong></p>
      <pre><code>sudo dnf install ./Harbor-*.rpm</code></pre>
      <p><strong>openSUSE</strong></p>
      <pre><code>sudo zypper install ./Harbor-*.rpm</code></pre>
    </td>
    <td width="50%" valign="top">
      <h3><img src="https://cdn.simpleicons.org/flatpak/4A90D9" width="20" height="20" align="absmiddle" alt="" /> Flatpak</h3>
      <p><a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115"><strong>Download the latest .flatpak →</strong></a></p>
      <pre><code>cd ~/Downloads
flatpak install --user ./Harbor_*.flatpak</code></pre>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><img src="https://avatars.githubusercontent.com/u/16617932?s=200&amp;v=4" width="20" height="20" align="absmiddle" alt="" /> AppImage <small>(experimental)</small></h3>
      <h4><a href="https://github.com/harborstremio-linux/harbor-linux-builds/releases/tag/beta-v0.9.115">Download the latest .AppImage →</a></h4>
      <pre><code>cd ~/Downloads
chmod +x Harbor_*.AppImage
./Harbor_*.AppImage</code></pre>
      <h4>Automatic updates with <a href="https://github.com/mijorus/gearlever">Gear Lever</a></h4>
      <ol>
        <li>Open the downloaded AppImage with Gear Lever.</li>
        <li>Choose <strong>Integrate</strong>.</li>
        <li>Gear Lever discovers and installs future Harbor updates automatically.</li>
      </ol>
      <p><sub>A portable x86_64 build using Tauri's experimental AppImage bundler, pending <a href="https://github.com/tauri-apps/tauri/pull/12491">upstream PR #12491</a>.</sub></p>
    </td>
    <td width="50%" valign="top"></td>
  </tr>
</table>

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

Stable releases track upstream Harbor release tags. Beta releases track an exact commit from `beta-branch`. New releases provide `.deb`, `.rpm`, Flatpak, and an experimental AppImage bundle. Flatpak and AppImage build separately, so either can fail without blocking the core packages or the AUR update.

These are community-maintained builds, not binaries published by the upstream Harbor project. The workflow and exact upstream source ref for each build are visible in the [Actions tab](https://github.com/AdityaHebballe/harbor-linux-builds/actions).
