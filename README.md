# Ellie Killer 🎯 (Squeak & Seek)

## Basic Details
### Team Name: pseudocoders

### Team Members
- Team Lead: Abhin Joe Saji - Vimal Jyothi Engineering College
- Member 2: Jis John Sajan - Vimal Jyothi Engineering College

## Project Description
**Ellie Killer** is a gloriously useless WebXR augmented-reality game where a virtual rat scurries around your *actual* room, your floating AI dog companion barks to snitch on its hiding spot, and your only job is to corner the rat, catch it — and then **YEET it into the stratosphere** with full ragdoll physics, complete with random Malayalam meme sound effects and fullscreen meme flashes on impact. It's a complete cardio workout disguised as a game.

### The Problem (that doesn't exist)
Humanity has faced no greater crisis than this: a rat is *right there* in your living room (virtually), and you have no physically-accurate, smartphone-based, dog-assisted mechanism to chase it, catch it, and hurl it into the void while being rewarded with Basil Joseph laughing at your throwing technique. Peer-reviewed studies (by us, in our imagination) confirm that 0% of AR apps on the market let you yeet a rat. This is the market failure of our generation.

### The Solution (that nobody asked for)
A full WebXR pipeline that: detects your real-world floor with plane detection, spawns a rat with hiding AI that uses XR hit-testing to bolt behind your actual furniture, a low-poly dog companion camera-anchored to your phone that tracks the rat with look-at rotation and barks (RUFF!) when it's hidden, a raycast tap-to-catch system, and a swipe-to-yeet cannon-es ragdoll launch where the rat screams across your room in a physics-accurate arc — landing with a splat, a ta-da fanfare, a random meme sound, and a fullscreen meme image. The loop then repeats with a fresh rat, because the rat supply, like our genius, is infinite.

## Technical Details
### Technologies/Components Used
For Software:
- Languages: JavaScript (ES Modules), HTML5, CSS3
- Frameworks: Three.js (WebGL/WebXR rendering)
- Libraries: cannon-es (physics/ragdoll), Web Audio API (synthesized SFX), WebXR Device API (hit-test, plane detection, local-floor, dom-overlay)
- Tools: VS Code, Git/GitHub, GitHub Pages, http-server

For Hardware:
- Any WebXR-capable Android phone (ARCore-supported) with a camera
- Specs: Chrome browser, HTTPS connection, gyroscope + accelerometer (standard smartphone sensors)
- No extra tools required — it runs entirely in the mobile browser

### Implementation
For Software:
#### Installation
```bash
git clone https://github.com/jisjohnsajan/pseudocoders.git
cd pseudocoders
```
(No build step — pure static site. If you want a local server:)
```bash
npx http-server -p 8080
```

#### Run
- **Instant play:** open https://jisjohnsajan.github.io/dog-game/ (or serve locally and open `index.html`)
- On an ARCore Android phone with Chrome → tap **ENTER AR** → scan your floor → tap the green ring to spawn the rat
- No WebXR device? Tap **Preview in this browser** — full gameplay loop in a simulated room

### Project Documentation
For Software:
# Screenshots
![Screenshot1](Screenshot%202026-09-12%20145213.png.jpg)
*Start screen + preview mode: the rat scurries on the floor, the dog companion (bottom-right) tracks it, HUD shows the yeet counter — while the user chases the rat around the simulated room in the desktop Preview mode*

# Diagrams
```
[Camera/Phone] → WebXR hit-test + plane detection
       ↓
[Rat AI] ← hiding spots (tables/pillars from real-world scan)
       ↓ (rat hides)
[Pet AI] → look-at controller → barks toward hidden rat
       ↓ (user physically moves + corners rat)
[Tap raycast] → CATCH (boing) → rat attached to camera
       ↓ (swipe up)
[cannon-es ragdoll] → YEET → random meme sound + fullscreen meme flash on impact
       ↓ (rat settles)
[Splat + fanfare + score] → respawn → repeat forever
```
*Game loop: each yeet scores +1 and respawns a fresh rat; meme sounds and images are drawn from shuffle-bags so every throw is a surprise*

### Project Demo
# Video
[https://drive.google.com/file/d/1u08qsbDUyhbZ0bCGgPlLMQ0100EzKM2w/view?usp=drivesdk](https://drive.google.com/file/d/1u08qsbDUyhbZ0bCGgPlLMQ0100EzKM2w/view?usp=drivesdk)
*The video demonstrates the full gameplay loop: spawning the rat in AR, the dog companion tracking and barking, chasing the rat as it hides behind real furniture, tap-to-catch, and the swipe-to-yeet ragdoll launch with meme sound and image reactions*

# Additional Demos
- Live deployment (GitHub Pages, HTTPS for WebXR): https://jisjohnsajan.github.io/dog-game/
- All synthesized sound effects (squeaks, barks, boings, splats, fanfares) are generated at runtime in `sfx.js` — zero audio assets for core SFX

## Team Contributions
- Abhin Joe Saji: Game design & mechanics, rat AI/hiding logic, gameplay testing, presentation & demo video
- Jis John Sajan: WebXR/AR pipeline, Three.js scene & rendering, physics integration, sound engine & meme system, deployment

---
Made with ❤️ at TinkerHub Useless Projects

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)
