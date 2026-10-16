# Bike Brevard Map — landing page

A one-page site for the [Bike Brevard Map](https://github.com/sarahrittertech-commits/brevard-bike-map)
iOS app, hosted on GitHub Pages.

Plain HTML and CSS: no framework, no build step, no analytics, no tracking,
and no requests to any other site (the fonts are hosted here too).

```
index.html     the whole page
styles.css     all styling
fonts/         Bricolage Grotesque + Karla (SIL Open Font License)
img/           photos, the launch scene, the icon and the squirrel
shots/         app screenshots
```

## Preview it on your Mac

```bash
python3 -m http.server 8765
```

Then open http://127.0.0.1:8765 in a browser.

## The App Store link

The app is live at
https://apps.apple.com/us/app/bike-brevard-map/id6816144426
(approved October 2026). The link appears **twice** in `index.html`: the
hero button at the top and the closing banner button at the bottom. Each sits
between `<!-- APP STORE LINK (1 of 2) -->`-style comments, so if the URL ever
changes, update both.

## Parked: "When Helene came through"

Taken off the page on 16 October 2026 to bring back later. It sat between
"How we use the path" and the Heart of Brevard video. To restore it, paste
this back into `index.html` just above `<!-- Featured video -->`. Its styles
(`.band-quiet`, `.closing-line`) are still in `styles.css`.

```html
  <!-- Helene -->
  <section class="band band-quiet">
    <div class="wrap narrow">
      <p class="eyebrow eyebrow-light">September 2024</p>
      <h2>When Helene came through</h2>
      <p>After Hurricane Helene we had no power, no gas, no cell service and no internet, and the radio news was out of date. But we had bikes and plenty of food to share.</p>
      <p>So we rode. We checked on neighbors across town and delivered handwritten notes offering hot showers at our house. We dropped off supplies at the little free library boxes. We passed around handwritten news so friends knew where to find clean water, who could lend a camp stove, and that they could come stay with us.</p>
      <p class="closing-line">Biking around town gave us the power to connect with our neighbors.</p>
    </div>
  </section>
```

## Photos

Photos are resized (1400px or less) and compressed (under 300 KB). They are
re-encoded with **no metadata**, so no GPS location, camera or date
information is published. If you add a photo, strip it the same way.
On a Mac, exporting from Photos with "Include location information" turned
off and then running `sips -Z 1400` on it is a reasonable manual route.

## Credits

The launch scene, icon and white squirrel come from the app's own design
artwork. Fonts are Bricolage Grotesque and Karla, both under the SIL Open
Font License.
