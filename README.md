# Curling Tools Product Guides

Product guides for SmartBroom 4, SmartBeam, CoreBroom, LightBroom, and RockArm, built with
[Zensical](https://zensical.org/docs/).

[Read the product guides](https://docs.curling.tools/) ·
[Visit Curling Tools](https://curling.tools/) ·
[Contact support](https://curling.tools/pages/contact)

## Local development

Use Python 3.14:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
zensical serve
```

Open <http://127.0.0.1:8000/>. The preview reloads when source files
change. Stop it with Ctrl-C.

Build the static site with:

```sh
zensical build --strict
```

Generated files appear in `site/`. Do not commit generated output, `.venv/`, or
`.cache/`. Dependencies are pinned in `requirements.txt`.

## Contributing

Product pages live under `docs/smartbroom/`, `docs/smartbeam/`,
`docs/corebroom/`, `docs/lightbroom/`, and `docs/rockarm/`. Navigation and
site settings are in `zensical.toml`. Shared broom care and competition pages
live under `docs/broom-basics/` so product guides can reference the same content.
CoreBroom includes the shared Broom Basics sections with `pymdownx.snippets`.
LightBroom shares the sleeve-replacement content and has its own Competition Use
page explaining its certification status. Shared content stays in one place
while navigation remains within each product guide.

- Publish verified instructions and use the app's exact control labels.
- Keep product instructions in these guides and link to the relevant guide pages rather than legacy support articles.
- Keep Getting Started concise and link to focused task pages for detail.
- Use one H1 per page and descriptive H2/H3 headings.
- Add published pages to `project.nav` and use relative Markdown links.
- Update incoming links when moving pages or sections.
- Use Canadian spelling, including colour, centre, and metres.
- Give informative images meaningful alt text; do not rely on colour alone.
- Run a strict build and check the preview before submitting changes.

### Draft pages

Name an unfinished page `*.draft.md`, or place it under `docs/drafts/`.

`zensical serve` includes drafts with a DRAFT notice. Open them by URL, such as
`/smartbeam/new-topic.draft/`; they are not added to the sidebar
automatically. `zensical build` excludes drafts from HTML output, search, and
the sitemap.

Keep draft-only assets under `docs/drafts/` so they are excluded from the build
too. To publish, remove `.draft` from the filename or move the page and its assets
out of `drafts/`, update links, and add the page to navigation.

Draft exclusion applies to the generated site only. Drafts committed to this
public repository remain visible here.

### Images

Store images under `docs/assets/images/` in the relevant product or app folder.
Use descriptive filenames, crop screenshots to the task, remove personal
information, and compress images before adding them.

Product photographs, the beam-adjustment image, and branding come from the
official [Curling Tools website](https://curling.tools/).

CoreBroom, LightBroom, and RockArm photos are sourced from the official product pages:
[CoreBroom](https://curling.tools/pages/corebroom),
[LightBroom](https://curling.tools/products/lightbroom), and
[RockArm](https://curling.tools/products/rockarm).

LightBroom animations are copied locally from the official
[rainbow sparkle](https://curling.tools/cdn/shop/files/lightbroom-sparkle-rainbow.webp?v=1789602350)
and [Cylon](https://curling.tools/cdn/shop/files/lightbroom-cylon.webp?v=1789602039)
assets. Both URLs serve animated GIF data, stored here with `.gif` extensions.

### LightBroom operating instructions

Operating behaviour was checked against the local `cct-esp32-firmware` checkout
at commit `5eb0486` (product `firmware/products/inner-light`). Sources include
`main/src/led_controller.c` (button actions and display timing),
`main/src/system_controller.c` (sleep, wake, and saved colour),
`main/src/led_render_soc.c` (battery bar),
`main/src/led_render_general.c` (motion and sparkle),
`main/include/led_render_colour_picker.h` (colour order), and
`main/include/config.h` (hold timing and low-charge wake cutoff).
These pages describe the physical controls; Bluetooth protocol features do not
establish a supported customer app workflow.
