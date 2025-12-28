# Brand Values Section + Navigation Structure

## BRAND VALUES SECTION (Patagonia-Style)

### Overview
A black background section with 4 columns showcasing brand promises, inspired by Patagonia's footer value propositions.

### Section Positioning
- Above the main footer
- Full-width section
- Fixed height on desktop, stacked on mobile

---

## Design Specifications

### Background & Styling
- **Background Color**: Black (#000000)
- **Text Color**: White (#FFFFFF)
- **Padding**: 80px top/bottom, 40px left/right
- **Max Width**: 1400px centered

### Layout
- **Desktop**: 4 equal columns
- **Tablet**: 2 columns
- **Mobile**: 1 column (stacked)

---

## Content for Each Column

### Column 1: Content Creation
**Icon**: 🎥 Video camera or play button (simple line icon)

**Heading**: "We Create Content That Inspires"

**Body Text**: "Every video is an invitation to explore. From trail guides to gear reviews, we document real adventures that motivate you to create your own."

**Link**: "Watch Our Journey" → https://youtube.com/@shujaaking

---

### Column 2: Quality Gear
**Icon**: ⛰️ Mountain or backpack (simple line icon)

**Heading**: "We Build Quality Gear"

**Body Text**: "Designed for real adventurers, tested in the wild. If it can't handle the outdoors, it doesn't leave our warehouse."

**Link**: "Shop the Collection" → /collections/all

---

### Column 3: Outdoor Support
**Icon**: 🌲 Tree or nature symbol (simple line icon)

**Heading**: "We Support the Outdoors"

**Body Text**: "A portion of every purchase goes toward conservation efforts. When you gear up, you're giving back to the trails, rivers, and wild places we all love."

**Link**: "Learn More" → /pages/conservation

---

### Column 4: Philosophy
**Icon**: ✓ Checkmark or compass (simple line icon)

**Heading**: "We Encourage Imperfection"

**Body Text**: "Because something's better than nothing—always. Start messy. Adventure anyway. The perfect trip is the one you actually take."

**Link**: "Our Story" → /pages/about

---

## Implementation Code

### Shopify Section: `sections/brand-values.liquid`

```liquid
<div class="brand-values-section">
  <div class="page-width">
    <div class="values-grid">

      {%- comment -%} Column 1: Content {%- endcomment -%}
      <div class="value-column">
        <div class="value-icon">
          <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
            <rect x="2" y="2" width="20" height="20" rx="2"/>
            <polygon points="10 8 16 12 10 16 10 8"/>
          </svg>
        </div>
        <h3 class="value-heading">We Create Content That Inspires</h3>
        <p class="value-text">Every video is an invitation to explore. From trail guides to gear reviews, we document real adventures that motivate you to create your own.</p>
        <a href="https://youtube.com/@shujaaking" class="value-link" target="_blank">
          Watch Our Journey
        </a>
      </div>

      {%- comment -%} Column 2: Quality {%- endcomment -%}
      <div class="value-column">
        <div class="value-icon">
          <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
            <path d="M3 21l18-9L3 3v7l13 2-13 2z"/>
          </svg>
        </div>
        <h3 class="value-heading">We Build Quality Gear</h3>
        <p class="value-text">Designed for real adventurers, tested in the wild. If it can't handle the outdoors, it doesn't leave our warehouse.</p>
        <a href="/collections/all" class="value-link">
          Shop the Collection
        </a>
      </div>

      {%- comment -%} Column 3: Outdoors {%- endcomment -%}
      <div class="value-column">
        <div class="value-icon">
          <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
            <path d="M12 2L2 7l10 5 10-5-10-5z"/>
            <path d="M2 17l10 5 10-5M2 12l10 5 10-5"/>
          </svg>
        </div>
        <h3 class="value-heading">We Support the Outdoors</h3>
        <p class="value-text">A portion of every purchase goes toward conservation efforts. When you gear up, you're giving back to the trails, rivers, and wild places we all love.</p>
        <a href="/pages/conservation" class="value-link">
          Learn More
        </a>
      </div>

      {%- comment -%} Column 4: Philosophy {%- endcomment -%}
      <div class="value-column">
        <div class="value-icon">
          <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
            <polyline points="20 6 9 17 4 12"/>
          </svg>
        </div>
        <h3 class="value-heading">We Encourage Imperfection</h3>
        <p class="value-text">Because something's better than nothing—always. Start messy. Adventure anyway. The perfect trip is the one you actually take.</p>
        <a href="/pages/about" class="value-link">
          Our Story
        </a>
      </div>

    </div>
  </div>
</div>

{% schema %}
{
  "name": "Brand Values",
  "settings": [],
  "presets": [
    {
      "name": "Brand Values"
    }
  ]
}
{% endschema %}
```

### CSS Styling

```css
/* Brand Values Section */
.brand-values-section {
  background: #000000;
  padding: 80px 40px;
  color: #ffffff;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 60px;
  max-width: 1400px;
  margin: 0 auto;
}

.value-column {
  text-align: left;
}

.value-icon {
  margin-bottom: 24px;
  opacity: 0.9;
}

.value-icon svg {
  width: 48px;
  height: 48px;
}

.value-heading {
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 16px;
  line-height: 1.3;
}

.value-text {
  font-size: 15px;
  line-height: 1.6;
  opacity: 0.9;
  margin-bottom: 20px;
}

.value-link {
  color: #E8915B;
  text-decoration: none;
  font-size: 15px;
  font-weight: 500;
  display: inline-flex;
  align-items: center;
  transition: color 0.2s;
}

.value-link:hover {
  color: #D67D47;
  text-decoration: underline;
}

.value-link::after {
  content: '→';
  margin-left: 8px;
  transition: transform 0.2s;
}

.value-link:hover::after {
  transform: translateX(4px);
}

/* Responsive */
@media (max-width: 1024px) {
  .values-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 40px;
  }
}

@media (max-width: 640px) {
  .brand-values-section {
    padding: 60px 20px;
  }

  .values-grid {
    grid-template-columns: 1fr;
    gap: 48px;
  }

  .value-column {
    text-align: center;
  }

  .value-icon {
    display: flex;
    justify-content: center;
  }
}
```

---

## NAVIGATION STRUCTURE

### Top Utility Bar (Black Background)
**Optional** - Can be added for promotions/announcements

**Left Side**:
- "Stories" → /blogs/adventures or YouTube
- "Gear Guide" → /pages/gear-guide
- "Content" → YouTube channel

**Center**:
- Promotional message (e.g., "Free Shipping on Orders $50+")

**Right Side**:
- Social media icons (YouTube, TikTok, Instagram)
- "Contact" → /pages/contact

---

### Main Navigation Header

**Logo Position**: Left or Center
- "Something's Better Than Nothing" wordmark or icon logo

**Main Menu Items** (Center or Right):

1. **Featured** → /collections/featured
   - No dropdown

2. **Hats** → /collections/hats
   - No dropdown

3. **Apparel** → /collections/apparel
   - Dropdown:
     - Hoodies
     - T-Shirts
     - Long Sleeves

4. **Accessories** → /collections/accessories
   - No dropdown

5. **Collections** → Mega menu dropdown:
   - By Activity:
     - Camping
     - Hiking
     - Magnet Fishing
     - Travel
   - By Type:
     - New Arrivals
     - Best Sellers
     - Sale Items

6. **About** → /pages/about
   - Dropdown:
     - Our Story
     - Conservation
     - Content Creator

7. **YouTube** 🔗 → https://youtube.com/@shujaaking
   - External link (opens in new tab)
   - Icon: Small YouTube play button

**Header Icons** (Far Right):
- 🔍 Search
- ❤️ Wishlist (optional)
- 👤 Account
- 🛒 Cart (with item count badge)

---

### Footer Navigation

### Footer Column 1: Shop
- Hats
- Apparel
- Accessories
- Gift Cards
- All Products

### Footer Column 2: Explore
- About Us
- Our Story
- Conservation
- Latest Adventures
- Contact

### Footer Column 3: Follow
- YouTube
- TikTok
- Instagram
- Facebook
- Snapchat

### Footer Column 4: Support
- FAQ
- Shipping & Returns
- Size Guide
- Track Order
- Contact Us

### Footer Bottom
- © 2025 Something's Better Than Nothing
- Privacy Policy
- Terms of Service
- Refund Policy
- Built with Shopify

---

## Mobile Navigation

### Hamburger Menu Structure
```
┌─ Home
├─ Shop
│  ├─ Hats
│  ├─ Apparel
│  └─ Accessories
├─ Collections
│  ├─ Camping
│  ├─ Hiking
│  ├─ Magnet Fishing
│  └─ Travel
├─ About
├─ YouTube ↗
└─ Contact
```

**Search Bar**: At top of mobile menu
**Social Icons**: At bottom of mobile menu

---

## Menu Configuration in Shopify

### How to Set Up (Admin → Navigation)

**Main Menu**:
1. Create menu called "Main Menu"
2. Add items in this order:
   - Featured → /collections/featured
   - Hats → /collections/hats
   - Apparel → /collections/apparel
   - Accessories → /collections/accessories
   - Collections (parent item)
     - Add nested items under it
   - About → /pages/about
   - YouTube → https://youtube.com/@shujaaking

**Footer Menu - Shop**:
- Hats → /collections/hats
- Apparel → /collections/apparel
- Accessories → /collections/accessories
- Gift Cards → /products/gift-card
- All Products → /collections/all

**Footer Menu - Explore**:
- About Us → /pages/about
- Conservation → /pages/conservation
- Latest Adventures → https://youtube.com/@shujaaking
- Contact → /pages/contact

**Footer Menu - Follow**:
- YouTube → https://youtube.com/@shujaaking
- TikTok → https://www.tiktok.com/@shujaa.kinggg
- Instagram → https://www.instagram.com/shujaa.king
- Facebook → https://www.facebook.com/share/1BaE2kjjin/
- Snapchat → https://snapchat.com/t/a8U7iBA3

---

## Pages to Create

1. **/pages/about** - About page (content already written)
2. **/pages/conservation** - Conservation/giving back info
3. **/pages/contact** - Contact form
4. **/pages/gear-guide** - Recommended gear lists
5. **/pages/size-guide** - Sizing information
6. **/pages/faq** - Frequently asked questions

---

## Social Media Integration

**Add social icons to:**
- Top utility bar
- Footer
- Product pages ("Share on social")
- About page

**Platforms to link:**
- YouTube (primary)
- TikTok
- Instagram
- Facebook
- Snapchat
