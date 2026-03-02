# Jolie Smiles Demo — REBUILD

You are building a premium single-page website demo for a dental implant specialist. This must look like a $40K agency build. Read EVERY line of this prompt before writing code.

## ABSOLUTE RULES — BREAK ANY AND THE BUILD IS REJECTED

1. Font pairing: Cormorant Garamond (Google Fonts) for headings, Inter for body at 14px
2. NO rounded corners by default. Sharp edges. Only CTA buttons and the map get border-radius.
3. NO emojis anywhere. Use Lucide icons via CDN: `<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>`
4. NO centering everything. Use asymmetric split layouts (60/40, 70/30). Left-align text blocks.
5. NO flat cards. Every card needs: box-shadow, hover transform, image overlay, or glassmorphism.
6. Body text: 14px. Headings: use clamp() for responsive sizing.
7. NO em dashes in copy.
8. Light theme: background #faf8f5 (warm cream), text #1a1a1a, accent gold #c9a96e, navy #1a1a2e for dark sections
9. ALL images must use their original Webflow CDN URLs (NOT local paths). Base URL pattern: `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/FILENAME`
10. Videos are active elements, not decoration. YouTube embeds must be prominent.
11. Scroll animations: `.reveal` class with IntersectionObserver. BUT also add a fallback: after 2 seconds, force ALL `.reveal` elements to `.visible` so the page never appears blank.

## IMAGE URLS (use these exact CDN URLs)

### Key Images
- Logo: `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab5281011_Full%20Logo%20Black.png`
- Dr. Truong: `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab528102c_About%20Us%20Hero.webp`
- Office: `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810f2_JolieSmiles_Office.webp`
- About: `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab5281110_about.webp`

### Patient / Procedure Photos (use in services + gallery sections)
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810dc_Photo3-topaz-enhance.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810dd_Photo5-topaz-enhance.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810de_Photo7-topaz-enhance.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810df_Photo8-topaz-enhance.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e0_Photo2-topaz-enhance.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e1_1000013292.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e2_1000014813.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e3_1000015704.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e4_1000014432.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e5_1000015808.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810e6_1000015810.webp`

### Before/After Gallery
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810f9_Before%20(10).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810fa_Before%20(11).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab5281105_Before%20(12).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab5281118_Before.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab5281119_Before%20(4).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab528111a_Before%20(6).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab528111b_Before%20(8).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab528111c_Before%20(16).webp`
- Veneers Before: `https://cdn.prod.website-files.com/637e153cb4b25769e5d5bd94/62eb28a0198b2234a4e30b01_VeneersBefore1.jpeg`
- Veneers After: `https://cdn.prod.website-files.com/637e153cb4b25769e5d5bd94/62eb28a0198b2213f5e30af3_VeneersAfter1.jpeg`

### Office / Clinical Shots
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811d5_DSC_1238.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811d7_DSC_1246.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811d9_DSC_0995.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811da_DSC_1193.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811dd_DSC_1062.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811de_DSC_1017.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e0_DSC_1263.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e1_DSC_0740%20-%20Copy.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e2_DSC_0797.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e3_DSC_1084.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e4_DSC_0591%20(1).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e5_DSC_0937.webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811e6_DSC_0748.webp`

### Homepage Video (autoplay muted background)
`https://cdn.prod.website-files.com/637e153cb4b25769e5d5bd94%2F67d2e974473496d5fd4cda05_1000000768-1-transcode.mp4`

### Veterans / Community
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52811af_Veterans-p922t390yhp3n7vt352a9n4irzkufstk11tbe24494.webp`

### Payment / Promo
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/6863051f2edd95eab52810f5_Payment-options%20(1).webp`
- `https://cdn.prod.website-files.com/6863051f2edd95eab5280ecb/68a38c11b295882391cd575a_%5BJollie%20Smiles%5D%20Dental%20Implant%20-%20NPG%20Magazine%20%2B%20Gift%20Card%20(1).png`

## BUSINESS INFO

- Name: Jolie Smiles Denture & Implant Studio
- Doctor: Dr. Caroline Truong, DMD, MS (Prosthodontist)
- Address: 7749 Van Dyke Rd, Odessa, FL 33556
- Phone: (813) 576-2602
- Email: info@joliesmiles.com
- Hours: Mon-Thu 8AM-4PM
- Booking: https://flexbook.me/joliesmile
- Instagram: @thejoliesmiles
- YouTube: @joliesmiles4285

## DR. TRUONG BIO (use this exact content)

- DMD + MS from University of Florida
- 11 years of training
- Chief Doctor at UF Prosthodontics and Implant Specialty program
- Clinical Professor at UF and Lake Erie College of Medicine
- Speaks French, Vietnamese, English. Office also: Spanish, Russian.
- Volunteers at dental clinics across FL, led mission trips to Guatemala
- Veterans Stand Down Denture Mobile Clinic volunteer
- 2 research publications in the Journal of Prosthetic Dentistry
- "She represents the answer for those who have been told 'it can't be done.'"

## SERVICES (6 main)

1. Dental Implants - Permanent solution for missing teeth
2. All-on-4 Dental Implants - Complete smile makeover with just 4 implants
3. Digital 3D Premium Dentures - Thinner, more comfortable, done in one day
4. Implant Supported Dentures - Implants hold dentures securely in place
5. Snap-On Dentures - Click into place, eat your favorite foods again
6. Zygomatic Implants - "No bone? No problem." For patients told they need grafting.

## DIFFERENTIATORS (weave into copy)

- Private practice, not corporate. "No feeling like a number."
- Specialist: other dentists refer TO her
- Same-day solutions with in-house lab
- 3D CT scanning + intraoral cameras
- Custom smile design matched to your face
- Proprietary surgery recovery recipe
- "The answer for those told 'it can't be done'"

## PATIENT TESTIMONIALS (real quotes, real names)

- "I'm not in pain anymore" - Dolvin
- "This has changed my life. I tell everyone about my new smile."
- "I feel beautiful"
- "If I gave it a 10/10 I'd be lying, I need to go higher"
- "I can trust you" - Carolyn
- "The whole process is basically pain free" - Matt
- "You make it fun and pain free" - Guy
- "I am not used to laughing... Now you can, now you will" - Lenka
- "Dr. Truong worked with me on a price, she personally called me" - Will
- "The people here are so sweet and so kind" - Beatrice
- "This has tremendously changed my life. More confidence." - Paulina

## YOUTUBE VIDEOS (embed 6 as prominent cards with thumbnails)

- GkuAiWS0MOk
- KGMkD50Sues
- xZ0jC1LN3S8
- VgLwI5lz-sM
- evae0bAaw74
- pGU-IKuQrrM

Embed as: `<iframe src="https://www.youtube.com/embed/VIDEO_ID" ...>` with lazy loading. Show as cards with a play button overlay, not raw iframes.

## MAPBOX

```js
const token = ["pk.eyJ1Ijoic3RhdGl","tdG1zIiwiYSI6ImNta3JqZWN2NDE0NGozZXE0NnFydndyeDYifQ",".p8lkXg8IgEzKVWBc9Jj8pg"].join("");
```
Center: [-82.5764, 28.1293] — Odessa, FL. Use satellite-streets-v12 style.

## PAGE STRUCTURE (follow this exactly)

### 1. HERO (100vh)
- Background: the MP4 video, muted autoplay loop
- Dark gradient overlay (0.4 to 0.7 opacity, bottom heavier)
- Left-aligned text block (60% width max):
  - Small eyebrow text: "PROSTHODONTIST & IMPLANT SPECIALIST"
  - Large heading: "It's time to smile again."
  - One-liner: "Same-day dental implants and premium dentures. One specialist. One visit. One smile."
  - CTA button: "Schedule Your Consultation" linking to flexbook.me/joliesmile
- Logo in top-left nav (transparent, goes solid on scroll with glassmorphism)

### 2. MEET DR. TRUONG
- 60/40 split: her photo on left (the About Us Hero image), bio text on right
- Name in large Cormorant Garamond
- Key credentials as subtle pill badges (not a bullet list)
- Quote block: "She represents the answer for those who have been told 'it can't be done.'"
- Background: cream (#faf8f5)

### 3. VIDEO TESTIMONIALS
- Section heading left-aligned: "Real patients. Real stories."
- 3-column grid (2 on tablet, 1 on mobile)
- Each card: YouTube thumbnail as background, play button overlay, patient name + quote below
- Click loads the iframe (lazy)

### 4. SERVICES
- 3-column grid of photo overlay cards
- Each card uses a real clinical/procedure photo as background
- Service name + one-liner overlaid at bottom with gradient
- Hover: slight scale + arrow slides right

### 5. BEFORE & AFTER
- Side-by-side image pairs in a clean grid
- Use the Before images paired logically
- Include the Veneers before/after pair
- Heading: "See the transformation."

### 6. WHY JOLIE SMILES (dark section, navy #1a1a2e background)
- 3-4 feature blocks with Lucide icons
- "Private practice, not corporate" / "Same-day, in-house lab" / "The specialist other dentists trust" / "No bone? No problem."
- Gold (#c9a96e) accent on icons and highlights
- White text

### 7. PATIENT STORIES CAROUSEL
- Auto-scrolling marquee (CSS animation, no JS library)
- Quote cards with left gold border
- Duplicate cards for seamless loop
- Mask edges with gradient fade

### 8. CTA BANNER
- Dark rounded container with radial gold glow
- Pill badge: "Now Accepting New Patients" with pulsing dot
- Heading: "Your smile transformation starts here."
- CTA button to flexbook.me

### 9. CONTACT + MAP
- Split: info on left, Mapbox satellite map on right
- Phone, email, address, hours
- "Schedule Now" button

### 10. FOOTER
- Logo, social links (Instagram, YouTube, Facebook), nav links
- "2026 Jolie Smiles Denture & Implant Studio. All rights reserved."

## TECHNICAL REQUIREMENTS

- Single index.html file. All CSS in `<style>`, all JS in `<script>`.
- Google Fonts: Cormorant Garamond (400,600,700) + Inter (400,500,600)
- Lucide icons via CDN
- Mapbox GL JS v3.4.0
- Mobile-first responsive
- Smooth scroll: `html { scroll-behavior: smooth; }`
- Nav: transparent over hero, glassmorphism on scroll
- Hamburger menu on mobile (working toggle)
- IMPORTANT: Add this fallback for reveal animations:
  ```js
  setTimeout(() => document.querySelectorAll('.reveal').forEach(el => el.classList.add('visible')), 2000);
  ```

## WHAT NOT TO DO

- Do NOT dump all images in a grid at the bottom "just to use them all"
- Do NOT use images without purpose. Every image must serve the section it's in.
- Do NOT center all text. Use asymmetric layouts.
- Do NOT use placeholder text. All copy comes from this prompt.
- Do NOT use local image paths. All images use CDN URLs above.

When completely finished, run: openclaw system event --text "Done: Jolie Smiles demo rebuilt" --mode now
