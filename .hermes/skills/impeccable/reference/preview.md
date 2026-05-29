Use this command when the user wants a three-variant website preview for a local business, especially trades and service businesses, with a comparison canvas and a clean selection flow.

Load before execution:
- `references/local-business.md`
- `references/design-brief-collage-workflow.md`
- `references/subpath-safe-canvas-selection-flow.md`
- `references/local-business-multi-variant-preview-checks.md`
- `references/dark-variant-polish.md` when any lane is dark or cinematic

This command is the full WebsiteUpgrade-style preview workflow inside Impeccable. It produces three clearly different directions, three crafted variants, one customer-facing canvas, and a working preview selection endpoint.

## Required Workflow

### 0. Inheritance Map before build
Before shape or craft on an existing local-business site, write down the inheritance map from the source site or supplied screenshot set. Do this before you start inventing layout improvements.

Required fields:
- original hero principle
- original image family
- original section order
- lead project or proof section
- what stays
- what may change
- what must not be diluted

Interpret them literally:
- **Original hero principle**: full-bleed vs boxed, image-led vs text-led, material detail vs finished-result image, overlay density, CTA placement relative to the image.
- **Original image family**: the trust-bearing type of photo the business already uses successfully.
- **Original section order**: the core homepage acts that currently guide the customer.
- **Lead project or proof section**: the one named project or standout proof block that carries disproportionate trust weight.
- **What stays**: the structural moves that must survive the redesign.
- **What may change**: visual system, spacing, typography, or sequence changes that do not break the original conversion logic.
- **What must not be diluted**: the parts that would make the rebuild feel generic or disconnected from the real business if weakened.

Do not proceed into build until this map is explicit.

### 1. Shape three real directions
Run shape three times, once per direction.

For rebuilds where the user wants deliberate review gates, execute the workflow step by step:
- shape Direction A, report only that result, then wait for confirmation
- shape Direction B, report only that result, then wait for confirmation
- shape Direction C, report only that result, then wait for confirmation
- build one Design-Brief-Collage per confirmed direction from real project material, save it immediately into the project tree, send it, then wait again
- before each craft pass, restate how the variant will satisfy the visual rules, build only that one variant, report the live URL, then wait

Do not batch multiple shape, collage, or craft phases into one response when the user explicitly asks for gated review.

If the user later explicitly removes those gates, switch to an uninterrupted production run: craft A, then B, then C, verify each live page, send a screenshot after each one, then rebuild and verify the canvas in the same run.

Each direction needs its own visual premise, not just a variant label. A good direction brief should state:
- what the concept feels like
- what the page is trying to signal to the customer
- what kind of business personality it fits
- how the layout and density should behave
- what makes it clearly different from the other two

Useful direction patterns include:
- warm and local, with a human, hand-made feel
- premium and editorial, with calm confidence
- practical and conversion-first, with very direct structure

Do not let all three briefs converge toward the same center.

### 2. Build one Design-Brief-Collage per direction
For each confirmed shape brief, build one Design-Brief-Collage from real project material.

Do not generate stock-photo probes for this workflow.

The collage is the visual contract for craft and should lock:
- the real image source from the customer project
- composition pressure and image dominance
- type energy and typographic voice
- color accent and tonal direction
- anti-goals as visible text inside the image
- character words that define the direction

Each direction gets its own collage. Do not reuse one collage across all three unless the user explicitly asked for that.

Use only project-grounded material:
- uploaded customer photos
- logo or wordmark assets
- screenshots from the current or existing site
- reference imagery explicitly present in PRODUCT.md or DESIGN.md
- if necessary, a screenshot from a reference URL already named in the brief

Never use generated stock-photo placeholders or generic people imagery.

The collage should be a wide horizontal image, roughly 1400×600px, with overlapping elements and visible attitude, not a spaced-out moodboard grid. It should make the direction legible to a customer at a glance.

When the user is pressure-testing visual structure only, keep the collage discussion focused on what the eye sees: hierarchy, typography character, image use, anti-goals, accent, and compositional force. Do not drift into copy critique unless the user explicitly asks for it.

### Pflicht vor jedem craft-Pass — Context Compaction Guard
Lade folgende Dateien neu bevor du mit craft beginnst.
Nicht aus dem Gedächtnis arbeiten — Context Compaction
kann frühere Ladungen abschwächen oder löschen.

Neu laden:
- impeccable SKILL.md
- reference/preview.md
- references/local-business.md
- references/dark-variant-polish.md
- PRODUCT.md
- DESIGN.md des aktuellen Projekts

Erst wenn alle sechs frisch geladen sind: craft starten.

### 3. Craft three variants
Run craft three times, once per shaped direction.

For each variant, build mobile first and derive the larger breakpoints from that composition.

Do not solve the desktop hero first and then try to compress it onto a phone. For local-business previews this creates the exact failure pattern we do not want: decent desktop screenshots and compromised mobile reality. Start at phone width, lock hierarchy and CTA clarity there, then scale outward to tablet and desktop.

Reason:
- roughly 62% of global page views happen on mobile
- local-business traffic is often even more phone-heavy
- if the page feels convincing on a phone, the later desktop pass becomes refinement instead of rescue

Each variant must be built against its own brief and its own Design-Brief-Collage:
- variant A follows direction A
- variant B follows direction B
- variant C follows direction C

Keep the content and business facts aligned, but let the visual systems diverge clearly.

Treat the collage as a layout, tone, and material instruction, not as decoration and not as a loose moodboard. During craft, explicitly translate the direction collage into the page by deciding:
- what the core composition is
- what material language is visible in surfaces, borders, shadows, framing, and image treatment
- what typography energy it implies
- what spacing rhythm it implies
- what should be removed from the default landing-page pattern so the variant does not collapse back into the same shell

Before writing code, extract and name at least these five translation targets per direction:
- composition pattern
- material language
- type energy
- spacing rhythm
- CTA behavior

If three direction collages exist but the three crafted pages still share the same underlying layout shell, the craft phase failed and must be redone before polish.

### 3.5 CLI Auto-Detect before critic

After each craft pass completes and before calling the critic sub-agent, run the Impeccable CLI detector on the built HTML file:

```bash
npx impeccable detect [variant-file].html --json
```

Parse the JSON output and fix critical findings immediately. Do not send a file to critic that the CLI already flagged as broken.

**Auto-fix rules — apply in this order:**

1. **Low contrast under 4.5:1**
   - Find the flagged color pair in CSS
   - Darken text or lighten background until ratio ≥ 4.5:1
   - Re-test with the CLI to confirm

2. **Overused fonts (Inter, Roboto, Arial, Helvetica)**
   - Replace with a project-appropriate alternative from DESIGN.md
   - If no alternative is defined, pick one: DM Sans, Source Sans 3, Work Sans, or a local-business-appropriate webfont
   - Never leave the page with Inter or Roboto as the primary face

3. **Skipped headings (h1 → h3, h2 → h4, etc.)**
   - Insert the missing heading level or re-level the hierarchy
   - h1 → h2 → h3 → h4 must be sequential
   - No skips for screen-reader navigation

4. **All-caps body text over 30 characters**
   - Convert to sentence case or title case
   - Reserve uppercase for short labels (< 15 chars) and buttons only

5. **Hero eyebrow chips**
   - Remove the tracked-caps pill or tiny label above the h1
   - Integrate the kicker into the headline, or drop it entirely
   - No "eyebrow" pattern above hero headlines

**Workflow:**
1. Run `npx impeccable detect [file] --json`
2. Parse findings array
3. If any critical finding matches the five rules above → fix it
4. Re-run detect to verify the fix
5. Only when detect returns clean (or only non-critical warnings) → proceed to critic

**Non-critical warnings** (do not block, but note for polish):
- Layout transition warnings (padding/margin animations)
- Minor spacing suggestions
- Non-hero eyebrow labels

### 3.6 Sub-Agenten-Prüfung nach jeder Sektion

Nach jeder fertiggestellten Sektion oder Komponente (Hero, Services, Trust, Prozess, Kontakt, Footer):

1. **critic Sub-Agent starten**
   - Lade `agents/critic/AGENT.md`
   - Übergib die fertige Sektion zur Prüfung
   - Warte auf PASS oder FAIL

2. **Bei PASS:**
   - Weiter mit der nächsten Sektion

3. **Bei FAIL:**
   - Notiere den Fehler konkret
   - Repariere die Sektion
   - Sende erneut an critic
   - Max. 2 Reparaturversuche pro Sektion

4. **Nach 2 Fails in Folge:**
   - Stoppe den Build
   - Informiere Markus (watchi) mit:
     - Welche Sektion betroffen ist
     - Was der critic bemängelt hat
     - Was bereits versucht wurde
   - Warte auf Entscheidung vor dem Weitermachen

**critic prüft gegen:**
- Strukturelle Anti-Patterns (5 Template-Fallen)
- Inhaltliche Qualität (kein AI-Sprech, keine Platzhalter)
- Visuelle Konsistenz (Farben, Typo, Abstände)
- Technische Sauberkeit (keine Konsole-Fehler, responsive)
- Local-Business-Konformität (Impressum, tel:-Links, Adresse)

### 4. Build the comparison canvas
The customer-facing comparison page must show all three variants side by side.

Use the provided canvas template:
`reference/assets/design-canvas.html`

Do not create a new canvas from scratch unless the template is unusable.

The canvas should:
- label each variant clearly
- explain what that variant explores
- show enough of the visual system to compare
- present the choice without making the page feel crowded
- remain readable on the browser sizes used for review
- be refreshed after major variant rewrites so the comparison reflects the current pages, not stale earlier probes

When the underlying variants changed materially during a fix pass, prefer live previews of the actual variant pages in the canvas over static design-brief collages alone. Collages are still useful for explaining the concept, but the customer-facing comparison must not drift away from the real current variants.

If the craft outputs are delivered as top-level files such as `craft-A.html`, `craft-B.html`, and `craft-C.html` instead of per-variant directories, point the canvas iframe previews and open-links directly at those files. Do not leave stale directory links behind after switching output structure.

The canvas copy must be written for the customer, not for the builder:
- no internal version language like Version17, shape, craft, humanized, or polish pass in visible customer copy
- no meta commentary about what changed in the implementation
- intro copy should directly tell the business owner that this is their preview and that they can compare three directions and choose one
- each variant card should explain the direction in owner language: how it feels, what kind of impression it gives, and when it fits
- helper text should restate the action clearly: open each version, compare calmly, then choose a favorite

If the canvas will be shown to the customer, run a final pass that asks: does this read like a client presentation, or like an internal design review board? If it feels internal, rewrite before delivery.

For deployable previews, make the canvas subpath-safe by default:
- variant links must use project-relative paths
- avoid root-relative paths like `/preview-select.php` when the preview lives under a nested public subpath
- if the page may move between local preview, VPS subpath, and public URL, prefer links and endpoints relative to the canvas file itself
- derive customer or route context from the current URL only as a fallback, not as the primary dependency

### 5. Add `preview-select.php`
The preview must include a way for the customer to send back their selection.

`preview-select.php` should support at minimum:
- chosen variant identifier
- optional comment or feedback
- customer identifier or route context if available
- a confirmation response that the choice was received

Keep the flow simple. The customer should not need to think about the form.

For preview delivery, the safest default is to place `preview-select.php` next to the canvas inside the project directory and post to it with a relative endpoint such as `preview-select.php`. This keeps the selection flow portable across nested public paths.

Recommended persistence pattern:
- append every submission to `data/preview-selections.jsonl` for an audit trail
- write the latest submission to `data/last-selection.json` for quick lookup
- return a machine-readable JSON response so the canvas can confirm success without a page jump

Use the packaged template at `reference/assets/preview-select.php` as the starting point.

### 6. Humanize copy before final polish
When the user asks for anti-AI copy cleanup on preview variants, run it as a scoped pass, not as a blind rewrite.

Default scope for live preview HTML:
- rewrite only body copy, subcopy, helper text, and form labels
- keep headlines, variant names, and core directional slogans unchanged unless the user explicitly asks to rewrite them
- preserve the variant's intended voice: rough for raw or dark directions, calm for editorial directions, direct for conversion-first directions

What to remove from body copy:
- assembled-sounding sales phrasing
- tidy AI rhythm where every sentence lands the same way
- generic uplift language, vague significance, or marketing fog
- overly polished label text that feels like a form template instead of a person speaking

After the humanizer pass, do one explicit readback check: if the page still contains a sentence that sounds like generic AI website copy, rewrite it again before moving to polish.

### 7. Polish and audit all three
Run polish and audit on every variant, not just the one that looks strongest.

### Structural anti-template audit before polish signoff
Run this as a hard structural audit before you call any preview polished, finished, or ready.

Check all five failure patterns explicitly:
- numbers band or KPI strip
- service card row or equal-tile service system
- three-up project raster or similar mini-gallery teaser
- evenly split three-column trust block
- bright or pasted-on contact ending

If any one of the five is present:
- stop
- do not describe the page as polished or final
- rebuild the structure first
- only return to polish after the structural pattern is gone

Structural cleanup outranks visual cosmetics. Do not tweak spacing, type, or shadows around a failed structure and call that a fix.

Check each of the three for:
- visual polish
- responsive behavior
- accessibility
- keyboard and focus states
- long-copy handling
- image loading and sizing
- layout stability
- browser cleanliness

The weakest variant still needs to be good.

### 8. SEO-Writer nach finalem craft

Nachdem alle drei Varianten gecraftet, gepolished und geprüft sind:

1. **seo-writer Sub-Agent starten**
   - Lade `agents/seo-writer/AGENT.md`
   - Übergib die finale HTML/Text-Inhalte aller drei Varianten
   - Warte auf DONE

2. **seo-writer verarbeitet:**
   - Humanize-Pass: AI-Sprech entfernen, natürliche Sprache einfügen
   - SEO-Optimierung: Keywords, Meta-Daten, Local-SEO-Signale
   - Final Check: Lesbarkeit, Handwerker-Sprache, Kein Marketing-Fog

3. **Nach seo-writer DONE:**
   - Integriere die überarbeiteten Texte in die Varianten
   - Führe einen letzten critic-Pass durch (nur Text-Änderungen)
   - Wenn PASS: Build ist final
   - Wenn FAIL: Repariere und erneut an critic

**Wichtig:** Der seo-writer ändert nur Text-Inhalte, nie HTML-Struktur oder Design.

## Verification Checklist
- [ ] Three directions were shaped separately
- [ ] Each direction has its own Design-Brief-Collage from real project material
- [ ] Three craft passes were built from three different briefs
- [ ] Before coding, each direction was translated into explicit composition, material, type, rhythm, and CTA decisions
- [ ] The three variants are visibly different, not just recolored copies
- [ ] **critic Sub-Agent wurde nach jeder Sektion aufgerufen und hat PASS gegeben**
- [ ] **Bei 2+ FAILs wurde Markus informiert und Entscheidung eingeholt**
- [ ] The canvas uses `reference/assets/design-canvas.html`
- [ ] `preview-select.php` exists and accepts the choice
- [ ] Canvas links and selection endpoint are relative and subpath-safe
- [ ] Public review was verified on the real served URL or subpath, not only localhost or file URLs
- [ ] Polish and audit were run on all three variants
- [ ] **seo-writer Sub-Agent wurde nach finalem craft aufgerufen und Texte sind integriert**
- [ ] Browser checks were completed
- [ ] The result feels like a real customer decision, not an AI variation dump
