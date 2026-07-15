# orbit_sim

An interactive N-body gravitational simulator running in the browser. Built with Three.js and Vite.

## Controls

| Action | Effect |
|---|---|
| Click empty space | Add a body at that point |
| Click a body | Select it and show its attributes |
| Drag | Orbit the camera |
| Scroll | Zoom |

## How it works

Gravity is computed pairwise each step using Newton's law, `F = G·m₁·m₂ / r²`. Accelerations are accumulated for all bodies in one pass before positions are integrated in a second pass.

## Known limitations

- **No gravitational softening.** Two bodies passing very close produce a near-singular force and slingshot. Adding a softening term (`r² + ε²`) is on the list.
- **Presets carry net momentum**, so the system's center of mass drifts across the screen over time.
- **No collision handling** beyond the black hole's swallow behaviour.