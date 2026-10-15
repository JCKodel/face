# FACE

FACE (Focus Agentic Code Environment) is the window a team opens to build
software when agents write the code. You run one `face` binary in a folder
of projects; it treats each subfolder as a project, plants the
[focus-kit](https://github.com/JCKodel/focus-kit) method in it, and lets you
talk, from the browser, to the coding agent you already pay for (Claude
Code, Codex, Copilot, Cursor, Antigravity, OpenCode, Qwen Code). What the
method keeps in files (queue, pages, documents, decisions) FACE shows as a
board, milestones, progress and cost.

[Leia em português](README.pt.md)

The site, in the six languages of the FACE screen, with screenshots and
the downloads: <https://face.kodel.com.br>.

## Install

On macOS or Linux, with [Homebrew](https://brew.sh):

```sh
brew install jckodel/face/face
```

On Windows, with [winget](https://learn.microsoft.com/windows/package-manager/):

```powershell
winget install JCKodel.FACE
```

On Debian or Ubuntu, download the `.deb` for your machine from Releases
(`face_<v>_amd64.deb` or `face_<v>_arm64.deb`) and install it with `apt`,
which also installs `git`:

```sh
sudo apt install ./face_<v>_amd64.deb
```

On Linux, or on macOS without Homebrew, the script from the site downloads
the zip for your machine from Releases, checks it against `SHA256SUMS` and
puts `face` in `~/.local/bin`, without sudo:

```sh
curl -fsSL https://face.kodel.com.br/install.sh | sh
```

Then run `face` in the folder that holds your projects, or give it that
folder from anywhere:

```sh
cd ~/Projects && face
face ~/Projects
```

To update, run `brew upgrade face` or `winget upgrade JCKodel.FACE`,
install the new `.deb` the same way, or run the same `curl` line again.

## Download by hand

This is the manual way. The zips are on
[the site](https://face.kodel.com.br) and in
[Releases](https://github.com/JCKodel/face/releases), one per platform:

- `face-<v>-darwin-arm64.zip` (macOS, Apple Silicon)
- `face-<v>-darwin-amd64.zip` (macOS, Intel)
- `face-<v>-linux-amd64.zip` (Linux x86_64)
- `face-<v>-linux-arm64.zip` (Linux arm64)
- `face-<v>-windows-amd64.zip` (Windows x86_64)
- `face-<v>-windows-arm64.zip` (Windows arm64)

Download the one for your platform, unzip it in the folder that holds your
projects and run `face` there, with nothing to rename:

```sh
./face      # macOS, Linux
face.exe    # Windows
```

On a Mac, if macOS refuses to open `face`, it is because the file the
browser downloaded and Finder unzipped comes in quarantine. Remove the
quarantine and run it again:

```sh
xattr -d com.apple.quarantine face
./face
```

Each release also has `SHA256SUMS`. Download it next to the zip and check
it with:

```sh
shasum -a 256 -c --ignore-missing SHA256SUMS
```

## Terms

FACE is free to download and use. The source is not public yet; the license comes later.

This repository holds only issues and binaries, so `go install` does not
work: download the binary for your platform instead.

Each release carries `THIRD_PARTY_NOTICES.txt`, with the name, version,
license and license text of the third-party software the binary includes.

## Issues

Bug reports and requests are welcome in any of the six languages of the
FACE screen: English, Portuguese, Spanish, French, German or Simplified
Chinese. Open one in [Issues](https://github.com/JCKodel/face/issues/new/choose).
The `Report a bug` link at the bottom of the FACE home opens the bug form
with your version filled in.
