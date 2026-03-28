# bpost e-MassPost Skills Library

AI agent skill library for the **BPost e-MassPost Mail ID** data exchange protocol.
Distributable as versioned ZIP files for Claude, Gemini, and other AI agent platforms.

## Skills

| Skill | Description | Status |
|---|---|---|
| [epost-masspost-protocol](skills/epost-masspost-protocol/) | Core protocol: schemas, flows, barcodes, error codes, transport | ✅ Available |

## Install (Claude.ai)

1. Go to the [Releases](../../releases) page
2. Download the skill ZIP: `epost-masspost-claude-vX.X.X.zip`
3. Go to `claude.ai/customize/skills` → Upload ZIP
4. Enable the skill

## Versioning

This repo uses semantic versioning (`vMAJOR.MINOR.PATCH`). Each GitHub Release
automatically builds and attaches the skill ZIPs via GitHub Actions.

## Reference Materials

The `reference/` folder contains the original BPost technical documentation
(PDF, screenshots, XSD schemas) for human and developer use.
These files are **not included** in skill ZIPs.

## License

See [LICENSE](LICENSE).
