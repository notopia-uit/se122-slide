# Notopia slides

A Slidev presentation based on `se121-slide/`, retaining its academic theme,
components, assets, tooling, and page structure without the original slide content.

## Getting started

Use the Node.js version in `.tool-versions` and pnpm 10.33.4 (also pinned in
`package.json`). With mise installed, run `mise trust` and `mise install`.

```sh
pnpm install
pnpm dev
```

Open <http://localhost:3030>.

## Editing slides

- `slides.md`: deck settings, cover, table of contents, and page imports.
- `pages/`: placeholder sections using the reference project's filenames.
- `components/`: reusable Vue components, copied unchanged.
- `public/`: shared logos and images, copied unchanged.
- `style.css`: shared styling, copied unchanged.
- `.agents/`: the reference project's Slidev skill.

Replace the placeholder content and update the title, author, and export filename
in `slides.md`. The UI showcase is optional and is not imported by default.
The reference project in `se121-slide/` is unchanged.

## Build and export

```sh
pnpm build
pnpm export
```

The static site is written to `dist/`; PDF export creates `notopia-slide.pdf`.
If Chromium is missing, run `pnpm exec playwright install chromium` first.

The copied GitHub Actions workflow builds and deploys GitHub Pages under
`/notopia-slide/` and attaches the PDF to tagged releases. Change its `--base`
path if your repository has a different name.

Learn more at <https://sli.dev/>.
