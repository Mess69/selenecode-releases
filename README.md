# selenecode-releases

Prebuilt binaries and package-manager metadata for
[SeleneCode](https://selenecode.com) — the source lives in a private repo
(`Mess69/SeleneCode`); this one is public so every install channel can read
from it without a token.

## Install

```bash
# macOS / Linux
curl -fsSL https://selenecode.com/install.sh | sh

# macOS / Linux, via Homebrew
brew install mess69/selenecode/selene
```

```powershell
# Windows
irm https://selenecode.com/install.ps1 | iex
```

```powershell
# Windows, via Scoop
scoop bucket add selenecode https://github.com/Mess69/selenecode-releases
scoop install selene
```

Once installed, `selene upgrade` updates in place; `selene upgrade --check` just looks.

## What lives here

- GitHub Releases: per-platform archives, `.sha256` sidecars, the shell/PowerShell installers,
  and `dist-manifest.json` — published by [`dist`](https://github.com/axodotdev/cargo-dist) from
  the source repo's CI on every `vX.Y.Z` tag.
- `bucket/selene.json` — the Scoop manifest, rewritten after each release by a post-announce job
  in the source repo's CI. Not hand-edited.

See [selenecode.com](https://selenecode.com) for what SeleneCode does.
