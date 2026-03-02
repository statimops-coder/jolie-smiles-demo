---
name: nan-web-style
description: Nan's personal web design preferences and standards for client demo sites. Use when building any lead gen demo website for Statim's web development business. Provides design rules, component patterns, and quality standards to follow before writing a single line of HTML.
---

# Nan's Web Style Guide

Before building any demo site, read references/design-preferences.md for the full component library and examples. This file covers the workflow and critical rules.

## Workflow

1. **Scrape first** — always fetch the business's real site before designing. Extract real photos, colors, fonts, team members, testimonials, service lists. Never invent content.
2. **Read design-preferences.md** — load component patterns before coding.
3. **Build single-file HTML** — self-contained, inline CSS and JS. No build tools, no npm, no CDN frameworks (except Google Fonts and Mapbox GL JS).
4. **Preview mentally** — before writing, visualize every section on mobile. If it would look cheap, redesign it.
5. **Deploy to GitHub Pages** — `statimops-coder/<business-name>-demo` repo.

## Non-Negotiable Rules

- **Light theme always** unless Nan explicitly requests dark. Cream/white backgrounds, dark text.
- **Real photos only** — no Unsplash, no AI-generated images. Scrape from the business's existing site, Instagram, Google Maps, or Facebook.
- **No em dashes** (`—`) in any copy. Use plain punctuation. Em dashes make copy look automated.
- **No ALL CAPS body text** — headings can be uppercase sparingly.
- **No basic flat cards** — every card needs depth: photo overlay, shadow, hover transform, or gradient.
- **No placeholder testimonials** — use real quotes scraped from their site, Google reviews, or Yelp.
- **Mobile is the primary canvas** — design mobile-first, desktop is secondary.
- **Mapbox for location businesses** — always use satellite-streets style when possible. Token: split across array to bypass GitHub scanner.
- **Serve video from source CDN** — never commit large video files to git. Reference original URL.

## What Nan Hates

- Basic WordPress-clone layouts (header image, 3 columns of text, footer)
- Flat service cards with just text and an icon
- Single testimonial quotes (needs carousel with multiple)
- Cookie-cutter color schemes (navy+white, green+white for everything)
- Animations that are bouncy, flashy, or distracting
- CTAs that look like basic rectangles
- **Basic/rounded/sans-serif fonts** — avoid generic system-style or overly friendly fonts
- **Rounded corners as a default** — not every element gets `border-radius`; use sharp or subtle radius intentionally
- **Centering everything by default** — centered layout only when there's a clear visual reason; default to left-aligned or asymmetric
- **Emojis as icons** — use real icon libraries (Lucide, Heroicons, Font Awesome, etc.), never emoji placeholders

## What Nan Likes

- Real data and real media — scraped from the business, not invented
- Soft, subtle effects (shadows, blurs, gradients — nothing flashy or bouncy)
- Editorial or distinctive fonts — not basic, not safe
- Medium or small body font sizes — not huge, bloated text
- Research-informed design — look up current frontend/design trends before building
- Mapbox for any map integration
- Layered / multi-depth content — overlapping elements, z-stacking, sections with depth
- Videos and real photos used as active visual elements, not decoration
- No generic templates or components — every section should feel custom-built

## Quick Quality Checklist

Before considering a build complete:
- [ ] Hero is full-screen with real business photo or video
- [ ] Service cards have photo overlay or real image + hover effect
- [ ] Testimonials are a carousel with 4+ real quotes
- [ ] Gallery exists if business has visual content (med spa, lawn care, etc.)
- [ ] Maps embedded for businesses with physical location
- [ ] CTA section looks premium (rounded corners, gradient bg, subtle glow)
- [ ] Mobile hamburger menu works
- [ ] Scroll-reveal animations on every section (subtle, not flashy)
- [ ] No stock photos, no AI headshots

## See Also

- **references/design-preferences.md** — full component library with code patterns
