# Relay

<img src="https://raw.githubusercontent.com/iamjason/relay-site/main/assets/icon.png" width="128" height="128" alt="Relay's hand-off mark on a teal tile">

**Every link, handed to the right browser.**

Relay is a small macOS menu bar app that sends links to the browser you choose. Set Relay as your default browser once, then use the mark in your menu bar to decide where links open.

## Choose where a link goes

- **Always** — pick your usual browser and keep using it until you change your selection.
- **Next link** — send one link to a different browser, then return to your usual choice.
- **15 min** — switch browsers temporarily, with a countdown in the menu.
- **Hold Option** — choose a browser at your cursor. Use the arrow keys, a number key, or Return; Escape cancels. The modifier is configurable.

Relay discovers installed browsers, lists Chrome profiles as their own choices, remembers your selection, and can also forward local HTML documents. If a browser is unavailable, it asks you to choose another. It does not keep a browsing history. Five themes are included; Brasil is the default.

## Availability

Relay is **experimental** and requires **macOS 15 or later**. Visit the [website](https://iamjason.github.io/relay-site/) for availability and the latest download. Published builds are signed with Developer ID and notarized by Apple.

This repository contains Relay's public information, artwork, and Compendium manifest. The application source is maintained separately in a private repository. Relay was previously published as Kaepora; older download links redirect here.

## The woodland family

Relay grew up as Kaepora, named for the owl who offers guidance in *Ocarina of Time*, and it stays beside Deku and Korok in the [Hyrule Compendium](https://iamjason.github.io/hyrule-compendium-site/).

The Compendium discovers this repository through the `hyrule-tool` topic and uses [`hyrule.json`](hyrule.json) for its listing. Published releases will appear in the Compendium on its next refresh.

## Website publishing

This is a static GitHub Pages site served from `main` at the repository root, matching Deku and Korok. `.nojekyll` keeps the HTML and CSS unchanged.

From the separate Relay application checkout, `./relay update-site` refreshes the download block from the latest public release, and `./relay deploy` commits website changes, pushes them, and verifies the exact page is live. `./relay release [major|minor|patch|none]` builds, signs, notarizes, publishes the ZIP here, then updates and deploys the site. The updater reads this repository’s latest GitHub release.

## Usage statistics

This site records anonymous usage statistics: page views, download clicks and a daily visitor count derived from a hash of your IP address and browser. No cookies, no personal data, nothing stored in your browser. The collector is [Gossip Stone](https://github.com/iamjason/gossip-stone-swift#what-is-sent).
