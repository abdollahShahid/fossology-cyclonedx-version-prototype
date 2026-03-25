# FOSSology CycloneDX Version Prototype

This repository contains a pre-GSoC prototype based on the CycloneDX export pipeline in FOSSology.

## What this prototype shows
This prototype demonstrates a small but real backend refactor in the CycloneDX exporter. The change restructures how the BOM header is generated inside `src/cyclonedx/agent/reportgenerator.php` and shows a clear before/after change in the exported CycloneDX header.

## What was implemented
- moved BOM header creation into dedicated backend helper methods
- centralized `bomFormat`, `specVersion`, and schema URL generation
- separated metadata construction from report assembly
- produced a prototype header output showing CycloneDX `1.7`

## Repository structure
- `baseline/` - header output before the change
- `modified/` - header output after the change
- `code/` - actual diff from `reportgenerator.php`
- `notes/` - short explanation of the refactor

## Important note
This is a prototype slice of the broader CycloneDX upgrade work. It demonstrates backend ownership of the correct export path, but it does not claim that the full exporter is already fully migrated to CycloneDX 1.7.
