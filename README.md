# Curling Tools Product Guides

Static Markdown product guides built with [Zensical](https://zensical.org/docs/).
The site contains SmartBroom 4 and SmartBeam product guides, with a short Getting Started
flow, Essentials, and Beyond for each product.

## Repository structure

```text
zensical.toml                  Site settings and navigation
requirements.txt               Pinned Python dependencies
.github/workflows/pages.yml    Build and GitHub Pages deployment
overrides/partials/            Header, footer links, and automatic theme handling
docs/
  index.md                     Product chooser
  contact.md                   Support contacts and product guide links
  smartbroom/                  SmartBroom 4 hardware and iPhone/iPad workflows
  smartbeam/                   SmartBeam hardware and app workflows
  assets/images/               Real product photos, diagrams, and screenshots
  assets/stylesheets/brand.css Homepage, footer, logo contrast, and LED swatches
```

`.venv/`, `.cache/`, and generated `site/` output are ignored. Never commit them.

## Local development

Use Python 3.14 to match CI:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
zensical serve
```

Open <http://127.0.0.1:8000/cct-guide/>. The development server rebuilds and reloads
when source files change. Stop with Ctrl-C. Without activating the environment,
use `.venv/bin/zensical serve`.

Build the static output with:

```sh
.venv/bin/zensical build --clean --strict
```

Strict builds fail on warnings, including missing navigation destinations and
broken product guide links. Check the preview after changes to content or layout.
Dependencies are pinned in `requirements.txt`; update deliberately and repeat the
clean build and preview checks. No Node or Docker setup is needed.

## Writing product guides

Publish only verified product instructions. Keep unfinished notes outside `docs/`:
Markdown in that directory can be published and indexed even without a navigation
entry. Do not add placeholder pages or work-in-progress notices.

Keep hardware and app tasks together under the product directory. Each page
should have one H1 and descriptive H2/H3 headings. Use Getting Started for a short
flow linking to task pages; keep detailed instructions in one place and link to
them from other pages. Setting up Beams and Arming and Timing use clickable section titles for their
main pages, with focused sub-pages beneath them in the sidebar. Update incoming links when moving a
section to another page, and preserve meaningful anchors when editing headings.

Add every page explicitly to `project.nav` in `zensical.toml`. Link to Markdown
sources using relative paths, for example `[Charging](charging.md)` or
`[Beam alignment](beam-alignment.md#adjust-the-beam-height)`. Zensical converts
these to directory URLs. The standard theme provides breadcrumbs, page contents,
previous/next links, and mobile navigation.

Use the app's exact control labels in bold. Use Canadian spelling in prose,
including colour, centre, and metres. Distinguish beam-state, system-state, and
battery/charging LEDs. Colour swatches supplement readable colour names; never
rely on colour alone. Confirm product behavior from firmware, app source, or
official product material before documenting it.

To add a product, create its Getting Started and verified task pages, add its
navigation section and homepage product card, and add a product guide link on Contact.

## Images and screenshots

Store real assets in `docs/assets/images/` under the relevant product or app.
Use descriptive lowercase hyphenated filenames. Crop screenshots to the task,
remove personal information, and compress them. Use PNG for crisp screenshots,
JPEG/WebP for photos, and SVG for existing vector artwork. Give informative images
meaningful alt text and explain essential instructions in surrounding prose.

These product photographs were downloaded from the official website:

- `smartbroom/smartbroom-4.jpg`: <https://curling.tools/cdn/shop/files/smartbroom-4-three-quarters.jpg?v=1789582760&width=1000>
- `smartbeam/smartbeam-colours.jpg`: <https://curling.tools/cdn/shop/files/4-Colours_square.jpg?v=1773235161&width=1000>
- `smartbeam/rockarm.png`: <https://curling.tools/cdn/shop/files/rock-arm.png?v=1783628995&width=1000>
- `smartbeam/beam-height-adjustment.jpg`: <https://cdn.shopify.com/s/files/1/0679/4687/3014/files/smartbeam-height-adjustment.jpg?v=1790288051&width=1200> — from [Adjusting SmartBeam Laser Angle](https://curling.tools/blogs/support-articles/adjusting-smartbeam-laser-angle).

These are local assets, not hotlinked. Keep source URLs here when replacing them.

## Theme and search

`zensical.toml` configures the theme and navigation. The site follows the browser's
light/dark preference without a theme selector. The palette override discards old
manual choices; the header override shows “Product Guides” beside the official
wordmark. The footer provides sitewide support and main-site links.

The official logo source is:
<https://curling.tools/cdn/shop/files/Curling_Tools_Banner_-_Avenir_aebf3f35-6590-4ae1-972f-f5189ecd2b34.png?v=1744030618&width=600>.

`brand.css` handles the product chooser, footer, LED swatches, and wordmark contrast
in dark mode. Product guides retain the standard Zensical layout. System fonts
avoid hosted font requests. No custom frontend dependency is needed.

Built-in search indexes public product guide pages during the build. Its assets and
index ship with the static site; no external search service is required.

## GitHub Pages deployment

The workflow builds pull requests and pushes to `main`. Successful builds on
`main` upload `site/` and deploy through the `github-pages` environment. Manual
runs deploy only when the selected branch is `main`. A failed build blocks
deployment. GitHub Pages must use **GitHub Actions** as its source.

The configured sharing URL is <https://aflemm.github.io/cct-guide/>. The project
path is reflected in `site_url`, including local preview links. This configuration
does not confirm that a deployment has succeeded.

For the intended <https://guide.curling.tools/> domain, configure the custom domain
in repository Settings → Pages, complete GitHub's ownership and DNS verification,
then change `site_url` and redeploy. Follow GitHub's
[custom domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
and [custom workflow documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).

## SmartBroom content sources

SmartBroom 4 instructions were checked against the local `SmartBroom-iOS` and
`cct-esp32-firmware` repositories. Review these sources when behavior changes:

- App connection and ownership: `Views/SmartBroom/SmartBroomConnectedView.swift`,
  `BackgroundSweepingCollectionSheet.swift`, `SmartBroom/OwnershipManager.swift`,
  and `Data/Local Storage.swift` (remembered keys and iCloud sync).
- Live recording: `SmartBroom/LiveSweepController.swift` and
  `Views/Sweeps/Live Sweep Session View.swift`.
- Background storage permissions and live/storage exclusivity:
  `firmware/products/smartbroom/main/src/smartbroom.c`.
- Downloads and review: `SmartBroom/Downloader.swift`,
  `Views/SmartBroom/DownloadHistoryView.swift`, and `Views/Sweeps/Review/`.
- Raw captures: `Views/SmartBroom/RawLiveData/`,
  `SmartBroom/RawLiveDataController.swift`, and `docs/voyager_live_raw_protocol.md`.
- iPad windows: `App/SmartBroomApp.swift`, `App/WindowState.swift`,
  `App/AppState.swift`, and `Info.plist` (multiple scenes enabled).
- LEDs: `firmware/docs/smartbroom_led_indication.md` and
  `firmware/products/smartbroom/main/include/led_indications.h`.
- Settings and updates: `Views/Settings/PreferencesView.swift`,
  `Views/SmartBroom/SmartBroomDeviceView.swift`,
  `Views/SmartBroom/AutomaticFirmwareUpdateSheet.swift`, and
  `SmartBroom/OTAController.swift`.

The official [SmartBroom page](https://curling.tools/pages/smartbroom) confirms
USB-C charging. Apple's [iPad window guide](https://support.apple.com/guide/ipad/ipad8dfdf86b/ipados)
covers system window controls. Avoid using legacy SmartBroom 3 app instructions
as evidence for SmartBroom 4 workflows. No physical-device testing is implied by
these source checks.
