# Homepage Layout - Patagonia-Inspired Design

## Section Order (Top to Bottom)

---

### 1. HERO SECTION (Full Width)
**Image**: Your camping/lakeside sunset image
**Overlay**: Semi-transparent dark overlay for text readability
**Heading**: "Something's Better Than Nothing"
**Subheading**: "Gear for Real Adventurers"
**Button**: "Wear Your Motivation" → Links to /collections/all

**Technical**: Use the existing hero section in `templates/index.json`

---

### 2. FEATURED CONTENT GRID (Like Patagonia's "Things They Carry")
**Section Title**: "Latest Adventures"

**Layout**: 50/50 split
- **Left**: Large lifestyle image (outdoor adventure scene)
- **Right**: Coral/orange background with text overlay
  - **Heading**: "From Trail to Screen"
  - **Body**: "Follow along as we explore the great outdoors, one adventure at a time. Every video is an invitation to get outside."
  - **Button**: "Watch on YouTube" → Links to YouTube channel

---

### 3. PRODUCT COLLECTIONS GRID
**Section Title**: "Shop by Collection"

**Layout**: 4-column grid (responsive to 2 columns on mobile)

**Card 1: Hats & Headwear**
- Image: Trucker hat on outdoor background or lifestyle shot
- Overlay text: "Hats & Headwear"
- Subtext: "Shop"

**Card 2: Apparel**
- Image: Hoodie/t-shirt lifestyle shot
- Overlay text: "Apparel"
- Subtext: "Shop"

**Card 3: Accessories**
- Image: Gear/accessories flat lay
- Overlay text: "Accessories"
- Subtext: "Shop"

**Card 4: Gift Cards**
- Coral/orange background
- Gift card mockup
- Overlay text: "Gift Cards"
- Subtext: "Shop"

---

### 4. FEATURED STORY SECTION (Like Patagonia's "For Our Toughest Customers")
**Full-width image**: Family/group outdoor adventure scene or ShujaaKing in action

**Overlay text (centered or left-aligned)**:
- **Heading**: "For Those Who Adventure Anyway"
- **Body**: "Made for real explorers—not fair-weather followers. Our gear goes where content creators fear to tread."
- **Button**: "Shop the Collection"

---

### 5. ACTIVITY CATEGORIES GRID
**Section Title**: "Explore by Activity"

**Layout**: 3-column grid

**Card 1: Camping**
- Image: Camping/tent scene
- Text overlay: "Camping"
- Links: "Explore" → /collections/camping

**Card 2: Hiking**
- Image: Trail/mountain scene
- Text overlay: "Hiking"
- Links: "Explore" → /collections/hiking

**Card 3: Magnet Fishing**
- Image: Magnet fishing scene (from content)
- Text overlay: "Magnet Fishing"
- Links: "Explore" → /collections/magnet-fishing

---

### 6. LATEST VIDEOS SECTION (Like Patagonia's "Latest Stories")
**Section Title**: "Latest Videos"
**Subheading**: "View All" → Links to YouTube channel

**Layout**: Horizontal scrolling carousel (4-5 visible at a time)

**Video Card Structure**:
- Thumbnail image (from YouTube)
- Video title overlay
- Author: "ShujaaKing"
- Click to open: Links to YouTube video

**Videos to Feature** (manually updated or auto-pulled):
1. Recent camping adventure
2. Hiking/trail video
3. Magnet fishing expedition
4. Travel vlog
5. Gear review/tutorial

---

### 7. NEWSLETTER SIGNUP SECTION
**Background**: Light gray or cream

**Content**:
- **Heading**: "Join the Adventure"
- **Subheading**: "Get updates on new gear, latest videos, and exclusive offers."
- **Email input field**
- **Button**: "Sign Me Up"

---

### 8. BRAND VALUES SECTION (Like Patagonia's Footer Promises)
**Background**: Black (#000000)
**Text**: White

**Layout**: 4-column grid (responsive to 1 column on mobile)

**Column 1:**
- Icon: Video camera or play button
- **Heading**: "We Create Content That Inspires"
- **Body**: "Every video is an invitation to explore."
- **Link**: "Watch Our Journey"

**Column 2:**
- Icon: Mountain or gear
- **Heading**: "We Build Quality Gear"
- **Body**: "Designed for real adventurers, tested in the wild."
- **Link**: "Shop the Collection"

**Column 3:**
- Icon: Tree or nature symbol
- **Heading**: "We Support the Outdoors"
- **Body**: "A portion of proceeds goes to conservation."
- **Link**: "Learn More"

**Column 4:**
- Icon: Checkmark or badge
- **Heading**: "We Encourage Imperfection"
- **Body**: "Because something's better than nothing—always."
- **Link**: "Our Story"

---

## Color Scheme Summary

**Primary Background**: White (#ffffff)
**Accent Color**: Sunset Orange (#E8915B)
**Text**: Dark Teal (#2D4A4A)
**Buttons**: Orange background, white text
**Section Backgrounds**:
- White for product grids
- Light gray/cream for newsletter
- Coral/orange for featured content cards
- Black for brand values

---

## Navigation Structure

**Top Bar** (Black background):
- Left: "Stories" | "Gear Guide" | "Content"
- Center: Logo placeholder
- Right: "Find a Store" (or remove)

**Main Navigation**:
- Featured
- Hats
- Apparel
- Accessories
- Collections (dropdown: Camping, Hiking, Travel, Magnet Fishing)
- About
- YouTube (external link)

**Header Icons** (Right side):
- Search
- Wishlist
- Account
- Cart

---

## Mobile Responsiveness

- Hero: Full width, text centered
- Grids: Convert to 1-2 columns
- Video carousel: Horizontal scroll with snap
- Brand values: Stack vertically

---

## Images Needed

1. Hero camping image (you have this!)
2. Lifestyle shots of products in use
3. Activity category images (camping, hiking, magnet fishing)
4. Featured story full-width image
5. Product collection images
6. Video thumbnails from YouTube

---

## Implementation Notes

- Use Shopify's built-in section blocks for flexibility
- Leverage the Horizon theme's existing grid layouts
- Add custom CSS for Patagonia-style overlays
- Consider using metafields for YouTube video URLs
- Install a YouTube feed app for automated video display (optional)

---

## Next Steps for Full Implementation

1. Create Shopify pages (About, Collections)
2. Add products with adventure-focused descriptions
3. Upload lifestyle photography
4. Configure navigation menus
5. Customize theme sections to match this layout
6. Test mobile responsiveness
7. Add YouTube integration
