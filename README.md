# Bonzi Buddy for Codex

Unofficial, fan-made Bonzi Buddy pets for the Codex desktop app. Both editions include all nine standard animation states and a complete 16-direction look loop.

<p align="center">
  <img src="assets/bonzi-buddy-reference.png" alt="Original Bonzi Buddy reference holding a banana and a globe" width="520">
</p>

## Choose your Bonzi

### Globe Edition (recommended)

The Globe Edition adds a special working animation in which Bonzi holds and spins a vivid blue-and-green globe. The continents rotate across six frames, the globe stays attached to its stick, and the banana is absent during this animation.

<p align="center">
  <img src="assets/bonzi-buddy-globe-working.gif" alt="Bonzi Buddy spinning a blue and green globe" width="240">
</p>

Installable folder: [`bonzi-buddy-globe/`](bonzi-buddy-globe)

### Classic Edition

The original release keeps Bonzi's banana-focused animation set.

Installable folder: [`bonzi-buddy/`](bonzi-buddy)

## Install

Each pet is self-contained:

```text
bonzi-buddy-globe/
├── pet.json
└── spritesheet.webp
```

### macOS and Linux

Clone or download this repository, open a terminal in its directory, and install the recommended Globe Edition:

```bash
PET_ROOT="${CODEX_HOME:-$HOME/.codex}/pets"
mkdir -p "$PET_ROOT/bonzi-buddy-globe"
cp bonzi-buddy-globe/pet.json bonzi-buddy-globe/spritesheet.webp "$PET_ROOT/bonzi-buddy-globe/"
```

To install the Classic Edition instead, replace `bonzi-buddy-globe` with `bonzi-buddy` in all three places.

### Windows PowerShell

```powershell
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petDir = Join-Path $codexHome "pets/bonzi-buddy-globe"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\bonzi-buddy-globe\pet.json, .\bonzi-buddy-globe\spritesheet.webp -Destination $petDir -Force
```

Restart Codex after installation. The pet should then be available wherever your Codex build exposes custom pet selection.

## Share or install from a ZIP

You can send someone either complete pet folder as a ZIP. They only need to extract it under their Codex pets directory so the final layout is:

```text
${CODEX_HOME:-~/.codex}/pets/bonzi-buddy-globe/pet.json
${CODEX_HOME:-~/.codex}/pets/bonzi-buddy-globe/spritesheet.webp
```

The folder name and both files must be preserved. Source images and QA artifacts are not needed.

## Uninstall

Remove the installed `bonzi-buddy-globe` or `bonzi-buddy` folder from `${CODEX_HOME:-$HOME/.codex}/pets`, then restart Codex.

## Package details

- Codex pet format: v2
- Atlas: `1536 × 2288` WebP
- Grid: 8 columns × 11 rows
- Cell size: `192 × 208`
- Standard animation rows: 9
- Look directions: 16

## Disclaimer

This is an unofficial fan project. It is not affiliated with or endorsed by OpenAI or the original BonziBuddy creators. The character and reference artwork remain the property of their respective owners.
