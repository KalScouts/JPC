# Step-Power Generator — Pinion Tooth-Count Experiments

This is a static GitHub Pages project. Upload the contents of this folder to the repository publishing root. Keep the four `.glb` files beside the HTML files.

## Experiments

- `10.html` / `/10/`: 10 teeth, 10 mm nominal pitch diameter, about 15.92 ideal motor turns per 20 mm rack stroke.
- `20.html` / `/20/`: 20 teeth, 20 mm nominal pitch diameter, about 7.96 ideal motor turns per 20 mm rack stroke.
- `30.html` / `/30/`: 30 teeth, 30 mm nominal pitch diameter, about 5.31 ideal motor turns per 20 mm rack stroke.
- `40.html` / `/40/`: 40 teeth, 40 mm nominal pitch diameter, about 3.98 ideal motor turns per 20 mm rack stroke.
- `index.html`: opens the 20-tooth reference trial.

Each page now generates the matching visible pinion geometry, loads the matching AR model and includes a tooth-count selector with the theoretical comparison values. The two fixed 90T/18T gearbox stages are still shown as a 25:1 ideal secondary ratio. The estimate is `20 mm ÷ (π × pinion pitch diameter) × 25`; it predicts ideal motor turns, not real electrical power.

## Suggested fair test

Use the same 20 mm rack stroke for each pinion. Keep the motor, electrical load, stroke speed and rest time as consistent as possible. Repeat each configuration five times and record motor turns plus measured voltage/current. Compare averages and note any friction, slipping or missed tooth engagement. Turns alone do not measure electrical power.

## Important engineering limitation

The supplied physical print setup uses an 18-tooth rack pinion. The 10T, 20T, 30T and 40T replacements shown here are conceptual visual/ratio trials, not validated involute gears or ready-to-print replacement parts. The simple generated profiles are not proof of proper rack mesh. Confirm tooth pitch, centre distance, bore, shaft alignment, clearance, strength and motor/clutch behaviour before printing or operating an alternative. Do not load the pedal with a person or motor-spin printed parts until the structure and mechanism have been properly checked.

## GitHub Pages setup

1. Extract the ZIP.
2. Upload every file in this folder directly to the publishing root (not inside a nested folder).
3. Enable GitHub Pages for the intended branch/folder.
4. Test `/`, `/10/`, `/20/`, `/30/` and `/40/` over HTTPS. The 404 handler supports the clean trial routes.

The AR button needs a compatible device/browser and HTTPS. Test the published page on the actual phone/tablet; this package can be statically checked here but does not replace a live WebGL/WebXR device test.
