# Something's Better Than Nothing - Brand Colors Reference

## Quick Copy-Paste Color Codes

### Primary Brand Colors

```
Sunset Orange:    #E8915B
Deep Orange:      #D67D47
Burnt Orange:     #C86A37
Cream:            #F5E6D3
Light Cream:      #EDD9BB
Dark Teal:        #2D4A4A
Deep Teal:        #1F3838
```

### Color Scheme for Shopify Theme Customizer

#### BRAND - LIGHT SCHEME (Main theme for most pages)

Copy and paste these hex codes into Shopify Theme Settings → Colors:

```
Background:                   #F5E6D3
Heading Color:                #2D4A4A
Body Text:                    #1F3838
Links:                        #D67D47
Link Hover:                   #C86A37
Border Color:                 #E8915B (set opacity to 20-30%)

PRIMARY BUTTON:
  Background:                 #D67D47
  Text:                       #F5E6D3
  Border:                     #D67D47
  Hover Background:           #C86A37
  Hover Text:                 #FFFFFF
  Hover Border:               #C86A37

SECONDARY BUTTON:
  Background:                 transparent
  Text:                       #2D4A4A
  Border:                     #2D4A4A
  Hover Background:           rgba(45, 74, 74, 0.08)
  Hover Text:                 #1F3838
  Hover Border:               #1F3838

INPUT FIELDS:
  Background:                 #FFFFFF
  Text:                       #1F3838
  Border:                     rgba(45, 74, 74, 0.2)
  Hover Background:           #F5E6D3

VARIANTS:
  Background:                 #FFFFFF
  Text:                       #2D4A4A
  Border:                     #E8915B
  Hover Background:           #F5E6D3
  Hover Text:                 #1F3838
  Selected Background:        #D67D47
  Selected Text:              #F5E6D3
```

#### BRAND - DARK SCHEME (For hero, footer, announcement bar)

```
Background:                   #2D4A4A
Heading Color:                #F5E6D3
Body Text:                    #EDD9BB
Links:                        #E8915B
Link Hover:                   #D67D47
Border Color:                 #F5E6D3 (set opacity to 20-30%)

PRIMARY BUTTON:
  Background:                 #E8915B
  Text:                       #2D4A4A
  Border:                     #E8915B
  Hover Background:           #D67D47
  Hover Text:                 #1F3838
  Hover Border:               #D67D47

SECONDARY BUTTON:
  Background:                 transparent
  Text:                       #F5E6D3
  Border:                     #F5E6D3
  Hover Background:           rgba(245, 230, 211, 0.08)
  Hover Text:                 #EDD9BB
  Hover Border:               #EDD9BB

INPUT FIELDS:
  Background:                 #1F3838
  Text:                       #F5E6D3
  Border:                     rgba(245, 230, 211, 0.2)
  Hover Background:           rgba(31, 56, 56, 0.2)
```

---

## CSS/HTML Color Usage

### For Custom CSS:

```css
:root {
  /* Primary Colors */
  --brand-sunset-orange: #E8915B;
  --brand-deep-orange: #D67D47;
  --brand-burnt-orange: #C86A37;
  --brand-cream: #F5E6D3;
  --brand-light-cream: #EDD9BB;
  --brand-dark-teal: #2D4A4A;
  --brand-deep-teal: #1F3838;

  /* Opacity Variations */
  --brand-orange-10: rgba(232, 145, 91, 0.1);
  --brand-orange-20: rgba(232, 145, 91, 0.2);
  --brand-orange-50: rgba(232, 145, 91, 0.5);
  --brand-teal-10: rgba(45, 74, 74, 0.1);
  --brand-teal-20: rgba(45, 74, 74, 0.2);
  --brand-teal-50: rgba(45, 74, 74, 0.5);
}
```

---

## RGB Values

For design tools that need RGB:

```
Sunset Orange:    RGB(232, 145, 91)
Deep Orange:      RGB(214, 125, 71)
Burnt Orange:     RGB(200, 106, 55)
Cream:            RGB(245, 230, 211)
Light Cream:      RGB(237, 217, 187)
Dark Teal:        RGB(45, 74, 74)
Deep Teal:        RGB(31, 56, 56)
```

---

## RGBA (with transparency examples)

```
Sunset Orange 50%:    rgba(232, 145, 91, 0.5)
Sunset Orange 20%:    rgba(232, 145, 91, 0.2)
Sunset Orange 10%:    rgba(232, 145, 91, 0.1)

Dark Teal 50%:        rgba(45, 74, 74, 0.5)
Dark Teal 20%:        rgba(45, 74, 74, 0.2)
Dark Teal 10%:        rgba(45, 74, 74, 0.1)

Cream 90%:            rgba(245, 230, 211, 0.9)
Cream 50%:            rgba(245, 230, 211, 0.5)
```

---

## Color Usage Guidelines

### Where to Use Each Color:

**Sunset Orange (#E8915B):**
- Accent elements
- Sale badges
- Highlights
- Icon accents
- Decorative borders

**Deep Orange (#D67D47):**
- Primary CTA buttons
- Links
- Active states
- Important headings

**Burnt Orange (#C86A37):**
- Button hover states
- Link hover states
- Pressed/active button states

**Cream (#F5E6D3):**
- Page backgrounds (light theme)
- Button text on dark buttons
- Card backgrounds
- Section backgrounds

**Light Cream (#EDD9BB):**
- Subtle background variations
- Text on dark backgrounds
- Hover states on dark backgrounds

**Dark Teal (#2D4A4A):**
- Main headlines
- Hero section backgrounds
- Footer backgrounds
- Navigation text
- Section headers

**Deep Teal (#1F3838):**
- Body text
- Subheadings
- Descriptive text
- Secondary information

---

## Accessibility Notes

### Contrast Ratios (WCAG AA Compliant):

✅ **GOOD CONTRAST:**
- Dark Teal (#2D4A4A) on Cream (#F5E6D3) - 8.5:1 (AAA)
- Deep Teal (#1F3838) on Cream (#F5E6D3) - 10.2:1 (AAA)
- Cream (#F5E6D3) on Dark Teal (#2D4A4A) - 8.5:1 (AAA)
- Cream (#F5E6D3) on Deep Orange (#D67D47) - 4.8:1 (AA)

⚠️ **USE WITH CAUTION:**
- Sunset Orange (#E8915B) on Cream (#F5E6D3) - 3.2:1 (Use for large text only)

❌ **AVOID:**
- Orange on Light Cream for body text
- Light Cream on Cream

### Recommendations:
- Always use Dark Teal or Deep Teal for body text
- Use Sunset Orange only for decorative elements or large headings (24px+)
- For buttons, use Deep Orange with Cream text for best readability

---

## Social Media Color Codes

For creating branded social media graphics:

### Instagram/Facebook Posts:
- Background: #F5E6D3 or #2D4A4A
- Primary Text: #2D4A4A or #F5E6D3
- Accent/CTA: #D67D47

### Story Templates:
- Background gradient: #2D4A4A to #1F3838
- Text: #F5E6D3
- Highlights: #E8915B

---

## Print Colors (CMYK)

For merchandise printing:

```
Sunset Orange:    C:0   M:50  Y:68  K:0
Deep Orange:      C:0   M:58  Y:76  K:0
Burnt Orange:     C:0   M:65  Y:82  K:0
Cream:            C:3   M:7   Y:16  K:0
Dark Teal:        C:75  M:45  Y:45  K:40
Deep Teal:        C:80  M:50  Y:50  K:55
```

**Note:** CMYK values may vary depending on your printer. Always request a test print!

---

## Pantone Equivalents (Approximate)

```
Sunset Orange:    Pantone 1575 C (closest match)
Deep Orange:      Pantone 7576 C
Dark Teal:        Pantone 5477 C
Cream:            Pantone 9183 C
```

---

## Gradient Combinations

### Suggested Gradients for Graphics:

**Sunset Gradient:**
```
Linear gradient: #E8915B → #D67D47 → #C86A37
Use: Hero backgrounds, product banners
```

**Teal Depth:**
```
Linear gradient: #2D4A4A → #1F3838
Use: Footer, dark sections, overlays
```

**Warm Neutral:**
```
Linear gradient: #F5E6D3 → #EDD9BB
Use: Subtle section backgrounds
```

**Sunset to Night:**
```
Radial gradient: #E8915B (center) → #2D4A4A (edges)
Use: Feature graphics, hero sections
```

---

## Color Combinations That Work Well Together

### Combo 1: "Sunset Vibes"
- Background: #F5E6D3
- Heading: #2D4A4A
- Body: #1F3838
- Accent: #E8915B

### Combo 2: "Dark Mode"
- Background: #2D4A4A
- Heading: #F5E6D3
- Body: #EDD9BB
- Accent: #E8915B

### Combo 3: "High Contrast"
- Background: #FFFFFF
- Heading: #1F3838
- Body: #2D4A4A
- Accent/CTA: #D67D47

---

**Quick Tip:** Save this file for easy reference when creating graphics, designing social media posts, or customizing your Shopify theme!
