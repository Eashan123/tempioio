# Placeholder Conventions

## Affiliate Link Placeholders

### Types

| Placeholder | Use |
|-------------|-----|
| `[AFFILIATE LINK: Product Name]` | Individual product links |
| `[KIT LINK: Kit Name]` | Complete kits on Kit.co |
| `[EXTERNAL LINK: Description]` | Non-affiliate links (calendars, references) |

### Examples

```
[AFFILIATE LINK: Quality Brass Diya]
[AFFILIATE LINK: Copper Sri Yantra]
[AFFILIATE LINK: Certified 5 Mukha Mala]

[KIT LINK: Complete Starter Kit]
[KIT LINK: Practitioner Kit]
[KIT LINK: Lakshmi Abundance Set]

[EXTERNAL LINK: 2025 Lunar Calendar]
[EXTERNAL LINK: Moon Phase Calculator]
```

### Formatting in Document

- Blue text (#0066CC)
- Bold
- On its own line after the relevant item or table

## Visual Placeholders

### Types

| Placeholder | Use | Suggested Size |
|-------------|-----|----------------|
| `[IMAGE: Description]` | Photos, product shots, comparisons | 2"x2" to 4"x2" |
| `[DIAGRAM: Description]` | Layouts, spatial arrangements | Full width x 3" |
| `[INFOGRAPHIC: Description]` | Charts, visual summaries | Full width x 4" |

### Examples

```
[IMAGE: Quality brass diya vs cheap clay diya comparison]
[IMAGE: Authentic rudraksha bead showing mukha lines]
[IMAGE: Example of properly set up altar]

[DIAGRAM: Altar layout — deity centre, diya southeast, yantra front, practitioner facing east]
[DIAGRAM: Ancestral altar arrangement with photo placement]
[DIAGRAM: Directional setup for element work]

[INFOGRAPHIC: Lunar phase chart — New Moon to Full Moon with work types]
[INFOGRAPHIC: Day of week correspondences with planetary rulers]
[INFOGRAPHIC: The eight gates overview wheel]
```

### Formatting in Document

Create a bordered box:
- Border: 1pt grey (#CCCCCC)
- Background: Light grey (#F5F5F5)
- Text: Blue (#0066CC), bold
- Padding: Comfortable internal margins
- Size: Based on type (see table above)

### Placement Guidelines

**Images:**
- After introducing an item that benefits from visual reference
- In product comparison sections
- Near quality signal descriptions

**Diagrams:**
- In setup/arrangement sections
- Where spatial relationships matter
- For directional or positional work

**Infographics:**
- For timing references (lunar, daily)
- For system overviews
- For quick reference charts readers will return to

## Implementation in docx-js

```javascript
// Create a placeholder box
const createPlaceholderBox = (text, type = "IMAGE") => {
  return new Table({
    width: { size: 100, type: WidthType.PERCENTAGE },
    rows: [
      new TableRow({
        children: [
          new TableCell({
            borders: {
              top: { style: BorderStyle.SINGLE, size: 1, color: "CCCCCC" },
              bottom: { style: BorderStyle.SINGLE, size: 1, color: "CCCCCC" },
              left: { style: BorderStyle.SINGLE, size: 1, color: "CCCCCC" },
              right: { style: BorderStyle.SINGLE, size: 1, color: "CCCCCC" }
            },
            shading: { fill: "F5F5F5", type: ShadingType.CLEAR },
            margins: { top: 200, bottom: 200, left: 200, right: 200 },
            children: [
              new Paragraph({
                alignment: AlignmentType.CENTER,
                children: [
                  new TextRun({ 
                    text: `[${type}: ${text}]`, 
                    bold: true, 
                    color: "0066CC",
                    font: "Georgia",
                    size: 22
                  })
                ]
              })
            ]
          })
        ]
      })
    ]
  });
};
```
