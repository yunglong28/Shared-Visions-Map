# Shared Visions // Solidarity Network Map

An interactive web-based visualization mapping global solidarity networks across fights, materials, spaces, and technologies.

## Overview

This project visualizes 19 organizations and initiatives working towards shared goals across Europe and globally. The interactive map shows geographical connections between nodes categorized into four domains:

- **Shared Fights & Struggles** (Red): Political and social movements
- **Shared Material & Logistics** (Green): Resource sharing networks
- **Shared Space** (Yellow): Physical community spaces
- **Shared Technologies** (Blue): Tech cooperatives and digital commons

## Files

- `shared-visions-solidarity-network.html` - Interactive visualization (standalone HTML file)
- `resources.csv` - Database of network nodes with geographical data

## Features

### Interactive Map
- Global projection using D3.js Natural Earth visualization
- 19 network nodes plotted by geographical coordinates
- Curved connection lines between nodes in the same category
- Smooth zoom and pan controls (0.5x to 20x)

### User Interactions
- **Hover** over sidebar items to zoom to locations
- **Click** markers or list items to visit organization websites
- **Keyboard navigation**: Arrow keys (↑↓), Enter, Esc, +/-, 0
- **Auto-reset**: Returns to overview after 2.5s of inactivity
- **Sound toggle**: Optional audio feedback (press S)

### Visual Effects
- Retro CRT aesthetic with scanlines and scan beam
- Animated orbital rings around the map
- Particle trail effects when navigating
- Pulsing markers with glow effects
- Responsive design for mobile and desktop

## Data Structure

The `resources.csv` database contains the following fields:

```csv
id,name,category,color,latitude,longitude,location,url
```

### Categories
- `fights` - Shared Fights & Struggles (#e63923)
- `material` - Shared Material & Logistics (#2e7d32)
- `space` - Shared Space (#f9a825)
- `tech` - Shared Technologies (#0277bd)

## Technical Architecture

### Core Technologies
- **D3.js v7.8.5**: Data visualization and geographic projection
- **TopoJSON v3.0.2**: World map topology data
- **Web Audio API**: Procedural sound generation
- **Canvas API**: Particle trail effects

### Map Rendering
1. Loads world topology from CDN (countries-110m.json)
2. Projects lat/lon coordinates using D3's Natural Earth projection
3. Renders land masses, graticule grid, and connection curves
4. Creates interactive SVG markers with multiple visual layers

### Animation System
- SVG-based zoom transformations with easing
- CSS animations for scanlines and orbital rings
- Canvas-based particle trails with alpha decay
- Web Audio API generates pentatonic scale tones

## Usage

### Viewing Locally
Simply open `shared-visions-solidarity-network.html` in a modern web browser. The visualization loads map data from CDN and runs entirely client-side.

### Keyboard Shortcuts
- `↑` / `↓` - Navigate through network nodes
- `Enter` - Open selected node's website
- `Esc` - Reset view to default
- `+` / `-` - Zoom in/out
- `0` - Reset zoom level
- `S` - Toggle sound on/off

### Data Updates
To add or modify network nodes, edit `resources.csv` and update the `entities` array in the HTML file (lines 899-919).

## Network Nodes

### Fights & Struggles (3)
- ANGA (Berlin)
- Art & Oppression (Global)
- Digital Sovereignty (Global)

### Material & Logistics (3)
- Offcut Network (Switzerland)
- Rebiennale (Venice)
- Woolshed (Alpine Region)

### Shared Space (5)
- BARN Brussels
- Level Five Cooperative (Brussels)
- KINlab (Milan)
- OT301 (Amsterdam)
- Amsterdam Alternative

### Technologies (8)
- LAUDS Factories (Europe)
- Fediverse (Global)
- Autonomic Cooperative (Bristol)
- Bread Cooperative (Manchester)
- Institute of Network Cultures (Amsterdam)
- lumbung.space (Indonesia/Global)
- Hackers & Designers (Amsterdam)
- Biblio-graph (Vienna)

## Design Philosophy

The visualization embodies the concept of networked solidarity through:
- **Geographical representation**: Showing real-world locations of initiatives
- **Category connections**: Visual links between related projects
- **Interactive exploration**: Allowing users to discover relationships
- **Aesthetic coherence**: Retro-futuristic design suggesting alternative infrastructures

> "If the network is the people — the revolution of infrastructure starts with you"

## Browser Compatibility

Tested on modern browsers supporting:
- ES6+ JavaScript
- SVG 2.0
- Web Audio API
- CSS Grid and Flexbox

Recommended: Chrome/Edge 90+, Firefox 88+, Safari 14+

## License

Data and visualization created for the Shared Visions project.

## Contributing

To add new network nodes:
1. Add entry to `resources.csv` with accurate coordinates
2. Update the `entities` array in the HTML file
3. Update the category counts in the sidebar
4. Test zoom and interaction behaviors

## Credits

Visualization design and development: Claude Sonnet 4.5
Project: Shared Visions Solidarity Network Infrastructure
