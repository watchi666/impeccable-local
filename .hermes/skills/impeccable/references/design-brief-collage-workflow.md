# Design-Brief-Collage workflow

## Source priority
1. customer project photos
2. logo or wordmark assets
3. screenshots from the current site
4. references already named in PRODUCT.md or DESIGN.md

## Format
- wide horizontal image around 1400×600px
- overlapping elements
- no spaced-out moodboard grid
- visible anti-goals and character words
- keep the image count tight, usually 3 to 4 images total
- enforce a hard hierarchy: 1 lead image, then 2 to 3 supporting proof images

## Image hierarchy rules
- the lead image must be the strongest trust-bearing motif available, usually the most finished and spatially convincing room, stair, facade, or detail
- do not let a raw Baustelle, cluttered work-in-progress shot, bucket, tool pile, or random phone-photo crop dominate the collage just because it has contrast or occupies more area
- supporting images should cover different proof roles, for example finished room, material surface, and precise detail or built-in element
- if the business sells completed spaces, the collage should bias toward finished-result imagery first and process imagery second
- process images may appear only as subordinate proof, never as the hero contract for a premium direction

## Creation method

Preferred: image generation via PIL/Pillow (Python) composing real project images on a 1400×600 canvas with design tokens from DESIGN.md.

Fallback when Pillow is unavailable, system-protected, or images cannot be composed programmatically:
- Build an HTML page at `collage-direction-[a|b|c].html` in the project root
- Use absolute-positioned `<img>` tags with real project image paths (`bilder/...`)
- Apply the warm image filter (`sepia(8%) saturate(95%)`) and design tokens via CSS
- Render text overlays (direction label, character words, anti-goals, craft-translation) with CSS positioned text
- Serve via PHP dev server on available port and capture as screenshot, or deliver the HTML directly for browser viewing
- The HTML collage is functionally equivalent: same images, same hierarchy, same design-token annotations
- When the designated port (e.g., 8124) is blocked by a zombie process and cannot be freed due to permission constraints, use the next available port and report the actual URL to the user

## Craft translation checklist
Before craft, name:
- composition pattern
- material language
- type energy
- spacing rhythm
- CTA behavior

The collage is a build contract, not decoration.
