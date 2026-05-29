# Subpath-safe canvas selection flow

## Links
- Use relative links from the canvas file to variant files.
- Do not use file URLs.
- Avoid root-relative endpoints when the preview may live under a nested customer path.

## Endpoint
- Put `preview-select.php` next to the canvas by default.
- Post to `preview-select.php`, not `/preview-select.php`.

## Persistence
- Append every response to `data/preview-selections.jsonl`.
- Mirror the newest response to `data/last-selection.json`.
- Return JSON so the canvas can confirm success inline.
