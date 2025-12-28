# Navigation Menus Setup Guide
## Something's Better Than Nothing Store

---

## MAIN NAVIGATION (Header Menu)

### Menu Name: `main-menu`

```
HOME
├─ Link: /

SHOP
├─ All Products → /collections/all
├─ New Arrivals → /collections/new-arrivals
├─ Best Sellers → /collections/best-sellers
├─ ──────────── (divider)
├─ Hats & Caps → /collections/hats
├─ T-Shirts → /collections/tshirts
├─ Hoodies & Sweatshirts → /collections/hoodies
├─ Accessories → /collections/accessories
└─ ──────────── (divider)
    └─ Sale → /collections/sale

ABOUT
├─ Link: /pages/about

CONTACT
├─ Link: /pages/contact
```

### Setup Instructions for Shopify:

1. Go to **Online Store → Navigation**
2. Click **Main menu**
3. Add menu items in this order:

**Level 1: HOME**
- Name: `Home`
- Link: `/` (Home page)

**Level 1: SHOP (with dropdown)**
- Name: `Shop`
- Link: `/collections/all`
- Add nested items:
  - `All Products` → `/collections/all`
  - `New Arrivals` → `/collections/new-arrivals`
  - `Best Sellers` → `/collections/best-sellers`
  - `Hats & Caps` → `/collections/hats`
  - `T-Shirts` → `/collections/tshirts`
  - `Hoodies & Sweatshirts` → `/collections/hoodies`
  - `Accessories` → `/collections/accessories`
  - `Sale` → `/collections/sale`

**Level 1: ABOUT**
- Name: `About`
- Link: `/pages/about`

**Level 1: CONTACT**
- Name: `Contact`
- Link: `/pages/contact`

---

## FOOTER MENU

### Footer Column 1: "SHOP"
**Menu Name:** `footer-shop`

```
All Products → /collections/all
New Arrivals → /collections/new-arrivals
Best Sellers → /collections/best-sellers
Hats & Caps → /collections/hats
T-Shirts → /collections/tshirts
Hoodies → /collections/hoodies
Sale → /collections/sale
```

### Footer Column 2: "COMPANY"
**Menu Name:** `footer-company`

```
About Us → /pages/about
Our Story → /pages/our-story
Blog → /blogs/news
Contact → /pages/contact
FAQs → /pages/faq
```

### Footer Column 3: "CUSTOMER SERVICE"
**Menu Name:** `footer-customer-service`

```
Shipping & Returns → /pages/shipping-returns
Size Guide → /pages/size-guide
Track Your Order → /pages/track-order
Privacy Policy → /policies/privacy-policy
Terms of Service → /policies/terms-of-service
Refund Policy → /policies/refund-policy
```

### Footer Column 4: "CONNECT"
**Menu Name:** `footer-social`

```
Instagram → https://instagram.com/yourbrand
Facebook → https://facebook.com/yourbrand
Twitter → https://twitter.com/yourbrand
TikTok → https://tiktok.com/@yourbrand
Pinterest → https://pinterest.com/yourbrand
```

---

## MOBILE MENU (Same as Main Menu)

The mobile menu typically uses the same structure as the main menu but displays differently.

### Mobile Menu Considerations:
- Keep to 2 levels maximum
- Use clear, concise names
- Popular items should be at the top
- Make sure CTA items (like "Sale") are easily accessible

---

## QUICK LINKS MENU (Optional - for promotional banners)

**Menu Name:** `quick-links`

Useful for announcement bars or promotional sections:

```
Free Shipping Over $50 → /pages/shipping
New: Summer Collection → /collections/summer-2024
Limited Edition → /collections/limited-edition
```

---

## ACCOUNT MENU (Customer Account Pages)

**Menu Name:** `account-menu`

```
My Account → /account
Orders → /account#orders
Addresses → /account/addresses
Wishlist → /pages/wishlist (if using wishlist app)
Logout → /account/logout
```

---

## COLLECTIONS TO CREATE

Before setting up navigation, create these collections in Shopify:

### 1. All Products
- **Handle:** `all`
- **Type:** Automated
- **Conditions:** All products

### 2. New Arrivals
- **Handle:** `new-arrivals`
- **Type:** Automated
- **Conditions:**
  - Product tag contains "new"
  - OR Product created date is within last 30 days

### 3. Best Sellers
- **Handle:** `best-sellers`
- **Type:** Manual
- **Note:** Manually add your top-selling products

### 4. Hats & Caps
- **Handle:** `hats`
- **Type:** Automated
- **Conditions:**
  - Product type equals "Hat"
  - OR Product tag contains "hat"

### 5. T-Shirts
- **Handle:** `tshirts`
- **Type:** Automated
- **Conditions:**
  - Product type equals "T-Shirt"
  - OR Product tag contains "tshirt"

### 6. Hoodies & Sweatshirts
- **Handle:** `hoodies`
- **Type:** Automated
- **Conditions:**
  - Product type equals "Hoodie"
  - OR Product tag contains "hoodie" or "sweatshirt"

### 7. Accessories
- **Handle:** `accessories`
- **Type:** Automated
- **Conditions:**
  - Product type equals "Accessory"
  - OR Product tag contains "accessory" or "sticker" or "bag"

### 8. Sale
- **Handle:** `sale`
- **Type:** Automated
- **Conditions:**
  - Compare at price is greater than Price
  - OR Product tag contains "sale"

---

## PAGES TO CREATE

Create these pages before linking them in your navigation:

### 1. About Page
- **Handle:** `about`
- **Template:** `page`
- **Content:** Your brand story, mission, values

### 2. Contact Page
- **Handle:** `contact`
- **Template:** `page.contact`
- **Content:** Contact form, email, social links

### 3. Our Story
- **Handle:** `our-story`
- **Template:** `page`
- **Content:** Detailed brand history, founder story

### 4. FAQ
- **Handle:** `faq`
- **Template:** `page`
- **Content:** Frequently asked questions

### 5. Shipping & Returns
- **Handle:** `shipping-returns`
- **Template:** `page`
- **Content:** Shipping policy, return policy, timelines

### 6. Size Guide
- **Handle:** `size-guide`
- **Template:** `page`
- **Content:** Size charts for hats, shirts, hoodies

### 7. Track Order
- **Handle:** `track-order`
- **Template:** `page`
- **Content:** Order tracking form/instructions

---

## MOBILE MENU BEST PRACTICES

### Recommended Mobile Navigation:

```
🏠 Home
🛍️ Shop
   • All Products
   • New Arrivals
   • Best Sellers
   • Sale
ℹ️ About
✉️ Contact
👤 Account (if logged in)
🛒 Cart
```

Keep it simple - users should be able to find products in 2 taps maximum.

---

## ANNOUNCEMENT BAR SETUP

**Location:** Above header

**Content Ideas:**
- "Free Shipping on Orders $50+ 🚚"
- "New Arrivals: Shop the Latest Drops ✨"
- "Limited Edition Designs Available Now"
- "Use code WELCOME10 for 10% off your first order"

**Links:**
- Link to `/collections/all` or `/collections/new-arrivals`

**Colors:**
- Use "Brand - Dark" color scheme (#2D4A4A background, #F5E6D3 text)

---

## SEARCH FUNCTIONALITY

### Search Configuration:
1. Enable predictive search in theme settings
2. Configure search to include:
   - Product titles
   - Product descriptions
   - Product tags
   - Collection titles
   - Pages
   - Blog posts

### Search Bar Placement:
- Desktop: Header (icon or full search bar)
- Mobile: Hamburger menu or fixed search icon

---

## BREADCRUMBS

Enable breadcrumbs for better navigation:

**Example:**
```
Home > Shop > Hats & Caps > Something's Better Than Nothing Trucker Hat
```

**Benefits:**
- Improves SEO
- Helps users navigate back
- Shows page hierarchy

---

## MEGA MENU (Optional - For Advanced Setup)

If you want a more visual dropdown menu:

### Shop Mega Menu Structure:

```
┌─────────────────────────────────────────────────────────┐
│  SHOP BY CATEGORY    │    FEATURED    │    QUICK LINKS  │
├──────────────────────┼────────────────┼─────────────────┤
│  Hats & Caps         │ [Image]        │  New Arrivals   │
│  T-Shirts            │  Best Seller   │  Best Sellers   │
│  Hoodies             │  Product Name  │  Sale           │
│  Accessories         │  $24.99        │  Gift Cards     │
└──────────────────────┴────────────────┴─────────────────┘
```

---

## STICKY HEADER CONFIGURATION

**Recommended Settings:**
- Enable sticky header on desktop
- Enable sticky header on mobile
- Include: Logo, Main Menu, Search, Cart
- Background: Semi-transparent white with blur effect
- Scroll behavior: Hide on scroll down, show on scroll up

---

## FINAL NAVIGATION CHECKLIST

- [ ] Main menu created with all links
- [ ] Footer menus created (Shop, Company, Customer Service, Social)
- [ ] All collections created and published
- [ ] All pages created and published
- [ ] Links tested (no broken links)
- [ ] Mobile menu tested
- [ ] Search functionality tested
- [ ] Breadcrumbs enabled
- [ ] Announcement bar configured
- [ ] Account menu configured
- [ ] Cart icon visible and functional
- [ ] All menu items have proper capitalization
- [ ] Dropdown menus work properly
- [ ] Footer social links updated with your actual URLs

---

**Pro Tip:** Test your navigation on mobile devices to ensure everything is easily accessible with one thumb!
