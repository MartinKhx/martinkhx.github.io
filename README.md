# martinkhx.github.io

Developer website for Martin Khachatryan, served by GitHub Pages at
<https://martinkhx.github.io/>. This root is the developer website listed on
both store listings for Loop Dodge (Apple App Store and Google Play).

## app-ads.txt — do not remove, rename or move

`app-ads.txt` must stay at the site root and must be reachable at exactly:

    https://martinkhx.github.io/app-ads.txt

### What it is

`app-ads.txt` (Authorized Sellers for Apps, an IAB Tech Lab standard) is a plain
text file a mobile app developer publishes on their developer website. Ad
crawlers — including Google's `Google-adstxt` crawler — take the developer
website URL from the app's store listing, fetch `/app-ads.txt` from it, and read
the list of ad publisher accounts that are authorized to sell inventory for that
developer's apps. An account not listed there cannot be verified, and ad demand
for the apps is reduced or refused.

### Current content

    google.com, pub-7307963416790245, DIRECT, f08c47fec0942fa0

The publisher id **must stay `pub-7307963416790245`** — this is the AdMob
publisher account for the Loop Dodge apps. Changing it, or dropping the line,
breaks verification for both the iOS and the Android app.

### Rules

- Never delete, rename or move `app-ads.txt`. It has to be at the site root.
- Never change `pub-7307963416790245` unless the AdMob publisher account itself
  changes.
- Serve it as plain text over HTTPS (GitHub Pages already does; `http://`
  redirects to `https://`).
- Keep the developer website field in **both** store listings pointing at the
  site root `https://martinkhx.github.io/` — not at a sub-page. Crawlers only
  look at `<developer website>/app-ads.txt`, so a sub-page URL hides the file.
- `robots.txt` must keep allowing `*` and `Google-adstxt`.

Add further `google.com, pub-…, DIRECT|RESELLER, <cert id>` lines only when a new
authorized ad network is genuinely added.
