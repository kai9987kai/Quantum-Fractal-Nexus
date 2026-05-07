# Quantum-Fractal Nexus Ultra

Quantum-Fractal Nexus Ultra is a single-file browser simulation lab in `index.html`. It combines fractal rendering, particle systems, active matter, morphogen fields, novelty search, quality-diversity archives, and probe-agent behavior in one interactive canvas app.

## Run

Open `index.html` directly in a browser, or serve the folder locally:

```powershell
python -m http.server 8765 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:8765/index.html
```

No build step or package install is required.

## Main Controls

- Drag: rotate the field
- Mouse wheel: zoom
- `W` / `S`: camera zoom drift
- `A` / `D`: camera rotation drift
- `Space`: pause/resume
- `B`: toggle bloom
- `/`: open command palette
- `Ctrl+S`: export state
- Shift-click: place a field
- Alt+Shift-click: place a repulsor field

## Labs

### Research Lab

Adds active-matter and swarmalator-inspired behavior:

- Collective coupling
- Disorder/noise
- Phase synchronization
- Live order, cluster, and novelty metrics

### Experimental Substrates

Adds research-inspired simulation substrates:

- Morphogen Memory: particles deposit and follow a diffusing field
- Chiral Species: asymmetric species torque and nonreciprocal sorting
- Quorum Edge: dense morphogen regions create circulating edge currents
- Protocols: Chemokinetic Trails, Nonreciprocal Sorting, Quorum Vortex, Protocell Pulse, and Damage & Regrow

### Evolution Lab

Runs local genome mutation and champion selection:

- Captures the simulation parameters as a genome
- Mutates global settings and substrate modes
- Scores behavior from novelty, clustering, morphogen activity, agency, defects, and FPS
- Saves a champion genome
- Exports telemetry as CSV

### QD Archive

Implements a MAP-Elites-style quality-diversity archive:

- Stores high-scoring elites by behavior bins
- Uses order and cluster metrics as archive descriptors
- Samples archived elites back into evolution
- Exports the archive as CSV

### Agency Lab

Adds embodied probe agents:

- Probes sense the morphogen field
- They choose goals, move, deposit signals, and nudge nearby particles
- Agency score feeds back into genome scoring
- Homeostat mode tries to keep probes near a target field concentration

## Exports

The app can export:

- `nexus-state.json`: complete app state
- `nexus-snapshot-*.png`: canvas snapshot
- `nexus-telemetry.csv`: evolution telemetry
- `nexus-qd-archive.csv`: quality-diversity archive contents

## Notes

State is saved in browser `localStorage`. If the app reloads with an old experimental state, use **Reset** or clear site data in the browser.

Microphone input is optional and only starts after pressing **Enable Mic**. If access is denied, the simulation uses a synthetic audio level instead.

WebXR support depends on the browser and device.
