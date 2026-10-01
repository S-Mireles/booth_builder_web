# Booth Builder (Web)

The Web build of Booth Builder, Robinson Show Services' trade-show booth planner, served by GitHub Pages at
https://s-mireles.github.io/booth_builder_web/.

It runs in desktop and tablet browsers. Its catalogue of items loads from
https://s-mireles.github.io/booth_builder_catalogue/ each time it starts, and each item's 3D model downloads the first
time it's needed.

## These files

Don't edit them by hand. They're the app's Web export, made with Godot 4.7.2 from Robinson Show Services' source
repository: to update the app, export it again and replace them.

- `index.html`, `index.js`: the page and the engine's loader.
- `index.wasm`: the engine.
- `index.pck`: the app.
- `index.*.png`, `index.*.js`: icons and audio helpers.
- `.nojekyll`: makes Pages serve the files as they are.

## Hosting requirements

- Any static web host. The build is single-threaded, so it needs no special headers (no COOP or COEP).
- `.wasm` files served as `application/wasm`, as GitHub Pages does.
- HTTPS, so browsers keep the catalogue's downloads between visits.
- The catalogue's address must allow requests from this site. GitHub Pages sends `Access-Control-Allow-Origin: *`, and
  both sites are on the same address anyway.

## Licence

Copyright © 2026 Robinson Show Services. All rights reserved. See [LICENSE.md](LICENSE.md), and
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for the third-party software it includes.
