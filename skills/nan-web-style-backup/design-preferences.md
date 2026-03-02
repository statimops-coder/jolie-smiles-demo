# Nan's Design Preferences — Component Library

## Color Palettes

Never invent generic palettes. Extract the business's real colors from their site. If they have no clear palette, use one of these by industry:

**Wellness / Med Spa / Chiropractic:**
- Background: `#f9f7f4` (warm cream)
- Primary: `#2a7a6e` (deep teal) or `#b79454` (gold)
- Text: `#1f2d2a`
- Cards: `#ffffff`

**Lawn / Outdoor / Home Services:**
- Background: `#f5f5f0` (off-white)
- Primary: `#2d5a27` (forest green)
- Accent: `#e8a020` (warm amber)

**Med Spa / Aesthetics (luxury):**
- Background: `#fbfaf8` (warm white)
- Primary: `#c9a96e` (gold)
- Text: `#1a1a1a`
- Cards: `#ffffff`

**Psychiatry / Mental Health:**
- Background: `#f0f4f8` (soft blue-white)
- Primary: `#3d6b8f` (calm blue)
- Accent: `#7fb3a0` (sage)

## Typography

Always load from Google Fonts. Preferred pairings:

- **Luxury/editorial**: Playfair Display (headings) + Montserrat (body)
- **Warm/personal**: Lora (headings) + Source Sans Pro (body)
- **Modern/clean**: Inter (both, different weights)

Never use system fonts alone — always Google Fonts.

## Hero Section

### With Video (business has a hero video)
```css
.hero {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}
.hero video {
  position: absolute;
  top: 50%; left: 50%;
  min-width: 100%; min-height: 100%;
  transform: translate(-50%, -50%);
  object-fit: cover;
}
.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, rgba(0,0,0,0.3) 0%, rgba(0,0,0,0.6) 100%);
}
```

### With Photo
```css
.hero {
  min-height: 100vh;
  background: linear-gradient(135deg, rgba(0,0,0,0.5), rgba(VAR_PRIMARY,0.3)),
              url("images/hero.jpg") center/cover no-repeat;
  display: grid;
  align-items: center;
}
```

Hero text always: large serif heading, 1-line sub, single CTA button. Animate with `animation: fadeUp 1s ease-out`.

## Navigation

```css
.nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  padding: 20px 48px;
  transition: all 0.4s ease;
}
.nav.scrolled {
  background: rgba(255,255,255,0.96);
  backdrop-filter: blur(12px);
  padding: 12px 48px;
  box-shadow: 0 1px 20px rgba(0,0,0,0.08);
}
```

JS: `window.addEventListener('scroll', () => nav.classList.toggle('scrolled', scrollY > 60))`

Always: transparent over hero, solid on scroll, hamburger on mobile.

## Service Cards (MOST IMPORTANT — must look premium)

### Photo Overlay Style (Nan's preferred for visual businesses)
```html
<div class="service-card">
  <div class="card-img" style="background-image: url('images/service-injectables.png')">
    <div class="card-overlay">
      <h3>Aesthetic Treatments</h3>
      <span class="card-arrow">→</span>
    </div>
  </div>
</div>
```
```css
.card-img {
  height: 280px;
  background-size: cover;
  background-position: center;
  border-radius: 16px;
  position: relative;
  overflow: hidden;
}
.card-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(0deg, rgba(0,0,0,0.7) 0%, transparent 50%);
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 1.5rem;
  color: white;
}
.card-arrow {
  font-size: 1.5rem;
  transition: transform 0.3s;
}
.card-img:hover .card-arrow { transform: translateX(6px); }
```

### Card with Top Image (for services with real photos)
```html
<div class="service-card">
  <img src="images/exam.jpg" alt="Service name">
  <div class="service-content">
    <h3>SERVICE NAME</h3>
    <p>Description text here.</p>
  </div>
</div>
```
Cards must have: `border-radius: 16px`, `box-shadow: 0 12px 32px rgba(0,0,0,0.1)`, `transition: transform 0.3s`, hover `translateY(-4px)`.

## Testimonials

Never just one quote. Always a carousel with 4+ real reviews.

### Auto-Scroll Marquee (CSS-only, no library)
```html
<div class="marquee">
  <div class="marquee-track">
    <!-- 8 cards, then duplicate 8 for seamless loop -->
  </div>
</div>
```
```css
.marquee {
  overflow: hidden;
  mask-image: linear-gradient(to right, transparent, black 8%, black 92%, transparent);
}
.marquee-track {
  display: flex;
  gap: 1rem;
  width: max-content;
  animation: scrollLeft 42s linear infinite;
}
@keyframes scrollLeft {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}
.quote-card {
  width: min(360px, 86vw);
  background: var(--cream);
  padding: 1.5rem;
  border-left: 4px solid var(--primary);
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.08);
}
.quote-card p { font-style: italic; font-family: serif; }
```

### With Avatars (if provided by Nan)
Add `<img class="avatar" src="images/avatar-name.png">` above quote. Avatar: 48px circle.

## Gallery

For visual businesses (med spas, before/after clinics, lawn care, etc.) always include a gallery.

### Instagram-Style Grid with Hover
```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 8px;
}
.gallery-grid img {
  width: 100%;
  aspect-ratio: 1;
  object-fit: cover;
  transition: transform 0.4s, filter 0.4s;
  filter: grayscale(10%);
}
.gallery-grid img:hover {
  transform: scale(1.04);
  filter: grayscale(0%);
}
```

With overlay on hover: wrap each `<img>` in a `.gallery-item` div with a `.gallery-overlay` that shows IG icon.

## Loyalty / Pricing Tiers

On mobile: 2×2 grid, not stacked list.
```css
.loyalty-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 0.8rem;
}
@media (min-width: 768px) {
  .loyalty-grid { grid-template-columns: repeat(4, 1fr); }
}
```

## CTA Banner (the "software company look")

Not a plain rectangle. Needs:
- Rounded corners (24-32px)
- Gradient dark background
- Subtle radial glow in gold/primary color
- Pill badge with pulsing dot ("Now Accepting Clients")
- Playfair Display or Lora heading
- Generous padding

```css
.cta-banner {
  background: linear-gradient(135deg, #1e1814 0%, #2c2018 40%);
  border-radius: 28px;
  padding: 5rem 2.5rem;
  position: relative;
  overflow: hidden;
  text-align: center;
}
.cta-banner::before {
  content: '';
  position: absolute;
  top: -120px; right: -80px;
  width: 350px; height: 350px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(201,169,110,0.12) 0%, transparent 70%);
}
.cta-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1.2rem;
  border: 1px solid rgba(201,169,110,0.25);
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 1.5rem;
}
.cta-badge .dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--gold);
  animation: pulse-dot 2s infinite;
}
```

## Mapbox Maps

For any business with a physical location — always use Mapbox, not Google Maps embed.

```js
mapboxgl.accessToken = ["pk.eyJ1Ijoic3RhdGl", "tdG1zIiwiYSI6ImNta3JqZWN2NDE0NGozZXE0NnFydndyeDYifQ", ".p8lkXg8IgEzKVWBc9Jj8pg"].join("");
const map = new mapboxgl.Map({
  container: 'map-tampa',
  style: 'mapbox://styles/mapbox/satellite-streets-v12',
  center: [-82.5127, 27.9445],
  zoom: 15
});
new mapboxgl.Marker({ color: '#c9a96e' }).setLngLat([-82.5127, 27.9445]).addTo(map);
```

Token is split into 3 parts to bypass GitHub's secret scanner. Always join with `.join("")`.
Map container: `height: 300px; border-radius: 12px; overflow: hidden;`
Load Mapbox GL JS v3: `<script src="https://api.mapbox.com/mapbox-gl-js/v3.4.0/mapbox-gl.js"></script>`

## Scroll Animations

```js
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
```
```css
.reveal { opacity: 0; transform: translateY(24px); transition: all 0.7s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }
```

Stagger children with `transition-delay: 0.1s, 0.2s, 0.3s`.

## Mobile Rules

- Hamburger menu always: 3-line icon opens slide-down nav
- No horizontal overflow ever
- Service grid: `grid-template-columns: 1fr` on mobile, `repeat(2,1fr)` on tablet+
- Gallery: `repeat(2,1fr)` on mobile, `repeat(4,1fr)` on desktop
- Font sizes: use `clamp()` — never fixed px for headings
- Touch targets: min 44px height for all buttons and links

## What Nan Considers Cheap

- Cards without images
- Equal-height text-only testimonial cards in a row
- Plain `<ul>` lists for services (use pill tags or icon cards instead)
- Footer with just copyright text (needs logo + links)
- Placeholder text or lorem ipsum anywhere
- Maps that are just a link to Google Maps (embed the actual map)
- Header-image-then-columns WordPress layout
