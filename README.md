# Musafir Cafe, Attock — website

**Quick look:** `Musafir-Cafe.html` is a single file with all photos embedded. Double-click it to open it in any browser, with no image folder needed.

**To deploy:** upload `index.html` with the `img/` folder (smaller, faster: images load separately and lazily).

Single-page, dependency-free site. Upload the whole folder to any static host (Vercel, Netlify, cPanel, GitHub Pages).

```
index.html            the site (HTML + inline CSS + small inline JS)
img/                  WebP photos (480w + 776w each), logo, logo mark, favicons
og-image.jpg          1200×630 social sharing image (real night photo)
robots.txt
sitemap.xml           includes image entries
```

## Real content used (from @musafircafe.pk, public posts and bio)

- Bio line: "A little roadside spot to sip, chill & connect"
- Drinks: mojitos, iced teas, shakes, daiquiris, smoothies (bio); karak chai, tea, coffee (posts)
- Hours: open daily, 5 PM – 12 AM
- Address: Opposite Tahir Byco Pump, Kamra Road, Attock
- Google Maps: https://maps.app.goo.gl/eApnDcbG5SXm9JeW9
- Tagline: "Kuch Der, Bas Apne Liye." · Reel title card: "A Little Place. A Lot of Stories."
- Story posts: handmade signboard (Gondal Bazaar planks, hand-painted), the empty-room build, Asra's crochet gift, the Lahore training trip, soft launch, first 20 days (UNO, painting, first workshop), first Jamming Night
- Announced events: game nights, movie nights, ghazal nights, canvas painting, community circles
- Guest quotes: short, attributed, linked to the original public posts by @postcardsbytooba and @thelittlefunclub___
- Photos: 8 of Musafir's own posts (night exterior, dusk at the kiosk, sunset crowd, drinks, first jamming night, the empty site, the handmade signboard, Asra's crochet gift). Photos in collaborator posts were not used.

## Still to fill

Search `index.html` for `data-placeholder` and `TODO`.

1. **Domain**: replace `https://www.example.com/` in `index.html`, `robots.txt`, `sitemap.xml`.
2. **Menu flavours & prices** (`data-placeholder="menu"`): not published on Instagram.
3. **Phone / WhatsApp** (`data-placeholder="phone"`): not published. Add `"telephone"` to the JSON-LD too.
4. **More photos (optional)**: add another `<figure class="card">` to the hero ring or a `<figure class="print">` to the photo table. The ring spaces itself for any number of photos.

## Behaviour

- Open/closed pill and "closes in …" line are computed in Pakistan time (UTC+5) from the 5 PM – 12 AM hours.
- Hero: a 3D ring of real photos (CSS 3D, no WebGL library). Drag or swipe to spin with momentum, arrow keys and buttons work too, tap the front photo to open it full size. It advances gently every few seconds when idle, and only while visible; reduced-motion turns that off.
- Photo table: drag the prints around (mouse, touch or arrow keys). Reveal-on-scroll applies only to content below the first screen.
- Hero image is preloaded with `fetchpriority="high"`; all other images are lazy with explicit width/height (no layout shift).

## Tested

No horizontal scroll and no runtime errors at 320, 375, 390, 412, 768, 1024, 1280 and 1600 px; dark and light colour schemes; reduced motion; keyboard (skip link, nav toggle with Escape, visible focus rings).
