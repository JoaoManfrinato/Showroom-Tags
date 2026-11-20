---
type: project
brand: Brazilian Lumber (showroom) — tags for Platinum Woods, Durathermo by Platinum Woods, Deckotech
created: 2026-11-19
---

# [BRL] Showroom Tags

Tool that generates print-ready product tags for the showroom boards.

- **Tool (local):** `Showroom Tag Studio.html`. Open it in Chrome or Safari. It needs internet to load jsPDF, opentype.js and qrcode-generator from CDN. Fonts and logos are embedded.
- **Visual reference:** `~/Desktop/TAGS.pdf` (Durathermo Ash, Platinum Woods Cumaru, Deckotech Royal Teak).

## Print spec
- Arch-top tag, proportions taken from the reference (239.85 × 498.14 pt).
- Default height **15 cm**, which gives a trim of **72.2 × 150 mm**. Other options: 12 / 17.6 (the original layout size) / 20 cm.
- Bleed 3 mm (2 or 5 also available). Crop marks at the corners of the bounding box. A slug line sits outside the trim.
- An optional last page holds the **die line** (magenta CutContour, 0.5 pt), because the shape is not a rectangle.
- All artwork is vector and **CMYK**:
  - Rich black 75/68/67/90 (from the reference)
  - Durathermo Red 5/98/100/0
  - Deckotech Orange 0/84/91/0
- All text is converted to outlines. Montserrat is used for PW and Durathermo, Inter for Deckotech.
- Logos come straight from the vault SVGs:
  - `PLT_Logo_Horizontal_White`
  - `DRT_LOGO_OP1`
  - `Deckotech_Logo_Type` (in orange)
- The Durathermo tag keeps the dark-grey Platinum "P" symbol beside the bullets, as in the reference.
- "Download all species / colors" exports every species (PW / Durathermo) or every colour of the current Deckotech product into one multi-page PDF.

## Tool UI (v2, 2026-11-19)
- The interface is in English and uses the Brazilian Lumber look:
  - green #066938 brand bar with the BRL logo
  - Archivo typeface
  - paper #f3f2ee / ink #0c0c0c
  - accent #39ac52 for focus and selection only
- Light and Dark theme toggle in the header. It follows the system setting until the user picks one, and the choice is remembered per browser.
- Layout:
  - left: numbered build steps (Brand → Product → Profile & size → Applications → Highlights → Warranty & QR)
  - centre: the proof on a cutting-mat grid
  - right: print output (height, bleed, die line, specs, file name, download buttons)
- The BRL branding is on the tool UI only. The generated tag PDFs still carry no Brazilian Lumber name or logo.

## Changes vs. the reference layout
- The content column is re-centred on the tag. In the reference it sits about 3 pt to the right.
- The Deckotech tagline is corrected to "Durability meets design, powered by innovation". The reference spelled it "inovation" and had no comma.
- Added the missing space in "Deckotech® Royal Teak".
- Deckotech bullets now come from the product material. The reference reused the hardwood bullets.
  - WPC: Low maintenance / Splinter-free / Rot & warp resistant
  - Solara: Class A fire rated / Aluminum core / UV stable
  - Ember: Moisture resistant / Mold resistant / Lightweight
- No Brazilian Lumber name or logo appears anywhere in the PDFs, per Platinum Woods brand rules.

## Open points to confirm
- **Deckotech warranty line.** The tag says "25 YEAR WARRANTY · INTERIOR & EXTERIOR". The legal documents say 25 yr *residential* / 15 yr *commercial*, prorated, and the spec sheets say 10 yr (DKT vault, Warranty).
- **Platinum Woods / Durathermo 20-year warranty.** This comes from the reference layout. No source for it was found in the vaults.
- **QR destinations.**
  - platinumwoods.us
  - platinumwoods.us/durathermo
  - deckotech.us

  These are editable per tag. Product-specific landing pages would be better.
- **Deckotech catalogue.** The colour and size lists follow the product photography, which goes beyond the spec sheets. Some examples: Terra decking colours, Prestige White Oak, Ember sizes. The Solara louver list only has the two documented sizes (25×15, 120×30 mm). The others can be typed with "Outro…".
- **Print shop.** Confirm the bleed they want, whether they accept the die line on a separate page or need a spot colour, and the substrate (rigid PVC / foam board).
