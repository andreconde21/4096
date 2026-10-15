# 4096

Personal fork of [gabrielecirulli/2048](https://github.com/gabrielecirulli/2048) — a small clone of [1024](https://play.google.com/store/apps/details?id=com.veewo.a1024), based on [Saming's 2048](http://saming.fr/p/2048/). 2048 was indirectly inspired by [Threes](https://asherv.com/threes/).

Gameplay is currently unchanged from upstream: join the numbers and get to the **2048 tile**. See `js/game_manager.js:170` for the win condition (`merged.value === 2048`).

Upstream was created by [Gabriele Cirulli](http://gabrielecirulli.com). This fork is maintained at [andreconde21/4096](https://github.com/andreconde21/4096).

## Run locally

Static site, no build step. Serve the repo root and open it in a browser:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Or just open `index.html` directly. `index.html:88-97` loads the game from `js/` with styles from `style/main.css`.

## How to play

Use the **arrow keys** (or swipe on mobile) to move the tiles. When two tiles with the same number touch, they **merge into one**.

## Project layout

- `index.html` — page markup
- `js/` — game logic (`game_manager.js`, `grid.js`, `tile.js`, `html_actuator.js`, `keyboard_input_manager.js`, `local_storage_manager.js`, polyfills, `application.js`)
- `style/main.scss`, `style/main.css` — styles (edit the SCSS, `main.css` is generated)
- `meta/`, `favicon.ico` — icons / mobile startup images

## Contributing

Changes and improvements are welcome. Fork and open a pull request against `master` in a specific branch, and make sure the game fully works before sending it. See [CONTRIBUTING.md](CONTRIBUTING.md) (upstream house rules: edit SCSS not CSS, 2-space JS indentation, `jshint` clean).

Upstream maintainers and notable contributors are credited in the git history and in the original README on `gabrielecirulli/2048`.

## License

MIT, see [LICENSE.txt](LICENSE.txt). Copyright (c) 2014 Gabriele Cirulli.
