# RPS Agent Simulation

A minimal Rock-Paper-Scissors agent-based simulation where agents move randomly, collide, and convert each other based on RPS rules.

## Features

- **66 agents** with image sprites (rock, scissors, paper)
- **Rotating sprites** that continuously spin as they move
- **Bounce physics** - agents physically bounce away from each other on collision
- **Bounding box collision detection** using actual image dimensions
- **Win state** - simulation ends when one species dominates
- **Mobile-friendly** - automatically scales images to 50% on smaller screens
- **Minimal dark mode UI** with live population counter

## Rules

- **Rock** beats **Scissors**
- **Scissors** beats **Paper**
- **Paper** beats **Rock**

When two agents collide, they bounce away from each other and the loser converts to the winner's type.

## Usage

Open `index.html` in any modern browser.

**Controls:**
- **Pause/Play** - Stop or resume the simulation
- **Reset** - Regenerate all agents with random positions and types
- **Play again** - Restart after a win (appears in victory overlay)

## Technical Details

- Single HTML file with embedded CSS and JavaScript
- Canvas-based rendering using `requestAnimationFrame`
- AABB (Axis-Aligned Bounding Box) collision detection
- Toroidal wrapping (agents wrap around screen edges)
- Elastic collision physics with constant speed maintenance
- Workbench font for victory message
- Responsive design with mobile optimizations (≤768px)
