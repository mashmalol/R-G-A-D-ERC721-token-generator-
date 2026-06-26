🎨 MAKE & OWN A TOKEN ; Real‑time Glitch Art & Datamosh
A WebGL‑powered interactive video glitch art studio that runs entirely in your browser.


✨ Features
Real‑time WebGL effects – Datamosh, Pixel Sort, Feedback Loop, Color Shift, ASCII Art, ASCII Numbers, and more.

Full control panel – fine‑tune every parameter with sliders & number inputs.

Presets – instantly switch between Psychedelic, Ghostly, Neon, Glitchy VHS, Dreamy, and Default.

Post‑processing effects – apply ASCII, dither, RGB split, invert, halftone, solarize, etc. on top of the main effect.

Freeze Frame – capture a frame and keep it as a frozen overlay.

Record video – export your session as MP4 or WebM (via MediaRecorder API).

Export animated GIF – capture a looped sequence and save as a GIF (using gif.js).

Snapshot – save a still PNG image.

Upload your own media – use an image or video file as the source (instead of the webcam).

Camera switching – toggle between front and rear cameras on mobile devices.

ERC‑721 Token Metadata Generator – create NFT‑ready JSON metadata with traits and attributes directly in the app.

Donation modal – shows crypto addresses (BTC, ETH, SOL, LTC, DOGE, etc.) with QR codes and copy‑to‑clipboard.

Minimizable / resizable control panel – keeps the UI clean on any screen.

Mobile‑friendly – responsive interface with touch support.

🚀 How to Run
Clone the repository (or download the single index.html file).

Open index.html in any modern browser (Chrome, Firefox, Edge, Safari).

Allow camera access when prompted – the app starts with your webcam.

Start playing with the sliders and presets!

No build step, no dependencies to install – everything is loaded from CDNs.

🕹️ Controls Overview
Tabs
Main Controls – Presets, post‑effects, trailing, motion, hue, freeze, upload.

Extra Controls – ASCII style, width, contrast, particle count, glitch seed, per‑channel chroma, grain, scanlines, glitch amount, seed, motion blur, etc.

Effects – Main effect selector (Datamosh, Pixel Sort, etc.) with intensity, displacement, feedback, threshold, and ASCII Numbers settings.

Advanced – Buffer size, extrapolation, GIF duration/FPS/quality, brightness, contrast, saturation.

Token Generator – Fill in name, description, image URL, attributes JSON, and generate/download ERC‑721 metadata.

Buttons
Randomize Effects (top‑right floating button) – randomises all sliders and optionally selects a random post‑effect.

Freeze Frame – captures the current frame and adds it to the frozen stack.

Clear Frozen – removes all frozen frames.

Record – starts/stops video recording.

Save GIF – opens a capture dialog and generates an animated GIF with the current settings.

Snapshot – downloads a PNG of the current canvas.

Refresh Stream – restarts the webcam or resets the uploaded media.

Switch Camera – toggles between front/back cameras.

Upload – choose an image or video file to use as the source.

🧠 How It Works
The app uses WebGL to run fragment shaders on a video input (webcam, uploaded file, or frozen frame). The core loop:

Capture a video frame into a texture.

Apply the main effect shader (Datamosh, Pixel Sort, etc.) that mixes the current frame with a history buffer to create temporal effects (trails, motion‑based glitches, feedback).

Optionally apply a post‑processing shader (ASCII, dither, RGB split, etc.) for additional stylisation.

Display the result on the canvas.

Maintain a history of frames for trail and feedback effects.

Allow freezing, recording, and GIF export.

The shader code is embedded in JavaScript and compiled at runtime. All parameters (sliders) are passed as uniforms to the shaders, giving real‑time visual feedback.

🛠️ Dependencies
All external libraries are loaded from CDN:

QRCode.js – for generating QR codes in the donation modal.

gif.js – for encoding animated GIFs. The worker script is fetched and served via a Blob URL to avoid CORS issues.

No other dependencies – the entire app is vanilla JavaScript + WebGL.

🎨 Customising Effects
Adding a New Shader
Define your fragment shader as a JavaScript string (using precision highp float; etc.).

Add it to the shaderSources object with a unique key.

Add an option to the effectSelector dropdown in the HTML.

The changeEffect() function will compile and switch to your shader.

Adding a New Control
Add a <div class="control-group"> with a range slider and number input, using IDs like myControlRange and myControlNumber.

Add a default value in controlValues.

Add a configuration entry in controlConfig (specifying precision, min/max, etc.).

The setupControl() function will automatically wire it up.

📜 License
This project is open‑source and available under the MIT License. Feel free to use, modify, and distribute it. If you make something cool, we’d love to see it!

🙏 Acknowledgments
Inspired by the glitch art community and the creative possibilities of real‑time video manipulation.

Thanks to the authors of gif.js and QRCode.js for their excellent libraries.

Donations are always appreciated to support further development! ❤️

📸 Screenshots
Add your own screenshots here to showcase the effects.

🐛 Issues & Contributions
If you encounter any bugs, or have suggestions for improvements, please open an issue or submit a pull request. Contributions are welcome!

📬 Contact
For questions or feedback, you can reach out via the GitHub Issues page.

Enjoy creating glitch art! 🌀