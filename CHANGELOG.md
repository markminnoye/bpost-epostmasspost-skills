# Changelog - BPost e-MassPost Skills Library

All notable changes to this project will be documented in this file.

## [v1.0.1] - 2026-03-28

### Added
- Created formal `CHANGELOG.md` to track technical protocol updates.

### Fixed
- **Schema Alignment (BUG-001)**: Comprehensive audit fixed multiple casing and naming inconsistencies between Markdown docs and XSD source of truth.
  - Corrected `<Context>` tag attributes to lowercase in `mailing-request.md`.
  - Mapped `fieldToPrint1-3` to `distributionOffice`, `routeName`, `routeSeq` in `mailing-response.md`.
  - Corrected indication flags to `icti`, `isec`, `ioff`, `irnd`.
  - Renamed `depositRef` to `depositIdentifier` in `deposit-response.md`.
  - Re-vetted XML and TXT examples across all schema documents.

## [v1.0.0] - 2026-03-27

### Added
- Initial release of the agent-optimized BPost e-MassPost technical guide.
- Added Mermaid diagrams for technical protocol flows.
- Added BETA badging and agent feedback loop integration.
- Configured GitHub issue templates for bug reporting (BUG-001).
- Standardized e-MassPost naming conventions.
