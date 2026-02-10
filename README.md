# Blood & Dust Campaign Hub

A Jekyll-based static site for the Blood & Dust TTRPG campaign, featuring a gladiatorial/ancient Rome aesthetic.

## Overview

This repository hosts the campaign hub for **Blood & Dust**, a Mythras Imperative campaign set in the brutal Grand Arena of ancient Obusia, where gladiators fight for survival, glory, and freedom.

## Features

- **Public Player Content:**
  - Rules & Info: Mythras Imperative mechanics and resources
  - World: Setting, revealed NPCs, locations, and factions
  - Sessions: Chronological session summaries
  
- **Private GM Content:**
  - Accessible via obscured URL (`/gm-vault-32f8a9/`)
  - Campaign planning and arc notes
  - Hidden NPCs and secret motivations
  - World secrets and mythic revelations
  - Not indexed by search engines (via robots.txt)

- **Theme:**
  - Ancient arena/Roman aesthetic
  - Earth tones: sand, iron, marble, faded gold
  - Classical typography and weathered styling
  - Mobile-responsive design

## Local Development

### Prerequisites

- Ruby 3.1 or higher (Ruby 3.1 tested, newer versions should work)
- Bundler gem

### Setup

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

The site will be available at `http://localhost:4000`

## Project Structure

```
.
├── _config.yml           # Jekyll configuration
├── _info/                # Rules and mechanics (public)
│   ├── mechanics/        # Mythras mechanics explanations
│   └── cheat-sheets/     # Quick reference sheets
├── _world/               # Campaign world content (public)
│   ├── npcs/             # Non-player characters
│   ├── locations/        # Places in Obusia and the arena
│   └── factions/         # Organizations and groups
├── _sessions/            # Session summaries (public)
├── _gm/                  # GM-only content (private URL)
│   ├── planning/         # Campaign and session planning
│   ├── npcs/             # Secret NPC information
│   └── secrets/          # Hidden world lore
├── assets/css/           # Custom styling
├── index.md              # Home page
├── info.md               # Rules landing page
├── world.md              # World landing page
├── sessions.md           # Sessions landing page
└── gm-notes.md           # GM vault landing page
```

## Adding Content

### Public Content

Create new markdown files in the appropriate collection folder:

**NPC Example:**
```markdown
---
layout: page
title: Character Name
topic: NPCs
summary: Brief description
---

# Character Name

Full content here...
```

**Session Example:**
```markdown
---
layout: page
title: Session Title
index: 1
summary: Brief summary
---

# Session 1: Title

Full session summary...
```

### GM Content

Same structure, but place files in `_gm/` directory. These will be published at the obscured URL but won't appear in navigation or search engine indexes.

## Deployment

The site automatically deploys to GitHub Pages via GitHub Actions when changes are pushed to the `main` or `master` branch.

### GitHub Pages Setup

1. Go to repository Settings → Pages
2. Set Source to "GitHub Actions"
3. The workflow in `.github/workflows/pages.yml` handles the rest

## Theme Customization

The site uses Jekyll's Minima theme with extensive customization in `assets/css/style.scss`. Color scheme and styling can be adjusted there to match the gladiatorial/ancient Rome aesthetic.

## Contributing

This is a private campaign repository. If you're a player, please don't peek at the `_gm/` folder—spoilers ahead!

## License

Campaign content is private. The Jekyll structure and theme are based on open-source components.

## Credits

- Built with [Jekyll](https://jekyllrb.com/)
- Theme based on [Minima](https://github.com/jekyll/minima)
- Powered by [Mythras Imperative](https://www.thedesignmechanism.com/)
- Structure inspired by [Vaultlight](https://github.com/JakeAO/Vaultlight)
