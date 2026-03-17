# Spider Spite

You are a spider. You have chosen the worst possible place to take a stroll.

## What is this

A browser-based survival game rendered in isometric pseudo-3D. You play as a spider navigating across a sleeping human. The human is large. You are small. The human occasionally swats. You do not want to be where the hand lands.

## How to play

Play at **[spiderspite.com](https://spiderspite.com)** or open `index.html` locally. No build step, no dependencies, no regrets.

**Controls:**

| Key | Action |
|-----|--------|
| `WASD` / Arrow Keys | Move |
| `Shift` | Creep (slower, quieter) |
| `Space` | Start / Retry |

## The mechanics

The sleeping human has a **Wake Meter**. It fills when you move across their body. It drains when you're still or off the body. Fill it to 100% and they wake up. Game over.

Not all parts of the body are equally dangerous:

| Zone | Sensitivity |
|------|-------------|
| Face | Extreme — tread very carefully |
| Chest | High |
| Belly | Medium |
| Legs | Low |
| Mattress (off body) | Safe — rest here |

Every few seconds the human feels something and **swats**. A pulsing orange warning zone appears — that's where the hand is coming. Move out of it before the hand comes down. The warning window gets shorter as time goes on.

**Strategy:** Hold `Shift` near the face. Sprint across the legs. Retreat to the mattress to let the wake meter drain between runs.

## Tech

Single HTML file. Vanilla JavaScript with HTML5 Canvas. The isometric projection is a standard 2D affine transform applied to the canvas context, so all world-space geometry (spider legs, swat zones, the body) projects naturally onto the bed surface without separate screen-space math.

## Tips

- The human's brow furrows as the wake meter climbs. That's your cue to stop moving.
- Swats are targeted toward wherever the spider was last detected on the body. You can bait them to a spot and dodge.
- The pillow area is safe. The face directly below it is not.

---

*There is no winning. There is only surviving.*
