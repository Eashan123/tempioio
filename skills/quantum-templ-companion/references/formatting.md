# Formatting Specifications

## Fonts

| Element | Font | Size | Style | Colour |
|---------|------|------|-------|--------|
| Body text | Georgia | 11pt | Regular | Black |
| Section titles | Georgia | 18pt | Bold, UPPERCASE | #2C3E50 |
| Sub-headings | Georgia | 13pt | Bold | #34495E |
| Subtitles/taglines | Georgia | 12pt | Italic | #5D6D7E |
| Footer | Arial | 8pt | Regular | #888888 |
| Header | Arial | 9pt | Regular | #888888 |

## Colours

| Use | Hex Code | Description |
|-----|----------|-------------|
| Dark text/headers | #2C3E50 | Primary headings |
| Medium text/subheads | #34495E | Secondary headings |
| Light text/taglines | #5D6D7E | Subtitles, notes |
| Accent/footer | #888888 | Footer, header text |
| Table header background | #2C3E50 | White text on dark |
| Table border | #CCCCCC | Light grey borders |
| Link placeholders | #0066CC | Blue, bold |
| Placeholder box background | #F5F5F5 | Light grey fill |

## Page Layout

- **Page size:** US Letter (8.5" x 11")
- **Margins:** 1 inch all sides
- **Header:** "GATE [X]: [SUBTITLE]" right-aligned, grey (#888888)
- **Footer:** "CIRCLEX CODEX™ · THE QUANTUM TEMPL™    THEQUANTUMTEMPL.AU/" left-aligned, grey

## Tables

- Light grey borders (#CCCCCC), 1pt
- Header row: dark background (#2C3E50), white bold text
- Body rows: white background, regular text
- Cell padding: comfortable (100 DXA top/bottom, 120 DXA left/right)
- Always include relevant columns: Item, Purpose, Cost Range, Quality Signals, Link

## Technical Specifications (docx-js)

```javascript
// Page size in DXA (1440 DXA = 1 inch)
page: { 
  size: { width: 12240, height: 15840 },
  margin: { top: 1440, right: 1440, bottom: 1440, left: 1440 }
}

// Table settings
width: { size: 100, type: WidthType.PERCENTAGE }
shading: { fill: "2C3E50", type: ShadingType.CLEAR }  // Use CLEAR, not SOLID

// Special characters
Trademark: \u2122 (™)
Copyright: \u00A9 (©)
En dash: \u2013 (–)
Em dash: \u2014 (—)
Bullet: \u2022 (•)
Apostrophe: \u2019 (')
Left double quote: \u201C (")
Right double quote: \u201D (")
```

## Numbering

- Bullets: Standard bullet character (•)
- Numbers: Arabic numerals (1. 2. 3.)
- Use docx-js LevelFormat.BULLET and LevelFormat.DECIMAL
