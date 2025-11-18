# typtyp

A minimal typing game where words descend down the screen and you type them to clear them before they reach the bottom.

## Features

- **Minimal Design**: Black background, white EB Garamond text
- **Progressive Difficulty**: Words fall faster as you score higher
- **Settings Menu**: Customize word speed, corpus preset, and word length
- **Multiple Word Corpora**: Choose from English adjectives, scientific jargon, or Korean idioms (사자성어)
- **Score Tracking**: See how long you can survive
- **Smooth Animations**: Simple fade effects when words are cleared

## How to Play

**Important**: Due to browser security restrictions, you must run a local web server to play the game. You cannot open `index.html` directly with `file://`.

**Start the game:**
```bash
# In the typtyp directory, run:
python3 -m http.server 8000

# Then open your browser to:
# http://localhost:8000
```

**Gameplay:**
1. Words will begin falling from the top of the screen
2. Type each word exactly as it appears in the input box at the bottom
3. Press Enter or continue typing to clear matched words
4. Don't let any word reach the bottom or it's game over!
5. Click the settings icon (⚙) to adjust difficulty

## Gameplay and Design

Minimal, black background, white text. Font: EB Garamond.

Descending text has no bounding boxes. Text entry box at bottom of the screen with visible cursor. Simple animation when a word is cleared by typing. Match must be exact.

## Settings

- **Word Speed**: Adjust how fast words descend (0.5x to 3x)
- **Word Corpus**: Choose your word list preset
  - English Adjectives (20,000+ words)
  - Scientific Jargon (3,000+ terms)
  - 사자성어 - Korean four-character idioms (2,300+ phrases)
- **Word Length**: Filter words by length (short, medium, long, any)
- **Zen Mode**: Disable game over for relaxed practice
