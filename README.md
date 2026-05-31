# Tubular Bowl Centrifuge Simulator

A browser-based simulator for the tubular bowl centrifuge, built as part of the **ChE206 Separation Processes** group project. It lets you study how bowl geometry, operating speed, flow rate, and particle properties affect whether a particle gets captured or escapes with the outflow.

The core idea is simple: if the liquid spends more time inside the bowl than it takes for a particle to migrate from the inner surface to the bowl wall, separation is successful. The simulator visualises this in real time alongside the governing equations, performance charts, and particle trajectory animations.

---

## Files

| File | What it does |
|------|--------------|
| `index.html` | Main simulator — inputs, visualisations, and live calculations |
| `final_centrifuge_simulation.html` | Same as index.html (submission copy) |
| `Sensitivity_Analysis.html` | Separate dashboard for one-at-a-time sensitivity analysis |

---

## How to Run

No installation needed. Everything runs in the browser.

**Option 1 — Just open the file**

Download the files and open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari). For the sensitivity analysis, open `Sensitivity_Analysis.html` the same way.

**Option 2 — Local server (recommended)**

If you run into any issues opening files directly, serve them with Python:

```bash
python -m http.server 8000
```

Then go to `http://localhost:8000` in your browser and click the file you want.

---

## What's Inside

**Main simulator (`index.html`)**
- Adjust bowl geometry, rotational speed, flow rate, and particle/fluid properties using sliders or number inputs
- Three built-in presets: blood plasma separation, whole blood baseline, and water–silica
- Live separation verdict showing whether t_res ≥ t_settle, with Q/Q_max ratio and gauge
- Charts for Q_max vs particle size and cut diameter vs speed
- 2D cross-section animation showing trajectories for three particle sizes (0.5·dp, dp, 2·dp)
- Interactive 3D view — drag to rotate, scroll to zoom

**Sensitivity analysis (`Sensitivity_Analysis.html`)**
- Edit baseline parameters and choose a perturbation level (±5% to ±50%)
- Outputs: Q_max, cut diameter, Sigma Σ, or G-factor
- Tornado chart, parameter sweep plot, ranked sensitivity table, and auto-generated engineering insight cards

---

