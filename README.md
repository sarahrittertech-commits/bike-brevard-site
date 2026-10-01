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

## When Apple approves the app

The "Coming soon" button and the status line appear **twice**: in the hero
at the top and in the closing banner at the bottom. Each copy sits between
these two comments in `index.html`:

```html
<!-- APP STORE LINK (1 of 2): ... -->
...
<!-- /APP STORE LINK (1 of 2) -->
```

In **both** places, replace everything between the comments with this,
pasting in the real App Store URL:

```html
<div class="store">
  <a class="store-btn" href="https://apps.apple.com/app/idXXXXXXXXXX">
    <svg viewBox="0 0 24 24" width="18" height="18" aria-hidden="true"><path fill="currentColor" d="M16.4 12.6c0-2.6 2.1-3.8 2.2-3.9-1.2-1.8-3.1-2-3.7-2-1.6-.2-3.1.9-3.9.9-.8 0-2-.9-3.4-.9-1.7 0-3.3 1-4.2 2.6-1.8 3.1-.5 7.7 1.3 10.2.8 1.2 1.8 2.6 3.1 2.5 1.2 0 1.7-.8 3.2-.8s1.9.8 3.2.8c1.3 0 2.2-1.2 3-2.4 1-1.4 1.4-2.7 1.4-2.8-.1 0-2.6-1-2.6-4.2zM13.9 5c.7-.8 1.1-1.9 1-3-1 0-2.1.7-2.8 1.5-.6.7-1.2 1.8-1 2.9 1 .1 2.1-.6 2.8-1.4z"/></svg>
    Download on the App Store
  </a>
</div>
```

That turns the grey "coming soon" label into a real link and drops the
"Submitted to the App Store…" line. Also change the closing banner heading
(search for `closing-title`) from "coming soon to the App Store" to
something like "Bike Brevard Map: now on the App Store".

Commit and push to `main`; GitHub Pages republishes within a minute or two.

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
