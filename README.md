# Curling Tools User Guide

One Markdown documentation repository for Curling Tools products, built with
[Zensical](https://zensical.org/docs/). The published output is fully static:
HTML, CSS, JavaScript, images, and a local search index. No application server,
database, CMS, or hosted search service is needed.

## Repository structure

```text
zensical.toml                  Site settings, navigation, theme, extensions
overrides/                     Small override to discard saved manual themes
requirements.txt               Pinned Zensical and transitive dependencies
.github/workflows/pages.yml    Build checks and future Pages deployment
README.md                      Contributor guide (not published)
docs/
  index.md                     Product chooser
  smartbroom/                  Unified product manual and landing page
    connecting-smartbroom.md, sessions.md, charts.md, video.md, settings.md
    troubleshooting/           SmartBroom troubleshooting
  smartbeam/                   Unified product manual and landing page
    connecting-smartbeam.md, setting-up-beams.md, arming-and-timing.md,
    understanding-results.md, history-and-data.md, settings.md
    troubleshooting/           SmartBeam troubleshooting
  contact.md                   Contact details and troubleshooting links
  assets/images/
    smartbroom/                SmartBroom photos, diagrams, annotations
    smartbroom-app/            SmartBroom app screenshots
    smartbeam/                 SmartBeam photos, diagrams, annotations
    smartbeam-app/             SmartBeam app screenshots
    shared/                    Approved logo, favicon, shared illustrations
  assets/stylesheets/brand.css Homepage layout and wordmark contrast
  _shared/                     Source-only reusable Markdown fragments
.venv/                         Local Python environment (ignored)
.cache/                        Zensical build cache (ignored)
site/                          Generated static output (ignored)
```

## Local development

Use Python 3.14 to match CI (the initial local verification used Python 3.14.7).
From the repository root:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
zensical serve
```

Open <http://127.0.0.1:8000/>. The preview rebuilds and reloads when Markdown or
configuration changes; stop with Ctrl-C. It is a development server only.
To run without activating the environment, use `.venv/bin/zensical serve`.

Build the deployable output:

```sh
source .venv/bin/activate
zensical build --strict
```

Or use `.venv/bin/zensical build --strict`. Generated files appear in `site/`.
Strict builds fail on warnings, including missing navigation destinations and
broken links. Use `zensical build --clean --strict` after changing dependencies.
Never commit `site/`, `.cache/`, `.venv/`, or Python bytecode.

`requirements.txt` pins Zensical and all installed transitive dependencies.
To upgrade deliberately, update Zensical in the virtual environment, review
`python -m pip freeze`, update the pins, and repeat build and preview checks.
No Node, Docker, or additional build system is used by this project.

## Writing documentation

Create a focused `.md` page within the relevant product or its troubleshooting
folder. Use one H1, then descriptive H2/H3 headings in order. Add it explicitly to
`project.nav` in `zensical.toml`, and link to source Markdown using relative paths:

```markdown
[Charging](charging.md)
[Sessions](sessions.md)
```

Zensical converts these to directory URLs, e.g. `smartbroom/sessions/`.
Hardware and app tasks are one product experience: keep task pages directly
under their product, with no separate app section or `app/` folder.
Top-level tabs are Home, SmartBroom, SmartBeam, and Contact; the left sidebar
contains the active section's documentation tree. Section index pages are first
in their section's navigation list. Breadcrumbs, page TOCs, previous/next links,
and responsive mobile navigation use the standard theme.

All current technical pages contain clearly marked placeholders. Replace them
only with verified Curling Tools content. Do not infer specifications, device
compatibility, button behavior, charging, Bluetooth, firmware or reset procedures,
warranty terms, safety notices, or contact details. Remove the shared
`documentation-status.md` include from a page once its content is complete.

### Add a product

Create `docs/newproduct/getting-started.md` and task pages such as
`connecting-newproduct.md`, `measurements.md`, and `settings.md` directly within
the product directory. Add a `troubleshooting/` subdirectory with its own
`index.md`. Keep hardware and app workflows together in the product navigation.
Add one top-level `project.nav` section following the existing product pattern.
Add a product card to `docs/index.md`, troubleshooting links to Contact, and
`docs/assets/images/newproduct/` and `newproduct-app/` as needed. There is no fixed
product count or product-specific code to change.

### Images and screenshots

Store real, approved assets in the matching `docs/assets/images/` directory.
Use descriptive lowercase hyphenated filenames (for example,
`session-chart-ios.webp`); distinguish platform/version only when it matters.
Crop screenshots to the relevant task, remove personal information, resize to
useful display dimensions, and compress them. Use PNG for crisp screenshots,
WebP/JPEG for photos, and SVG for approved vector diagrams or branding.

Link relative to the page:

```markdown
<!-- Example from docs/smartbroom/charts.md; add the actual file first. -->
![Describe the chart labels and relevant highlighted controls](../assets/images/smartbroom-app/session-chart-ios.png)
```

Every informative image needs meaningful alt text. Explain essential visual
instructions in the surrounding prose as well; do not rely only on color.
Hardware placeholder pages contain commented image placement examples, so no
missing or fake imagery is displayed. `.gitkeep` files preserve empty folders.

The homepage product photographs were downloaded from the official website:

- `smartbroom/smartbroom-4.jpg`: <https://curling.tools/cdn/shop/files/smartbroom-4-three-quarters.jpg?v=1789582760&width=1000>
- `smartbeam/smartbeam-colours.jpg`: <https://curling.tools/cdn/shop/files/4-Colours_square.jpg?v=1773235161&width=1000>

These are local assets, not hotlinked. Keep source URLs here when replacing them.

### Shared fragments

Place genuinely identical reusable text in `docs/_shared/`, then include it:

```markdown
--8<-- "documentation-status.md"
```

The supported `pymdownx.snippets` extension resolves paths from `docs/_shared`;
missing includes fail builds. Fragments are excluded from standalone pages and
search, but their included text is indexed in the parent pages. Avoid relative
links in fragments reused at different depths. Keep each product's charging and
other procedures within that product. See `docs/_shared/README.md` for details.

## Theme, branding, and search

Configuration is in `zensical.toml`. `project.theme.logo` uses the official
wordmark downloaded from the [Curling Tools website](https://www.curling.tools/).
The source asset is:

<https://curling.tools/cdn/shop/files/Curling_Tools_Banner_-_Avenir_aebf3f35-6590-4ae1-972f-f5189ecd2b34.png?v=1744030618&width=600>

`project.extra.homepage` links the header/sidebar logo to the main website;
the Home tab still opens the guide. `brand.css` adds a white background behind the wordmark in dark mode to preserve
its original colors and readability. It also scopes the homepage layout to
`.guide-home`; product manuals keep the standard theme. The homepage uses locally
stored official SmartBroom and SmartBeam photos in two linked product cards,
with an explicit main-site link and support area. No custom JavaScript or
frontend dependency is used for this layout.
The favicon path remains commented until an approved file is supplied.
Change `primary` and `accent` in the light/dark palette entries for brand colors.
The guide follows the browser’s appearance preference, including changes while
the page is open, with no theme selector. The small palette initialization
override discards any previously saved manual theme choice so it cannot override
the browser. System fonts avoid hosted font requests. Commented
`project.extra.social` marks where approved contact/social links belong.
The repository link is intentionally omitted from the customer-facing header.

Zensical's built-in browser search indexes all public Markdown pages across all
products during the build. It ships its own local search assets/index, with no
Algolia or external search server. Search for `SmartBroom`, `SmartBeam`, or a
specific topic in the preview; results should span the corresponding pages.

## Future GitHub Pages deployment

The workflow uses GitHub's artifact-based Pages deployment, not a generated
`gh-pages` branch. Pushes to `main` build with `zensical build --strict`, upload
only `site/`, and deploy through the `github-pages` environment. Pull requests
build only. Manual workflow runs deploy only when the selected branch is `main`.
A failed build blocks upload/deployment. The deployment job uses scoped
`pages: write` and `id-token: write` permissions and needs no custom secret.

The configured repository is `aflemm/cct-guide`; the temporary sharing URL is
<https://aflemm.github.io/cct-guide/>. This is the configured destination, not
confirmation of a successful deployment. To publish:

1. Create or select the GitHub repository and confirm its default branch is
   `main` (or update the workflow branch settings).
2. Enable Pages with **GitHub Actions** as the source, and allow the Actions and
   `github-pages` environment deployment permissions required by your repository.
3. Keep repository details in this README; the public header omits the repo link.
4. Push only when ready for the workflow to publish.

The current `site_url` is `https://aflemm.github.io/cct-guide/` so the initial
publication works under the GitHub project path. The intended production domain
is `https://guide.curling.tools/`; restore `site_url` to that address and redeploy
when the custom domain is connected.

### Connect guide.curling.tools later

In repository Settings → Pages, set the custom domain to `guide.curling.tools`.
Verify ownership as GitHub recommends, then create a DNS CNAME for `guide` pointing
to the **actual GitHub Pages hostname**, `OWNER.github.io` (not the repository
path). Use the values GitHub provides for the chosen account and domain. Once
DNS and the certificate are ready, enable **Enforce HTTPS** and check the domain.

For this custom Actions deployment, GitHub configures the domain in Pages
settings; a source `CNAME` file is not required and is intentionally absent.
No DNS provider or GitHub account is assumed. See GitHub's current
[custom domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
and [custom workflow documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).

## Content still needed

Supply approved hardware and app instructions, troubleshooting and reset steps,
firmware procedures, screenshots/photos, favicon, and brand colors. The placeholder content provides
structure only and makes no technical product claims.
