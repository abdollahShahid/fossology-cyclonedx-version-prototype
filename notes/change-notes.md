# Change Notes

This prototype refactors CycloneDX BOM header generation in `src/cyclonedx/agent/reportgenerator.php`.

## What changed
- Introduced `BOM_FORMAT` and `SPEC_VERSION` as dedicated constants
- Added `getSchemaUrl()` to derive the schema URL from the spec version
- Added `buildBomHeader()` to centralize BOM header creation
- Added `buildMetadata()` to separate metadata construction from report assembly
- Updated `generateReport()` to compose the final BOM from helper methods instead of building everything inline

## Before
The BOM header was created inline inside `generateReport()` with hardcoded values for:
- `bomFormat`
- `$schema`
- `specVersion`
- `version`
- `serialNumber`

## After
The BOM header is generated through backend helper methods, making the exporter structure cleaner and future version upgrades easier to manage from one place.
