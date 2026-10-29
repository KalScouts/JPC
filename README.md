# Step-Power Generator — interactive tooth-count trials

## What is included
- `index.html`: 20-tooth reference model
- `10.html`, `20.html`, `30.html`, `40.html`: 10T, 20T, 30T and 40T trials
- matching `step-power-generator-ar-*.glb` models for phone AR
- `404.html`: GitHub Pages route handling for `/10/`, `/20/`, `/30/`, `/40/`

## Changes in this revision
- Removed the large left-side experiment panel so the full mechanism stays visible.
- Added compact tooth-count selectors, Run/Pause, Single cycle and cycle-speed controls.
- Added a live corner generator screen showing estimated open-circuit voltage, shaft RPM and drive state.
- The rack moves through a 20 mm stroke and rotates its trial pinion. The two 90T/18T gear stages rotate in their 5:1 ratios. The shaft meshes and visible motor rotor/coupling key now rotate in step with the gear train; the one-way clutch coasts on the spring-return stroke rather than reversing the motor.
- Made a visual ground plane and subtle grid visible directly beneath the fixed base board. The base underside is at y=0 in the model coordinates; the floor is at y=-0.25 mm. The floor is hidden during AR placement.

## Voltage readout: important limitation
The voltage display is a calculation, not a sensor. It assumes a linear open-circuit relationship of **6 V at 6,000 rpm** by default. The reference voltage is editable in the screen for a different motor. Replace this assumption with the fitted motor's measured back-EMF constant or its own no-load test data. Real loaded voltage will be lower and depends on motor winding, rectification, load, speed, friction and electrical losses. The displayed volts are not an electrical-power result.

## Tooth-count math
With module 1 and nominal pitch diameter equal to tooth count in millimetres, rack travel of 20 mm and ideal secondary ratio 25:1:
- 10T: 10 mm pitch diameter; about 15.92 ideal motor revolutions per 20 mm downstroke
- 20T: 20 mm pitch diameter; about 7.96 revolutions
- 30T: 30 mm pitch diameter; about 5.31 revolutions
- 40T: 40 mm pitch diameter; about 3.98 revolutions

## Publish
Upload all files directly to the GitHub Pages root, preserving the HTML and GLB files together. Open the index page over HTTPS. Trial buttons use the 404 route handler for `/10/`, `/20/`, `/30/` and `/40/`.

## Mechanical limits
The current physical pack uses an 18T pinion. 10T/20T/30T/40T trial profiles are visual and ratio concepts, not validated involute or print-ready gears. Verify the rack/tooth profile, centre distance, shaft bore, alignment, clearance, strength, return spring, one-way clutch and motor load before changing the real mechanism. Do not stand on or load the pedal while testing an unverified mechanism.
