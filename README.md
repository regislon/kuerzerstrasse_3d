# Kürzerstrasse 9 — 3D walk-through

First-person walk-through of the renovation project of Kürzerstrasse 9, 2562 Port (BE),
in the browser (three.js). Open `kuerzerstrasse.html` (or `index.html`) through a web
server — not as a `file://` page:

```bash
python3 -m http.server 8777
# → http://localhost:8777/
```

## Controls

- **Arrow keys** (or W A S D) to move, **mouse** to look around, **Shift** to run,
  **Esc** to release the mouse. **Fly** toggles free flight (E / Space up, Q / C down).
- On phones: joystick bottom-left to move, drag on the right to look.
- **Go to** jumps to a room (eye height 1.70 m).
- The interface follows the browser language — English, Deutsch, Français, Română,
  Русский (English otherwise). Force one with `#de`, `#fr`, `#ro`, `#ru` or `#en` at the
  end of the URL.

## Files

| File | Content |
| --- | --- |
| `kuerzerstrasse.html` | the page (three.js 0.160 + three-mesh-bvh from jsDelivr) |
| `house-model.js` | the model as base64 (`window.HOUSE_GLB_B64`) — same bytes as `house.glb` |
| `house.glb` | the model (glTF binary, Y up, metres) |
| `rooms.json` | teleport points |
| `index.html` | forwards to `kuerzerstrasse.html` |

## Where it comes from

Built in Blender from the floor plans, the Matterport scan and the cadastral survey;
terrain from the survey ground points (elevation DWG); surroundings from swisstopo (
swissBUILDINGS3D 3.0 neighbours, swissTLM3D roads, trees, pools and sports grounds).
Model frame: x = E − 2'585'857, y = N − 1'218'262 (MN95 / LV95), z = 0 at 457.92 m a.s.l.
Generated files — they are re-exported from the Blender pipeline, not edited by hand.
