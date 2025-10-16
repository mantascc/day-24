# RPS Agent Simulation

A minimal Rock-Paper-Scissors agent-based simulation where colored agents move randomly and convert each other based on collision outcomes.

## Rules

- **Rock (blue)** beats **Scissors (green)**
- **Scissors (green)** beats **Paper (red)**
- **Paper (red)** beats **Rock (blue)**

When two agents of different types collide, the loser converts to the winner's type.

## Implementation

- 300 agents, each rendered as 2x2 pixels
- Random wandering behavior with small directional jitter
- Toroidal wrapping (agents wrap around screen edges)
- Collision radius: 8 pixels
- Dark mode aesthetic

## Usage

Open `index.html` in any modern browser.

**Controls:**
- **Pause/Play** - Stop or resume the simulation
- **Reset** - Regenerate all agents with random positions and types

## Technical Details

- Single HTML file with embedded CSS and JavaScript
- Canvas-based rendering using requestAnimationFrame
- O(n²) collision detection (optimized for <500 agents)
- Conversions applied after collision detection to prevent chain reactions within a single frame
