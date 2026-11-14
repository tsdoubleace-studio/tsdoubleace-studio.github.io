# TsDoubleAce Studio website

Free website on GitHub Pages for all TsDoubleAce apps and games: a home page, one folder per
app with its own privacy policy, and the AdMob `app-ads.txt` file.

Address once published: `https://<github-username>.github.io/` (the repository must be named
`<github-username>.github.io`).

## Files

| File | What it is |
|---|---|
| `index.html` | Home page: the list of apps, each with its privacy policy link |
| `style.css` | Shared look (light and dark) for every page |
| `app-ads.txt` | AdMob seller line. Must stay in the top folder. Put the website address in each Play listing (Store settings > Contact details > Website) so AdMob finds it |
| `.nojekyll` | Tells GitHub Pages to serve the files exactly as they are |
| `punch-game/privacy.html` | LaughLoop Punch Game privacy policy (master copy: `MaarGhasoona/docs/privacy-policy.html`) |
| `youtube/img/` | Channel banner and round LLS logo (WebP) for the YouTube box |
| `branding/` | Original full-size branding pictures (17 MB). Kept out of the website by `.gitignore`; make small WebP copies from them |
| `punch-game/img/` | Icon, banner and 2 screenshots (small WebP copies of `MaarGhasoona/docs/store`) used on the home page |

## Adding a new app

1. Make a folder with a short lowercase name, for example `arrows-puzzle/`.
2. Put the app's `privacy.html` in it. Copy `punch-game/privacy.html` as a start: keep the
   `../style.css` link and the back link, change the app name, what it stores, ads, purchases,
   permissions, contact email and the effective date.
3. Add the app to `index.html`: copy the `<article class="app">` block (banner, screenshots, icon, highlights, buttons) and put its pictures in `<folder>/img/` as WebP (about 1000 px wide).
4. If the app uses AdMob with the same AdMob account, `app-ads.txt` needs no change. A different
   ad network adds its own line.
5. Upload (commit and push). The page is live after about a minute at
   `https://<github-username>.github.io/arrows-puzzle/privacy.html`.

Privacy policy links to paste into Play Console (App content > Privacy policy, and the store listing):

- LaughLoop Punch Game: `https://<github-username>.github.io/punch-game/privacy.html`
