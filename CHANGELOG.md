# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.1-beta.2] - 2026-06-19

### Added

- Optional GitHub repository link on the text-block toolbar (`showGithubLink`, `githubUrl` props; default on)
- GitHub Actions CI workflow (typecheck + build)
- `repository`, `homepage`, `bugs`, and `keywords` fields in `package.json`
- Expanded README with badges, `@beta` install instructions, exports table, and link to [amiriel.com](https://amiriel.com)

### Fixed

- CSS export path: `import "amiriel/style.css"` now resolves to `dist/style.css` correctly

## [0.0.1-beta.0] - 2026-06-19

### Added

- Beta channel release following `0.0.1-alpha.0`

## [0.0.1-alpha.0] - 2026-06-18

### Added

- Initial release of the portable Vue 3 letter body editor and renderer
- `AmirielBodyEditor` with page themes, fonts, text blocks, and drag-and-drop media
- `AmirielBodyRenderer` for read-only preview and delivery flows
- Media lightbox, inline video player, and video thumbnail components
- `media-request` event for host-controlled uploads
- English and Chinese label sets with optional overrides
- TypeScript types and document helpers

[0.0.1-beta.2]: https://github.com/dingdangdog/Amiriel/compare/v0.0.1-beta.0...v0.0.1-beta.2
[0.0.1-beta.0]: https://github.com/dingdangdog/Amiriel/releases/tag/v0.0.1-beta.0
[0.0.1-alpha.0]: https://github.com/dingdangdog/Amiriel/releases/tag/v0.0.1-alpha.0
