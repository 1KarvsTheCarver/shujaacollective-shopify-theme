# Latest Adventures - Video Section Implementation Guide

## Overview
This section displays ShujaaKing's latest YouTube videos in a Patagonia-style horizontal scrolling carousel, similar to their "Latest Stories" section.

---

## Section Design

### Position on Homepage
After the "Activity Categories Grid" and before the "Newsletter Signup"

### Section Header
**Title**: "Latest Adventures"
**Subtitle**: "From trail to screen—follow the journey"
**Link**: "View All on YouTube" → https://youtube.com/@shujaaking

---

## Layout Structure

### Desktop View
- Horizontal scrolling carousel
- 4 videos visible at once
- Left/right arrow navigation
- Smooth scroll animation
- Cards are equal width with small gap between

### Mobile View
- Horizontal scroll (swipe)
- 1.5 videos visible (shows partial next card)
- No arrows, touch-based scrolling
- Snap to card on scroll

---

## Video Card Design

### Card Dimensions
- Width: 300px (desktop), 85vw (mobile)
- Height: Auto (maintains 16:9 ratio for thumbnail)
- Border radius: 8px
- Hover effect: Slight scale up (1.02x) + shadow

### Card Structure

```
┌─────────────────────────────────┐
│                                 │
│     [Video Thumbnail]           │
│     16:9 ratio                  │
│                                 │
├─────────────────────────────────┤
│ Video Title (2 lines max)       │
│ ShujaaKing • Views • Time ago   │
└─────────────────────────────────┘
```

### Card Elements

**1. Thumbnail Image**
- 16:9 aspect ratio
- Source: YouTube thumbnail URL
- Overlay: Play button icon (semi-transparent)
- On hover: Darken overlay slightly

**2. Video Title**
- Font: Inter (heading font)
- Size: 18px
- Weight: 600
- Color: Dark Teal (#2D4A4A)
- Max lines: 2 (ellipsis if longer)
- Margin bottom: 8px

**3. Metadata Row**
- Font: Inter (body font)
- Size: 14px
- Weight: 400
- Color: #6B7280 (gray)
- Format: "ShujaaKing • [view count] • [time ago]"

**4. Click Behavior**
- Entire card is clickable
- Opens YouTube video in new tab
- Target URL: Full YouTube video link

---

## Implementation Options

### Option 1: Manual (Easiest)
Manually add 5-10 featured videos that you update monthly

**Pros:**
- Full control over which videos appear
- No app required
- Can feature best/most relevant content

**Cons:**
- Requires manual updates
- Not automatically fresh

**How to implement:**
1. Create custom Liquid section
2. Use metafields or section blocks to add video data
3. Input YouTube video IDs manually
4. Update once a month with latest content

### Option 2: Automated via App (Best for Freshness)
Use a Shopify app to auto-pull latest videos from YouTube

**Recommended Apps:**
- **Elfsight YouTube Feed** - Easy setup, customizable
- **Socialwidget** - Multi-platform social feed
- **Instagram Feed + TikTok Feed by Elfsight** - If adding multi-platform

**Pros:**
- Always shows latest content
- Automatically updates
- Professional appearance

**Cons:**
- Monthly app fee ($5-15)
- Less customization control
- Depends on third-party service

### Option 3: Custom API Integration (Most Control)
Use YouTube Data API to fetch latest videos

**Pros:**
- Full customization
- No monthly fees
- Complete data control

**Cons:**
- Requires development
- API rate limits
- More complex setup

---

## Manual Implementation Code

### Shopify Section File
Create: `sections/latest-adventures.liquid`

```liquid
{% comment %}
  Latest Adventures - YouTube Videos Section
{% endcomment %}

<div class="latest-adventures">
  <div class="page-width">

    {%- comment -%} Section Header {%- endcomment -%}
    <div class="section-header">
      <h2 class="section-title">{{ section.settings.heading }}</h2>
      <a href="{{ section.settings.youtube_channel_url }}" class="view-all-link" target="_blank">
        View All on YouTube
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
          <path d="M6 12l4-4-4-4" stroke="currentColor" stroke-width="2"/>
        </svg>
      </a>
    </div>

    {%- comment -%} Video Grid {%- endcomment -%}
    <div class="video-grid scroll-container">

      {%- for block in section.blocks -%}
        <a href="{{ block.settings.video_url }}" class="video-card" target="_blank" {{ block.shopify_attributes }}>

          {%- comment -%} Thumbnail {%- endcomment -%}
          <div class="video-thumbnail">
            <img
              src="{{ block.settings.thumbnail_url }}"
              alt="{{ block.settings.video_title }}"
              loading="lazy"
            >
            <div class="play-overlay">
              <svg width="48" height="48" viewBox="0 0 48 48" fill="white">
                <circle cx="24" cy="24" r="24" fill="rgba(0,0,0,0.7)"/>
                <path d="M19 14l14 10-14 10V14z" fill="white"/>
              </svg>
            </div>
          </div>

          {%- comment -%} Video Info {%- endcomment -%}
          <div class="video-info">
            <h3 class="video-title">{{ block.settings.video_title }}</h3>
            <p class="video-meta">ShujaaKing • {{ block.settings.views }} • {{ block.settings.time_ago }}</p>
          </div>

        </a>
      {%- endfor -%}

    </div>

  </div>
</div>

{% schema %}
{
  "name": "Latest Adventures",
  "settings": [
    {
      "type": "text",
      "id": "heading",
      "label": "Section Heading",
      "default": "Latest Adventures"
    },
    {
      "type": "url",
      "id": "youtube_channel_url",
      "label": "YouTube Channel URL",
      "default": "https://youtube.com/@shujaaking"
    }
  ],
  "blocks": [
    {
      "type": "video",
      "name": "Video",
      "settings": [
        {
          "type": "text",
          "id": "video_title",
          "label": "Video Title"
        },
        {
          "type": "url",
          "id": "video_url",
          "label": "YouTube Video URL"
        },
        {
          "type": "image_picker",
          "id": "thumbnail_url",
          "label": "Thumbnail Image"
        },
        {
          "type": "text",
          "id": "views",
          "label": "View Count",
          "default": "1.2K views"
        },
        {
          "type": "text",
          "id": "time_ago",
          "label": "Time Published",
          "default": "2 days ago"
        }
      ]
    }
  ],
  "presets": [
    {
      "name": "Latest Adventures"
    }
  ]
}
{% endschema %}
```

### CSS Styling
Add to theme CSS:

```css
/* Latest Adventures Section */
.latest-adventures {
  padding: 80px 0;
  background: #ffffff;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 40px;
}

.section-title {
  font-size: 32px;
  font-weight: 700;
  color: #2D4A4A;
  margin: 0;
}

.view-all-link {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 16px;
  color: #E8915B;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s;
}

.view-all-link:hover {
  color: #D67D47;
}

/* Video Grid */
.video-grid {
  display: flex;
  gap: 24px;
  overflow-x: auto;
  scroll-behavior: smooth;
  padding-bottom: 16px;
  -webkit-overflow-scrolling: touch;
}

.video-grid::-webkit-scrollbar {
  height: 8px;
}

.video-grid::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 4px;
}

.video-grid::-webkit-scrollbar-thumb {
  background: #E8915B;
  border-radius: 4px;
}

/* Video Card */
.video-card {
  flex: 0 0 300px;
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
  border-radius: 8px;
  overflow: hidden;
}

.video-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.1);
}

.video-thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  background: #000;
}

.video-thumbnail img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s;
}

.video-card:hover .video-thumbnail img {
  transform: scale(1.05);
}

.play-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0.9;
  transition: opacity 0.2s;
}

.video-card:hover .play-overlay {
  opacity: 1;
}

/* Video Info */
.video-info {
  padding: 16px 12px;
  background: #fff;
}

.video-title {
  font-size: 18px;
  font-weight: 600;
  color: #2D4A4A;
  margin: 0 0 8px 0;
  line-height: 1.4;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.video-meta {
  font-size: 14px;
  color: #6B7280;
  margin: 0;
}

/* Mobile Responsive */
@media (max-width: 768px) {
  .latest-adventures {
    padding: 60px 0;
  }

  .section-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
  }

  .video-card {
    flex: 0 0 85vw;
  }

  .video-grid {
    gap: 16px;
    scroll-snap-type: x mandatory;
  }

  .video-card {
    scroll-snap-align: start;
  }
}
```

---

## How to Get YouTube Thumbnail URLs

For any YouTube video, the thumbnail URL format is:
```
https://img.youtube.com/vi/[VIDEO_ID]/maxresdefault.jpg
```

**Example:**
Video URL: `https://youtube.com/watch?v=ABC123`
Thumbnail: `https://img.youtube.com/vi/ABC123/maxresdefault.jpg`

**Alternative sizes:**
- `mqdefault.jpg` - Medium quality (320x180)
- `hqdefault.jpg` - High quality (480x360)
- `maxresdefault.jpg` - Maximum quality (1280x720)

---

## Sample Videos to Feature

Based on ShujaaKing's content, feature videos like:

1. **Latest Camping Adventure**
   - Title: "Solo Camping in Michigan's Upper Peninsula"
   - Thumbnail: Tent at sunset

2. **Hiking/Trail Video**
   - Title: "Sunrise Summit Hike | Worth the 4AM Wake Up"
   - Thumbnail: Mountain view

3. **Magnet Fishing**
   - Title: "We Found WHAT in This River?!"
   - Thumbnail: Magnet with catch

4. **Gear Review**
   - Title: "My Go-To Camping Gear for 2025"
   - Thumbnail: Gear laid out

5. **Travel Vlog**
   - Title: "Road Tripping to [Location]"
   - Thumbnail: Scenic road/destination

---

## Setup Instructions for Shopify Admin

1. **Add the section file** to your theme
2. **Navigate to**: Online Store → Themes → Customize
3. **Add section**: "Latest Adventures"
4. **Add video blocks**: Click "Add video" for each one you want to feature
5. **Fill in details** for each video:
   - Video title
   - Full YouTube URL
   - Upload thumbnail image (or use YouTube thumbnail URL)
   - View count
   - Time ago

6. **Position**: Place before newsletter signup section
7. **Save** and preview

---

## Maintenance Schedule

**Weekly** (if manual):
- Check for new top-performing videos
- Update thumbnails if needed

**Monthly**:
- Replace oldest video with latest content
- Update view counts
- Refresh "time ago" text

**Quarterly**:
- Review all videos for relevance
- Feature seasonal content (summer camping, winter adventures, etc.)

---

## Analytics Tracking (Optional)

Add click tracking to measure engagement:

```liquid
onclick="gtag('event', 'video_click', {
  'video_title': '{{ block.settings.video_title }}',
  'video_url': '{{ block.settings.video_url }}'
});"
```

This helps you see which videos drive the most traffic from your store to YouTube.
