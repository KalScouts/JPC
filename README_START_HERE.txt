STEP-POWER GENERATOR — FLAT GITHUB PAGES DEPLOYMENT

FILES ARE ALL IN ONE FOLDER
There are no subfolders in this package. Extract this ZIP, then upload the CONTENTS directly into the publishing root of your GitHub repository. Do not upload the ZIP itself, and do not upload the outer extracted folder as one nested folder.

FILES
- index.html: root preview, opens the 20T trial
- 404.html: clean-route handler for GitHub Pages
- 10.html, 20.html, 30.html, 40.html: individual trial pages
- step-power-generator-ar-10.glb, step-power-generator-ar-20.glb, step-power-generator-ar-30.glb, step-power-generator-ar-40.glb: the matching AR models
- .nojekyll: keeps the static bundle unmodified by Jekyll

CLEAN QR ROUTES
After the contents are published, these clean URLs are handled without route folders:
  https://YOUR-SITE/10/
  https://YOUR-SITE/20/
  https://YOUR-SITE/30/
  https://YOUR-SITE/40/

For a project Pages site with a repository base, for example https://USERNAME.github.io/REPOSITORY/, the routes are:
  https://USERNAME.github.io/REPOSITORY/10/
  https://USERNAME.github.io/REPOSITORY/20/
  https://USERNAME.github.io/REPOSITORY/30/
  https://USERNAME.github.io/REPOSITORY/40/
The route handler detects the repository base, redirects internally to the matching flat HTML file, and restores the clean route in the address bar. Refreshing a route is handled by 404.html again. The main / page opens 20T.

GITHUB PAGES SETUP
1. Extract the ZIP on your computer.
2. Open the extracted folder and select every file, including the four GLBs and .nojekyll.
3. Upload those selected files directly to the publishing root of the repository. The repository root should show index.html and 404.html alongside 10.html/20.html/30.html/40.html and the four .glb files. No folder should contain these files.
4. In GitHub, make sure Pages is enabled for the intended branch/folder and wait for the commit deployment to finish.
5. Test /, /10/, /20/, /30/, and /40/ over HTTPS before generating QR codes.

GEAR COMPARISONS
- /10/: 10 teeth, 10 mm pitch diameter, 15.92 ideal motor turns per 20 mm stroke
- /20/: 20 teeth, 20 mm pitch diameter, 7.96 ideal motor turns per 20 mm stroke
- /30/: 30 teeth, 30 mm pitch diameter, 5.31 ideal motor turns per 20 mm stroke
- /40/: 40 teeth, 40 mm pitch diameter, 3.98 ideal motor turns per 20 mm stroke
The estimates use 20 / (pi * pinion pitch diameter) rack turns, multiplied by the two 5:1 ideal secondary stages (25:1 total ideal speed ratio). They do not predict real electrical power.

IMPORTANT MECHANICAL LIMITATION
The supplied Rev J print pack includes an 18T rack pinion, not validated 10T/20T/30T/40T replacement parts. The alternative profiles are conceptual visual/ratio trials, not validated involute gears or ready-to-print STLs. Tooth mesh, pinion/rack centre distance, shaft bore, bridge location, clearance and strength must be designed and hand-tested before changing the physical build. The original supplied 18T setup remains the baseline. Do not load the pedal with a person or motor-spin the printed clutch/shafts before the structure and mechanism have been properly checked.

AR
The AR button uses the relevant GLB stored at the same flat root. AR needs HTTPS and a compatible device/browser. Android live WebXR hit testing and iOS native Quick Look have different behaviour; native AR can show a static model rather than keep the browser animation running. Test each platform after deployment.

TEST REVIEW
Automated checks for this pack verify that all required files are in the root, all HTML asset references point to matching root GLBs, and clean paths route to the correct gear page. A live 3D/AR browser test still needs to be done on the published HTTPS site and target phone because this build environment cannot provide a reliable live WebGL device render.
