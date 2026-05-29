# Local-business preview rules

Use this reference for trades, renovation, interior, and service-business preview work.

## Existing-site upgrade rules

### Keep the business's real world intact
When the task is an update of an existing business site, do not jump straight into replacement imagery.

Before craft:
1. inspect the live site visually
2. identify which images currently carry the real world of the business
3. decide whether those images should remain the backbone of the redesign

If the current site already has authentic, trust-bearing project photos, prefer reusing that image world over swapping in merely better-looking but less specific alternatives.

For local trades and renovation businesses, a modern redesign that loses the firm's actual material world is usually worse than an older site with honest images.

### Inherit good content structure and photo scale, not the old look
When the live site already has a sensible section order and image-sizing discipline, preserve those strengths even when the visual design is rebuilt from scratch.

That means:
- reuse the useful reading order from the live site when it helps the customer understand the business faster
- treat the old site as a structure and emphasis reference, not only as a content bucket
- if the live site uses photos in a restrained way, do not inflate them into giant showcase slabs just because the redesign is darker or more premium
- prefer one dominant hero image, then medium or small support images in later acts, unless the brief explicitly demands a more image-heavy composition
- in service sections, a single smaller material or proof image can be stronger than a second oversized gallery moment
- contact should not end in a giant decorative closing image if the live site's strength was direct contact clarity

Hard review question before signoff:
Did we keep the useful section logic and photo restraint from the original business site while still producing a clearly better overall visual system?

### Original-site inheritance is literal when the user says so
If the user says the photos, hero, or areas should be "übernommen", treat that as a direct structural requirement, not a mood hint.

That means:
- preserve the original section acts unless there is a clear conversion reason to change them
- preserve the original hero principle first: image role, full-width vs boxed, text overlay density, and CTA placement relative to the image
- reuse the same trust-bearing photo family where possible, especially for trades sites where authentic project shots are stronger than prettier replacements
- if one project from the original site carries most of the proof weight, make it visibly dominant in the rebuilt page rather than hiding it behind a generic portfolio label
- if a project gets its own detail page, the parent page still needs a strong teaser with enough visual mass that visitors notice it without hunting

- when the owner asks whether the page was checked against anti-slop patterns, answer that audit question directly before you talk about fixes or implementation
- for inherited heroes, prefer the exact live hero asset or an exact supplied counterpart when retrievable, not just a similar image family
- testimonial hierarchy must be obvious in one glance: one lead quote materially larger and roomier than the supporting quotes, not merely first in DOM order

### Anti-slop checks specific to handwerker redesigns
Before signoff, explicitly reject these patterns:
- KPI lines or fact chips with suspiciously round marketing numbers like `10+`, `500+`, `15 Spezialisten` when they read as invented dashboard filler
- timid project teasers that make a key proof project easy to miss in the scroll
- section styling that reveals the page as stacked modules too clearly, with each act reading as a separate block instead of one dark continuous stage
- oversized all-caps headlines that overpower the photography and flatten hierarchy by making every section scream at the same volume
- anti-grid layouts that still create accidental overlaps, tight collisions, or near-collisions between images and text

If factual stats are shown at all, prefer one of these:
- exact values from the source material
- slightly irregular but credible counts grounded in the business story
- or no numbers, if the numbers cannot be defended

### Local Business Pre-Signoff Gate
Hard gate. Pass or fail. If one point fails, the page is not finished and must not be described as ready, polished, or final.

1. **Hero inheritance passes**
   - Pass: the rebuilt hero preserves the original hero principle when the brief said the hero should be übernommen, including image role, breadth, and CTA relationship.
   - Fail: the hero drifted into a safer boxed or generic layout.
2. **Hero image family passes**
   - Pass: the lead image still belongs to the source site's trust-bearing image family, or an exact supplied counterpart.
   - Fail: the hero uses a prettier but less source-true replacement.
3. **Section acts pass**
   - Pass: the original homepage acts still survive recognisably, unless a change was explicitly justified.
   - Fail: the rebuild replaced the business flow with generic module order.
4. **Lead project hierarchy passes**
   - Pass: the standout project is clearly dominant, and if it needs depth it has its own destination page with a strong homepage teaser.
   - Fail: the lead project got flattened into a small generic preview.
5. **No KPI widget contamination**
   - Pass: trust is integrated narratively or structurally.
   - Fail: four-up numbers, stat chips, or dashboard-style metric blocks survived.
6. **No equal-card service system**
   - Pass: services read as guided flow, editorial sequence, image-plus-rail composition, or another structure that is clearly not a repeated card mechanism.
   - Fail: the service area is still a card row, accordion-card set, repeated equal tile system, or a staggered version of the same underlying card logic.
   - Fail: simply offsetting cards, changing column spans, or adding numbering does not count as a new structure if each service still reads like the same box repeated five times.
7. **No mini-raster proof teaser**
   - Pass: proof imagery has hierarchy and visual mass.
   - Fail: key project or proof imagery collapsed into a tidy three-up or similar mini-gallery raster.
8. **Contact integration passes**
   - Pass: the contact ending resolves inside the same surface language as the rest of the page.
   - Fail: a bright or pasted-on closing slab breaks the page atmosphere.

### When a project gets its own detail page, give it real depth
If a live or inherited site has a named project section that gets split onto its own page, that detail page must feel like a real project proof page, not a teaser stretched onto a new URL.

Minimum expectations before signoff:
- keep the finished-result hero image or an equally trust-bearing result image as the lead visual
- include a true gallery block with several project-specific images, not just one hero plus one or two repeats
- use the source folder aggressively, especially when the user explicitly pointed to a project like Stockum as important proof
- make sure the start page teaser still points clearly into that deeper gallery

Failure mode to avoid:
- extracting a project into its own page, then leaving only two images and calling it a gallery

## Visual design rules
1. Build the page on one continuous stage, not many competing color zones.
2. Use a few large visual masses instead of many small modules.
3. Give the hero one dominant image body.
4. Arrange imagery compositionally, not as a repeated equal-box grid.
5. Leave generous negative space between major moves.
6. Let important text sit in free space, not constantly inside boxes.
7. Use one oversized anchor and a brutal hierarchy step-down.
8. Favor controlled asymmetry over sterile symmetry or fake chaos.
9. Avoid visible modular showroom logic.
10. Concentrate visual force into a few decisive moments, not evenly distributed decoration.
11. Anti-grid is not permission for accidental overlap: do not rely on negative vertical offsets that make images or text collide. Create asymmetry with scale, column span, positive spacing, and stagger that still reads as deliberate.
12. When matching an inherited dark original, compare background depth as a first-class design property. If the rebuild drifts lighter, darken the stage and overlays before adding more modules.

## Mobile-First — Pflicht

Mindestens 2/3 der Besucher kommen vom Mobilgerät.
Jede Seite wird zuerst für Mobile gebaut, dann für Desktop erweitert.

Pflicht:
- Layout ab 375px vollständig funktionsfähig
- Touch-Targets mindestens 44x44px
- Schriftgrößen auf Mobile nicht unter 16px
- Bilder mobile-optimiert (srcset oder max-width: 100%)
- Navigation auf Mobile klar und erreichbar
- Kein horizontales Scrollen
- Kontakt und CTA auf Mobile sofort sichtbar ohne Scrollen

Selbstprüfung:
- Wurde die Seite zuerst auf 375px designed?
- Funktioniert alles auf Mobile ohne Pinch-Zoom?

## Narrative Flow & Anti-Box Architecture

### Core Philosophy: The Continuous Canvas

The page is not built as a sequence of boxes. It is built as one continuous canvas where content flows seamlessly into the next section.

### Absolute Prohibitions — Anti-Pattern Registry

- **Alternating backgrounds** — Sections must NOT be separated by alternating background colours (white → light grey → white). The background stays colour-homogeneous.
- **Card containers** — Content like services must NEVER be boxed with `border` or `shadow`. Containerless design: content stands free in space.
- **Alibi grids** — The typical 3-column icon grid is strictly forbidden. No compromise of "only 2 columns".
- **Full-width dividers** — No horizontal lines (`<hr>` or `border-b`) between content sections.

### Spatial & Kinetic Rules

- **Whitespace multiplier** — Drastically increase vertical spacing between sense units. At least `py-28` to `py-36` (112px–144px) so content breathes and transitions feel fluid.
- **Asymmetric axis break** — Every following sense unit MUST break the visual axis of the previous element. If text sits top-left, the next element is centred-narrow or asymmetrically pushed right. This forces the eye to travel instead of jump.
- **Typographic dominance** — Extreme contrasts: large, characterful headlines alternate with surprisingly small but perfectly readable body copy. Typography is a design element, not just labelling.

### The 4 Allowed Flow Archetypes

Pick one per build — or combine them. No other layout principle is allowed.

**Archetype A: Asymmetric Split (Focus: Dynamism)**
- No grids. Canvas mentally split 50/50.
- Element 1: huge headline left, room-filling image right.
- Element 2: mirrored — image left, text right.
- Images switch sides; never twice on the same side in a row.

**Archetype B: Editorial Style (Focus: Premium Craft)**
- Single column, maximum whitespace.
- Text blocks stand free in space (left-aligned or slightly indented).
- Interrupted only by full-bleed images (`h-screen`) that act as visual resting pillows.
- Sub-headlines so large they become independent design elements.

**Archetype C: Linear Guide (Focus: Process / Flow)**
- A thin, subtly coloured vertical CSS line runs through the entire site as a red thread.
- All content docks left or right of this line.
- The eye automatically follows this axis while scrolling.

**Archetype D: Proof Path (Focus: Project Photos)**
- Photos are the primary element; text is annotation.
- Full-bleed project photos dominate the page.
- Per project: one huge main image (`h-screen`), one detail beside it.
- Text appears as short, precise annotation — never long paragraphs.
- Contact emerges when the proof path ends — no separate section.

### DESIGN.md Directive — Kinetic Path

When shape is executed, the architecture must NOT be planned as a classic section list. The plan must be defined as a **kinetic path**:

1. **THE HOOK (Hero)** — Massive, bold typography tracking into screen centre. No bounding box. Full viewport.
2. **CONTINUOUS DESCENT** — Fluid transition into asymmetric layout. Content shifted off-axis to pull the eye down. No section border, no background change.
3. **THE PROOF TRAIL** — Full-bleed project showcase instead of thumbnail grids. Seamless scrolling transitions between projects.
4. **THE ANCHOR (Contact)** — Minimalist interface fading directly out of the canvas background. No separate footer block. No white slab.

### Self-Check before Signoff

1. Anywhere alternating backgrounds? → Remove
2. Any cards with border or shadow? → Remove
3. Any 3-column icon grid? → Remove
4. Any horizontal dividers between sections? → Remove
5. Which flow archetype did I use? → Name it
6. Does every sense unit break the visual axis of the previous one? → Check
7. Does the page feel like one piece while scrolling? → Must be true

Only when all seven are ✓: Signoff.

## Guided scroll flow, not anti-structure
The page should feel like one piece, not a stack of unrelated blocks. Use soft transitions and uneven rhythm, but keep clear content acts.

Required:
- the page reads as one guided composition
- transitions are soft, but functional shifts remain legible
- density, pacing, scale, and proof change deliberately across the scroll
- contact lands like a finale, not leftover admin

Do not confuse anti-grid with anti-structure. A page that melts all section boundaries but loses reading order, trust-building, and momentum is still wrong.

Reliable act structure for local service businesses:
1. strong opening stage
2. positioning or attitude
3. service condensation
4. visible proof, reference, or process
5. contact as the logical landing

## Required page structure: seven sections
1. **Header / navigation**
   - logo or brand name
   - anchor links to the main sections
   - direct contact visible in the header
2. **Hero**
   - dominant real customer image
   - strong main statement
   - one or two sentences of subcopy
   - at least one CTA
3. **Positioning / core statement**
   - what makes the offer different
   - its own section and image
   - real flowing text, not bullets only
4. **Services / offers**
   - concrete description of what the customer gets
   - at least three subpoints with real text
   - no lazy card grid as the default answer
5. **Image-led proof section**
   - at least three to four real customer photos
   - images dominate, text supports
   - avoid a neat same-size grid
6. **Trust / locality**
   - why this provider, not another
   - address, opening hours, personal anchor
   - optional quote or named owner touchpoint
7. **Contact**
   - form or direct contact details prominently visible
   - low-friction language
   - phone, email, and address all visible

Depth requirements:
- every section needs real content, not placeholders
- each section needs a clear headline
- most sections need two to four sentences of real text
- every section needs a visual element
- distribute real customer photos across the full page, not only in the hero
- target at least six to eight real photos across the page

## Multi-variant pitfalls
1. Do not build three variants from one skeleton and recolor them.
2. Do not let all three hero layouts share the same image mass and copy block behavior.
3. Use finished-result imagery in the hero when the business sells completed spaces.
4. Do not let a dark premium direction collapse into a tiled card showroom.
5. Keep project-gallery teasers restrained when a dedicated project page exists.
6. Do not replace real project imagery with mood images that feel less credible.
7. Do not abandon a strong original section order just because the redesign is visually bolder.
8. Do not let anti-grid styling destroy scroll logic or customer comprehension.
9. Do not leave the contact area as an afterthought after all visual energy is spent above.
10. Do not sign off until all three lanes survive the same polish, audit, and browser checks.
