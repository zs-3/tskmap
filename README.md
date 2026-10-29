# Kart Map Workshop

A mobile/tablet-friendly, browser-based low-poly arena editor inspired by colourful kart-battle maps. It is a standalone static site; no build step or server-side code is required.

## Run it

1. Extract the ZIP.
2. Open `index.html` in a modern browser with internet access (Three.js and Google Fonts load from CDNs).
3. For best results, host the folder on any static host or use a local web server. Some browsers restrict local-file storage/import features when opening files directly.

## Features

- Responsive layout: large viewport plus tool dock on desktop; arena above the tools on phones/tablets.
- Three.js renderer sized from the viewport with `ResizeObserver`, CSS canvas filling its container, pixel ratio capped at 2, and projection updates on resize/orientation changes.
- Orbit, pan, pinch zoom, wheel zoom, on-screen zoom buttons and a directional camera pad suitable for touchscreens.
- Procedural low-poly assets with a large searchable library and many palette variants; no copyrighted game models or textures are bundled.
- Templates: Candy Coast, Smash Fort, Lava Pit, Moonlit Graveyard, Castle Nightfall, Frostbite Speedway, Dusty Dunes, Neon Turbo and Blank Grass.
- Object placement, selection, drag movement, rotation, scale, lift, tint, duplicate, delete, nudge, undo/redo, and autosave in local browser storage.
- World size, ground, checker pattern, edge walls, fog, sky, below-map ocean/lava and grid snap controls.
- Editable map JSON and game-data JSON exports/imports.
- Experimental GLB/GLTF/OBJ source import. GLB is the most portable choice. Custom model placement is not yet integrated as seamlessly as built-in assets.

## Notes / limitations

- This is an original procedural editor using a similar bright, chunky, low-poly visual language—not a copy of Smash Karts' proprietary assets.
- The game-data export is a neutral JSON schema. You will still need to map object roles and coordinates into the code/engine of your own game.
- Imported model files are stored in project JSON, but restoring/rendering custom imports after a reload is currently experimental.
- For large scenes, keep object count moderate on older tablets. Reduce browser zoom or close other tabs if WebGL memory is tight.
