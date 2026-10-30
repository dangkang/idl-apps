# idl-apps

App catalog and direct-sale pages for interdisciplinary design lab
(Satoru Tokuhisa, sole proprietorship). Live at https://apps.dangkang.com/.

## Structure

```
index.html        Japanese top page (apps + dCal direct sale)
tokusho.html      特定商取引法に基づく表記
terms.html        販売条件 (terms of sale for direct copies)
privacy.html      Privacy policy for the site and direct purchases
en/               English versions of the four pages above
assets/style.css  Shared stylesheet (based on dcal-web, idl red accent)
assets/apps/      App icons at 256 px
CNAME             Custom domain
_config.yml       Excludes repo notes from the published site
```

The Japanese top page lists dCal and Murray. The English top page also lists
Povie Booth, which is not sold in Japan.

## Hosting

GitHub Pages, branch `main`, folder `/ (root)`, with Enforce HTTPS on.
DNS is on VALUE-DOMAIN: `cname apps dangkang.github.io.`

## Direct sale

Checkout is Stripe Managed Payments (Link is the merchant of record).
Until the Payment Link exists, the buy button shows a pending state
(`.btn.pending`). Replace it with `<a class="btn primary" href="…">` in both
`index.html` and `en/index.html`.

## Local preview

```
python3 -m http.server 8000
```
