# Dynamic Escapade

An interactive, arcade-inspired dance experience built with **HTML, CSS, JavaScript, and p5.js**. Explore six dreamlike worlds through portals, choose a soundtrack, and move a character to discover each world's hidden objective.

Originally developed as a collaborative interactive-design project by **Elise Chang and Prajanya Kannan**. This portfolio fork preserves the original project's history and contributors.

## Watch the demo and explore the design

**[Watch the full gameplay demonstration (Google Drive)](https://drive.google.com/file/d/1gWpuEJsmHOSwloHKTczhwsdhtDDkubiA/view?usp=sharing)** · **[View the illustrated project documentation (Google Docs)](https://docs.google.com/document/d/1E0lAbQ9h2jfGks_A9EogZ3yr-871Zwn4YiF5J2TI5to/edit)**

The demonstration shows the original interactive prototype in action. The documentation includes screenshots of all six themed worlds, animated portal transitions, the soundtrack-selection interface, and character gameplay, along with an explanation of the design process and implementation decisions.

These resources are viewable by anyone with their links. The demo video is hosted on Google Drive rather than embedded in the repository. The written documentation is also hosted on Google Drive and can be viewed without downloading the Git LFS media assets.

## How it works

- **Arcade-style navigation:** Animated title sequence, themed world selector, portal previews, and progress tracking.
- **Six playable worlds:** Beach, Candyland, Carnival, Concert, Mansion, and Paradise, each with its own visual theme and character accessory.
- **Interactive movement:** Drag the character or reposition its limbs to explore a world.
- **Hidden objectives:** A closeness meter helps guide the character toward a target. Completing a world requires reaching the target *and* moving at least one limb.
- **Soundtrack selection:** Choose between two tracks for each world; preview music before playing.
- **Transitions and state:** Canvas-based portal animations and browser session storage help connect the experience across pages.

## Tech stack

- **HTML, CSS, and vanilla JavaScript** for the interfaces and interactions
- **p5.js** for canvas-based character movement and gameplay
- **HTML Canvas / CSS animations** for transitions, visual effects, and navigation
- **sessionStorage** for remembering visited worlds within a browsing session
- **Git LFS** for game image and audio assets

## Run locally

1. Install [Git](https://git-scm.com/) and [Git LFS](https://git-lfs.com/).
2. Clone the repository and fetch its media assets:

   ```bash
   git clone https://github.com/elise-chang/Dynamic-Escapade-Arcade.git
   cd Dynamic-Escapade-Arcade
   git lfs install
   git lfs pull
   ```

3. Serve the project locally from the repository root:

   ```bash
   python3 -m http.server 8000
   ```

4. Visit `http://localhost:8000/` in a desktop browser.

No Node.js build step is required. The game loads p5.js from a CDN, so an internet connection is needed for that library.

**Media note:** The repository tracks large images and audio through Git LFS. If these files were not downloaded successfully, images, album art, and soundtracks will not load correctly. This README does not claim that all media assets or a hosted deployment have been tested.

## Project structure

| File or folder | Purpose |
|---|---|
| `index.html`, `script.js`, `style.css` | Intro and world-selection interface |
| `transition.html`, `transition.js`, `transition.css` | Animated transitions between screens |
| `world.html`, `world.js`, `world.css` | Shared gameplay and world-specific content |
| `background/`, `object/`, `accessory/`, `album/`, `audio/` | Visual and audio assets |

## Collaboration and media credits

This is a **team project**, originally created by Elise Chang and Prajanya Kannan. See the [original repository](https://github.com/praju-the-programmer2028/Dynamic-Escapade-Arcade) for its shared history.

The project includes third-party music and imagery. **Do not assume those assets are licensed for redistribution or public deployment.** Review their usage rights and replace unlicensed material with permitted assets before promoting or hosting a public playable version. The included `OFL.txt` documents the bundled font's license.

## Status

This repository represents the original interactive prototype. Core source code and documentation are available, but the full app, LFS downloads, and media rights still require verification before presenting it as a live demo.
