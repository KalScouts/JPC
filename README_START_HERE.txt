STEP-POWER GENERATOR — TOOTH-COUNT EXPERIMENT PACKAGE

FILES
Upload all contents of this folder directly to the GitHub Pages publishing root. Keep the four `.glb` files beside their matching HTML pages.

- index.html: 20-tooth reference experiment
- 10.html, 20.html, 30.html, 40.html: individual pinion trials
- 404.html: clean route handler for /10/, /20/, /30/, /40/
- step-power-generator-ar-10.glb
- step-power-generator-ar-20.glb
- step-power-generator-ar-30.glb
- step-power-generator-ar-40.glb: matching AR models

WHAT IS CHANGED
Each page uses the matching tooth count for the visible rack-drive pinion and its AR fallback. The experiment selector lets users change trial and see nominal pitch diameter plus an ideal motor-turn estimate for a 20 mm rack stroke. Other gearbox gears remain fixed.

THEORETICAL COMPARISON
10 teeth: 10 mm pitch diameter; 15.92 ideal motor turns per 20 mm stroke
20 teeth: 20 mm pitch diameter; 7.96 ideal motor turns per 20 mm stroke
30 teeth: 30 mm pitch diameter; 5.31 ideal motor turns per 20 mm stroke
40 teeth: 40 mm pitch diameter; 3.98 ideal motor turns per 20 mm stroke
Formula: 20 / (pi * pinion pitch diameter) * 25. The 25:1 secondary ratio is ideal. This is not a prediction of electrical power.

SUGGESTED FAIR EXPERIMENT
Use the same 20 mm rack stroke for each pinion. Keep the motor, electrical load, stroke speed and rest time the same. Repeat five times per setup and record turns plus measured voltage/current. Compare averages; turns alone do not measure electrical power.

IMPORTANT SAFETY / MECHANICAL LIMITATION
The supplied physical print setup uses an 18-tooth rack pinion. The other profiles are conceptual visual/ratio trials only; they are not validated involute gears or ready-to-print replacement parts. Validate tooth mesh, centre distance, shaft bore, alignment, clearance, strength, clutch and motor load before changing the real build. Do not load the pedal with a person or run printed components until the whole mechanism is properly checked.

DEPLOY AND TEST
1. Upload all files directly to the repository publishing root.
2. Enable GitHub Pages.
3. Confirm the main page and /10/, /20/, /30/, /40/ routes over HTTPS.
4. Test AR on the target mobile device. A static source check cannot replace live WebXR/Quick Look verification.
