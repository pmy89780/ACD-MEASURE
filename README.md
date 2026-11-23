# ACD Measure

Browser-based research tool that measures the horizontal distance between the **pupil centre** and the **centre of corneal curvature** from temporal side-view eye images (smartphone-based anterior chamber depth research).

**Live site:** `https://YOUR-USERNAME.github.io/acd-measure/`

## Features
- Capture a photo with the phone camera or upload an unmarked image
- Automatic detection of the pupil centre and the corneal curvature centre
- Horizontal distance shown in millimetres, drawn on the image
- Draggable markers to fine-tune the detected points
- Scale calibration (click both ends of a known length, e.g. 11.7 mm corneal diameter or a ruler)
- Save original image, processed image and measurement value (stored in the browser)
- Download images and export all measurements as CSV

## How to use
1. Open the site and tap **Capture** or **Upload**.
2. Choose whether the cornea projects to the left or right.
3. Tap **Calibrate scale** and click both ends of a known length. Without this, the result is marked "uncal."
4. Adjust the green (pupil) or red (corneal curvature) marker if needed.
5. Enter an image label / patient ID and tap **Save to records**.
6. Use **Export CSV** regularly to back up your data.

## How it works
- **Pupil centre:** the darkest rounded region near the image centre.
- **Corneal curvature centre:** estimated from the outer corneal edge along the pupil row, assuming a 7.8 mm corneal radius.
- **Distance:** |x(pupil) − x(curvature centre)| ÷ pixels-per-mm.

## Limitations
This is a research prototype using simple image analysis, not a trained model or a medical device. Do not use it for clinical decisions. Always validate against a reference method. Glare, eyelashes and shadows may affect detection.

## Privacy
All processing runs locally in your browser. Images are never uploaded to any server. Saved records live in the browser's IndexedDB on that device only.

## Deploy on GitHub Pages
1. Upload all files in this folder to a public repository.
2. Go to **Settings → Pages**, set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Open the link shown after a minute or two.

## License
MIT – see `LICENSE`.
