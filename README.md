# COMPAS documentation media

Figures and videos for the documentation of [COMPAS](https://github.com/scfpl-umich/COMPAS),
published at <https://scfpl-umich.github.io/COMPAS/>. They are kept here so that the history of
the COMPAS repository stays small.

- `figures/`: the images in the documentation pages and the README.
- `videos/`: the animations and their poster images.

## How COMPAS uses this repository

`docs/media.lock` in the COMPAS repository records the commit of this repository that its
documentation uses. `scripts/fetch_docs_media.sh` fetches that commit into `docs/media` before
the documentation is built, locally and by the documentation workflow:

```bash
bash scripts/fetch_docs_media.sh
sphinx-build -b html docs docs/_build/html
```

## Changing a figure or video

1. Open a pull request here that adds or replaces the file.
2. After it is merged, open a pull request in COMPAS that sets `docs/media.lock` to the new commit
   and updates the pages that use the file.

Commits of this repository that a COMPAS version uses must stay reachable, so the history of this
repository is never rewritten.

## License

Copyright (C) 2026 The Regents of the University of Michigan. Distributed under the same terms as
COMPAS: the GNU General Public License, version 3 or later, with the additional permission in
`COPYRIGHT`. See `LICENSE`.
