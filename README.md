# bpost e-MassPost Skills Library

![Beta](https://img.shields.io/badge/Status-Beta-orange)

AI agent skill library for the **BPost e-MassPost Mail ID** data exchange protocol.
Distributable as versioned ZIP files for Claude, Gemini, and other AI agent platforms.

## Feedback & Issues

This library is currently in **Beta**. If you or your AI agent encounters any errors, missing XML tags, or validation issues:
- [🐛 Report a Bug](https://github.com/markminnoye/bpost-e-masspost-skills/issues/new/choose)
- [✨ Request a Feature](https://github.com/markminnoye/bpost-e-masspost-skills/issues/new/choose)

## Skills

| Skill | Description | Status |
|---|---|---|
| [e-masspost-protocol](skills/e-masspost-protocol/) | Core protocol: schemas, flows, barcodes, error codes, transport | ✅ Available |

## Install (Claude.ai)

1. Go to the [Releases](../../releases) page
2. Download the skill ZIP: `e-masspost-claude-vX.X.X.zip`
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
