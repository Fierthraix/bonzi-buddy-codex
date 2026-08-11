# Bonzi Buddy for Codex

An unofficial, fan-made Bonzi Buddy pet for the Codex desktop app. He is a cheerful purple gorilla with expressive eyes, a friendly smile, a banana, nine standard animation states, and a complete 16-direction look loop.

<p align="center">
  <img src="assets/bonzi-buddy-reference.png" alt="Bonzi Buddy holding a banana and a globe" width="520">
</p>

## Install

This repository contains the complete pet in [`bonzi-buddy/`](bonzi-buddy):

```text
bonzi-buddy/
├── pet.json
└── spritesheet.webp
```

### macOS and Linux

Clone or download this repository, open a terminal in its directory, and run:

```bash
PET_ROOT="${CODEX_HOME:-$HOME/.codex}/pets"
mkdir -p "$PET_ROOT/bonzi-buddy"
cp bonzi-buddy/pet.json bonzi-buddy/spritesheet.webp "$PET_ROOT/bonzi-buddy/"
```

### Windows PowerShell

Clone or download this repository, open PowerShell in its directory, and run:

```powershell
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petDir = Join-Path $codexHome "pets/bonzi-buddy"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\bonzi-buddy\pet.json, .\bonzi-buddy\spritesheet.webp -Destination $petDir -Force
```

Restart Codex after installation. Bonzi Buddy should then be available wherever your Codex build exposes custom pet selection.

## Install from a ZIP

If someone sends you only the `bonzi-buddy` folder as a ZIP, extract it so the final layout is:

```text
${CODEX_HOME:-~/.codex}/pets/bonzi-buddy/pet.json
${CODEX_HOME:-~/.codex}/pets/bonzi-buddy/spritesheet.webp
```

The folder name and both files must be preserved. QA artifacts and source images are not required for installation.

## Uninstall

Remove the installed pet folder, then restart Codex:

```bash
rm -rf "${CODEX_HOME:-$HOME/.codex}/pets/bonzi-buddy"
```

## Package details

- Codex pet format: v2
- Atlas: `1536 × 2288` WebP
- Grid: 8 columns × 11 rows
- Cell size: `192 × 208`
- Standard animation rows: 9
- Look directions: 16

## Disclaimer

This is an unofficial fan project. It is not affiliated with or endorsed by OpenAI or the original BonziBuddy creators. The character and reference artwork remain the property of their respective owners.
