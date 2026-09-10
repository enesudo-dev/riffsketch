# RiffSketch

**Capture the riff before you forget it.**

RiffSketch is a lightweight, browser-based guitar riff sketchpad designed for quickly turning an idea into a playable sequence and ASCII TAB — without opening a DAW or full tablature editor.

The project focuses on speed, simplicity, and direct interaction: choose a tuning, enter fret numbers on a six-string grid, play the riff back, and copy the generated TAB.

## Features

- **6-string guitar sequencer**
- **0–24 fret support**
- **Multiple tunings**
  - E Standard
  - D Standard
  - Drop D
  - C Standard
- **8-step and 16-step patterns**
- **Chord and power-chord support** by placing notes on multiple strings in the same step
- **Direct keyboard fret entry**
- **Arrow-key navigation** across the grid
- **Muted notes (`X`)**
- **Delete / Backspace to clear notes**
- **Adjustable BPM**
- **Web Audio API playback**
- **Automatic ASCII TAB generation**
- **Copy TAB to clipboard**
- **Random riff idea generator**
  - Natural Minor
  - Phrygian
  - Chromatic
- **Local persistence with `localStorage`**
- **Responsive layout with horizontal sequencer scrolling**

## Keyboard Controls

| Key | Action |
| --- | --- |
| `0–24` | Enter fret number |
| `←` `→` | Move between steps |
| `↑` `↓` | Move between strings |
| `X` | Add muted note |
| `Delete` / `Backspace` | Clear selected cell |
| `Space` | Play / Stop |
| `Esc` | Deselect current cell |

## How It Works

RiffSketch represents a guitar riff as a six-row step sequencer. Each row corresponds to a guitar string and each column represents one sixteenth-note step.

The application calculates pitch from the selected tuning and fret position, then schedules playback using the Web Audio API. The same grid is also converted into aligned ASCII guitar TAB in real time.

Everything currently runs entirely in the browser. No account, backend, or database is required.

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Web Audio API
- Web Storage (`localStorage`)

The project intentionally avoids frameworks and backend infrastructure to keep the application small, portable, and easy to run.

## Running Locally

Clone the repository:

```bash
git clone https://github.com/enesudo-dev/riffsketch.git
cd riffsketch
```

Then open `index.html` in a modern browser.

No package installation or build step is required for the current version.

## Project Status

RiffSketch is an ongoing experimental project.

The current version focuses on the core riff-writing workflow: note entry, navigation, tuning support, playback, and TAB export.

The audio engine is still a prototype. A future version is planned to replace the current synthesized preview with a higher-quality, multi-sampled guitar playback system for clearer and more realistic note articulation.

## Roadmap

Planned improvements include:

- Multi-sampled guitar playback
- Better palm-muted and dead-note articulation
- Longer patterns and pattern chaining
- Note duration / sustain controls
- Improved riff generation
- Save / load multiple riffs
- Export options beyond plain ASCII TAB
- Additional tunings
- Further mobile usability improvements

## Development

RiffSketch was developed as an AI-assisted software project using **Claude** and **OpenAI Codex** as coding collaborators for planning, implementation, iteration, debugging, and refinement.

The project is also an experiment in using AI tools to rapidly prototype a practical utility around a real creative workflow.

## Author

**Enes Burak Yazan**  
Bursa Uludağ University

## License

Source-code licensing has not yet been finalized.

If third-party audio assets are added in future versions, their redistribution and attribution requirements will be documented separately before they are included in the public repository.
