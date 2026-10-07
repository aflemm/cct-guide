# Shared documentation fragments

Store only genuinely identical, reusable Markdown here. This directory is excluded
from published pages and search; included text becomes part of its parent page.

Include a fragment from any page with:

```markdown
--8<-- "documentation-status.md"
```

Paths resolve from `docs/_shared`, configured through `pymdownx.snippets` in
`zensical.toml`. Missing fragments fail the build. Do not enable remote includes.
Keep fragment links relative to each including page, or avoid links in fragments
used at different depths. Keep product procedures in their product directories.
