# Changelog - BPost e-MassPost Skills Library

All notable changes to this project will be documented in this file.

## [v1.1.0] - 2026-03-29

### Added
- **Build Automation**: Integrated GitHub Actions pipeline for automatic version injection into Claude Skill bundles and automated releases.
- **English Localization**: Translated the technical guide and installation instructions from Dutch to English for international consistency.

### Fixed
- **Documentation Audit (BUG-001)**: Completed a comprehensive audit and reached 100% alignment with BPost XSD schemas.
  - Standardized all `Context`, `Header`, and `Item` attributes to strictly lowercase (e.g., `distributionOffice`, `icti`, `isec`).
  - Corrected legacy field names (e.g., `fieldToPrint1-3`) to modern XSD-compliant attributes.
  - Re-vetted all XML and TXT payload examples for technical accuracy.
- **Naming Standardization**: Unified the repository and naming convention to **e-MassPost** across all documentation, metadata, and routing guides.
- **YAML Frontmatter**: Resolved parsing errors in skill descriptions.

## [v1.0.0] - 2026-03-27

### Added
- Initial release of the agent-optimized BPost e-MassPost technical guide.
- Added Mermaid diagrams for technical protocol flows.
- Added BETA badging and agent feedback loop integration.
- Configured GitHub issue templates for bug reporting (BUG-001).

