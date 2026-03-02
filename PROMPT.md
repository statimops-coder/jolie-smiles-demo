# Jolie Smiles Denture & Implant Studio — Demo Website

Build a stunning single-page demo website for Jolie Smiles. This is a pitch demo to show what their website COULD look like. Use ALL their real content, media, and branding.

## CRITICAL DESIGN RULES (read skills/nan-web-style-backup/SKILL.md first)

1. **Font:** Use Cormorant Garamond (editorial, elegant) for headings, Inter for body at 14-15px
2. **NO rounded corners by default** — use sharp or barely rounded (2-3px max)
3. **NO emojis as icons** — use Lucide SVG icons only (via CDN)
4. **NO centering everything** — use asymmetric layouts, left-aligned text blocks, split sections
5. **NO flat cards** — use depth: glassmorphism, layered elements, subtle shadows
6. **NO generic stock feel** — this must feel custom, editorial, premium
7. **Body text 14-15px**, not 16+
8. **Use their real images from images/ folder** — ALL of them
9. **NO em dashes in copy**
10. **Videos are ACTIVE elements** — embed YouTube testimonials prominently, not hidden

## Business Info

- **Name:** Jolie Smiles Denture & Implant Studio
- **Owner:** Dr. Caroline Truong, DMD, MS (Prosthodontist)
- **Address:** 7749 Van Dyke Rd, Odessa, FL 33556
- **Phone:** (813) 576-2602 / (813) 687-4916
- **Email:** info@joliesmiles.com
- **Hours:** Mon-Thu 8:00 AM - 4:00 PM
- **Website:** joliesmiles.com
- **Booking:** https://flexbook.me/joliesmile
- **Social:** Instagram @thejoliesmiles, YouTube @joliesmiles4285, Facebook
- **Tagline:** "It's time to smile again!"

## Dr. Caroline Truong Bio

- DMD + MS from University of Florida
- 11 years of training
- Chief Doctor at UF Prosthodontics and Implant Specialty program
- Clinical Professor at UF and Lake Erie College of Medicine
- Speaks French, Vietnamese, English (office also: Spanish, Russian)
- Volunteers: dental clinics across FL, mission trips to Guatemala, Veterans Stand Down
- 2 research publications (Journal of Prosthetic Dentistry)
- Member: ITI, ADA, American College of Prosthodontics, Florida Prosthodontic Assoc
- "One of the few & most known Denture & Implant Specialists in Florida"
- "She represents the answer for those who have been told 'it can't be done.'"

## Services

1. **Dental Implants** — Permanent solution for broken, damaged, or missing teeth
2. **All-on-4 Dental Implants** — 4 implants, complete smile makeover
3. **Implant Supported Dentures** — Implants hold dentures securely
4. **Zygomatic/Pterygoid/Mini Implants** — "No bone? No problem!"
5. **Digital 3D Premium Dentures** — Thinner, more comfortable, done in one day
6. **Snap-On Dentures** — Snap and hold into place
7. **Smile Makeovers** — Full mouth reconstruction
8. **Same Day Denture Repair**

## Key Differentiators

- "No corporate, no feeling like a number, true private small business"
- Specialist (prosthodontist), not a general dentist — other dentists refer TO her
- Same-day solutions with in-house dental lab
- 3D CT scanning, intraoral cameras
- Custom smile design (size, color, shape matched to face)
- Proprietary surgery recovery recipe
- Life Maintenance care package
- Flexible financing (Cherry, Proceed Finance, Lasso MD)
- "The answer for those who have been told 'it can't be done'"

## Patient Testimonials

- "I'm not in pain anymore" — Dolvin
- "This has changed my life; I tell everyone about my new smile"
- "I feel beautiful"
- "If I gave it a 10/10 I'd be lying, I need to go higher"
- "I can trust you" — Carolyn
- "The whole process is basically pain free" — Matt
- "You make it fun and pain free" — Guy
- "I am not used to laughing... Now you can, now you will" — Lenka
- "Dr. Truong worked with me on a price, she personally called me" — Will
- "The people here are so sweet and so kind" — Beatrice
- "This has tremendously changed my life. I have more confidence" — Paulina

## YouTube Videos to Embed (use at least 6 prominently)

- https://www.youtube.com/watch?v=GkuAiWS0MOk
- https://www.youtube.com/watch?v=KGMkD50Sues
- https://www.youtube.com/watch?v=xZ0jC1LN3S8
- https://www.youtube.com/watch?v=VgLwI5lz-sM
- https://www.youtube.com/watch?v=evae0bAaw74
- https://www.youtube.com/watch?v=pGU-IKuQrrM
- https://www.youtube.com/watch?v=5-wsDnO6IaI
- https://www.youtube.com/watch?v=8a3uq_1BKMk
- https://www.youtube.com/watch?v=dPoIT-HE7xc
- https://www.youtube.com/watch?v=tvuSoYudcgQ
- https://www.youtube.com/watch?v=lQ2aYXH6OSY

## Homepage Video (autoplay background)

https://cdn.prod.website-files.com/637e153cb4b25769e5d5bd94%2F67d2e974473496d5fd4cda05_1000000768-1-transcode.mp4

## Images (all in images/ folder, USE ALL)

- Doc.webp — Dr. Truong headshot
- Full Logo Black.png — logo
- about.webp — about section
- Photo2 through Photo8-topaz-enhance.webp — patient/smile photos
- Before (10-16).webp — before/after gallery
- 1000013292-1000015810.webp — patient/procedure photos
- DSC_*.webp — office/procedure shots
- Multiple branded design assets and YouTube thumbnails

## Map (Mapbox)

```js
const token = ["pk.eyJ1Ijoic3RhdGl","tdG1zIiwiYSI6ImNta3JqZWN2NDE0NGozZXE0NnFydndyeDYifQ",".p8lkXg8IgEzKVWBc9Jj8pg"].join("")
```
Center: [-82.5764, 28.1293] (Odessa, FL)

## Color Palette

- Primary: Deep navy (#1a1a2e)
- Accent: Warm gold (#c9a96e)
- Background: Warm off-white (#faf8f5)
- Text: Dark charcoal (#2d2d2d)
- Premium/luxurious feel — specialist practice, not chain dental

## Sections

1. Hero — Bold statement + background video + CTA
2. Video Testimonials — Grid of YouTube embeds with patient names/quotes
3. Meet Dr. Truong — Split layout, photo + bio + credentials
4. Services — Card grid with Lucide icons
5. Before & After Gallery — Interactive comparison with real photos
6. Why Choose Jolie Smiles — Differentiators
7. Patient Stories — Quote carousel (fade transitions)
8. What to Expect — 3-step process
9. Financing — Cherry, Proceed, Lasso
10. Contact/Location — Mapbox map, address, phone, hours, booking
11. Footer

## Technical

- Single HTML file, inline CSS
- CDN: Google Fonts, Lucide, Mapbox GL JS
- Responsive, mobile-first
- Scroll animations (intersection observer)
- Lazy YouTube embeds
- Glass nav on scroll
- Make it feel like a $40K agency build
