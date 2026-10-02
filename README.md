# Sky Match

A memory card-matching game that runs in a single HTML file. No build step, no dependencies.

## How to Play

1. Pick a difficulty: Easy (6 pairs), Normal (8 pairs) or Hard (12 pairs).
2. Flip two cards per turn.
3. If the symbols match, the pair stays face up. If not, both flip back.
4. Match every pair in as few moves as you can.

## Features

- Three difficulty levels with a responsive grid
- Move counter and timer
- Best score saved per difficulty in the browser (`localStorage`)
- 3D card flip animation, with reduced-motion support
- Keyboard accessible (Tab to a card, Enter or Space to flip)
- Automatic light and dark theme
- Works on desktop and mobile

## Tech

- HTML, CSS and vanilla JavaScript in one file
- No frameworks, libraries or external assets

## Getting Started

Download `skymatch.html` and open it in any modern browser. You can also serve it locally:

```bash
npx serve .
```

## Project Structure

```
.
├── skymatch.html   # markup, styles and game logic
└── README.md
```

## Customization

All changes are made in `skymatch.html`.

| What to change      | Where                                                         |
| ------------------- | ------------------------------------------------------------- |
| Card symbols        | `SYMBOLS` array in the script                                 |
| Difficulty levels   | `data-n` values on the level buttons (number of pairs)        |
| Colors              | CSS variables at the top of the `<style>` block               |
| Mismatch flip delay | The `800` ms timeout in the `flip` function                   |

The Hard level uses a 6-column grid. If you add more pairs, extend `SYMBOLS` so it has at least that many entries.

## Deployment

Because it is a static file, it can be hosted anywhere:

- **GitHub Pages:** rename the file to `index.html`, push, and enable Pages in the repo settings
- **Netlify or Vercel:** drag and drop the folder

## Ideas for Next Steps

- Two-player mode
- Sound effects
- Streak-based scoring
- Themed card sets (animals, flags, planets)

## License

MIT
