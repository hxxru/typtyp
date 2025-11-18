# Development Log

## 2025-11-18

### Corpus Preset Switching
- Added support for multiple word corpus presets
- New corpora directory structure with three word lists:
  - `eng_adjectives.txt` - 21,000+ English adjectives (original corpus)
  - `scientific_jargon.txt` - 3,000+ scientific terms
  - `사자성어.txt` - 2,300+ Korean four-character idioms
- Implemented corpus selector dropdown in settings menu
- Dynamic corpus loading without page refresh
- Corpus-specific filtering:
  - English: filters hyphens, spaces, capitals
  - Scientific: allows hyphens, filters spaces and capitals
  - Korean: no filtering applied

## 2025-11-16

### Initial Implementation
- Created basic HTML/CSS/JavaScript structure for typtyp typing game
- Implemented core gameplay mechanics:
  - Words spawn at random horizontal positions
  - Words descend vertically at configurable speed
  - Text input box at bottom of screen
  - Exact match required to clear words
  - Fade/scale animation when words are cleared
- Added minimal styling with black background and white EB Garamond font
- Implemented game over condition when word reaches bottom
- Added score tracking and progressive difficulty
- Initial word list of ~50 common words

### Settings and Enhancements
- Updated README.md with comprehensive feature list and instructions
- Created devlog.md to track development progress
- Added settings menu with adjustable parameters:
  - Word speed multiplier (0.5x to 3x)
  - Average word length filter (short, medium, long, any)
- Integrated corpus.txt containing 20,000+ adjectives
- Implemented word filtering to exclude hyphenated words
- Settings persist during game session
- Added settings icon (gear) in top-left corner

## Technical Details

### Word Loading
- Words are loaded from corpus.txt at game initialization
- Filters out words containing dashes (hyphenated words)
- Word length categories:
  - Short: 1-5 characters
  - Medium: 6-8 characters
  - Long: 9+ characters
  - Any: All word lengths

### Difficulty System
- Base speed increases with score (every 50 points)
- User can adjust speed multiplier independently
- Word selection filters based on chosen length setting
- Progressive challenge while maintaining user control

### Design Philosophy
- Minimal, distraction-free interface
- No unnecessary UI elements during gameplay
- Focus on typography and smooth animations
- Settings accessible but non-intrusive
