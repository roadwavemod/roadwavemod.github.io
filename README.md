# roadwavemod.github.io

Landing page for **Roadwave Advanced** — the paid companion to the free Roadwave
mod for BeamNG.drive. Plain static HTML, no build step, no dependencies.

    index.html      the page
    buy.html        redirect to the store; exists so buy clicks are countable
    img/            screenshots, WebP, resized to 1400px
    img/_src/       the original PNGs, not served — keep, do not link

## Publishing

1. Create a free GitHub **organisation** named `roadwavemod`.
2. In it, create a **public** repository named exactly `roadwavemod.github.io`.
3. Push these files to the default branch.
4. Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/`.

Live at `https://roadwavemod.github.io` within a minute or two.

## Measurement — the reason this page exists

Every channel links here, never straight to a store. The funnel is then:

    channel → index.html → buy.html → Ko-fi / Patreon

`buy.html` is a redirect, so **buy-button clicks show up as page views of
`/buy.html`** in any plain page-view counter. No event tracking needed.

To turn counting on: create a free Cloudflare Web Analytics site (no card, no
cookies, the domain does not need to be on Cloudflare), then uncomment the
beacon at the bottom of `index.html` and `buy.html` and paste the token in.

Link per channel so arrivals can be attributed — the query string shows up in
the analytics as a distinct page:

    https://roadwavemod.github.io/?from=modland
    https://roadwavemod.github.io/?from=forum
    https://roadwavemod.github.io/?from=youtube
    https://roadwavemod.github.io/?from=reddit

Reading it later:

| visits | buy.html views | sales | what it means |
|---|---|---|---|
| 500 | 20 | 1 | the page or the offer does not convince |
| 500 | 150 | 1 | people want it; the checkout is the friction |
| 500 | 250 | 20 | it works |
| 20 | — | — | the links are not visible enough |

## Still to do

- Add the desktop-audio demo video. The markup is ready and commented out near
  the top of `index.html` — paste the YouTube id in and delete the comment.
- Add the Cloudflare beacon token.
