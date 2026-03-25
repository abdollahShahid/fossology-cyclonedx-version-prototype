# Evidence Notes

This prototype does not rely on screenshots as primary proof.

## Why screenshots are not primary evidence
Screenshots can be staged, cropped, or manually prepared. They are useful only as optional illustration.

## Primary evidence in this repository
The real evidence is machine-readable and reviewable:

- `code/reportgenerator.php.diff` shows the exact code change
- `baseline/bom-header-before.json` shows the previous header state
- `modified/bom-header-after.json` shows the new header state
- `notes/syntax-check.txt` shows CLI validation output

## What this proves
Together, these files show:
- the actual backend refactor
- the before/after export header difference
- the modified PHP file passes syntax checking
