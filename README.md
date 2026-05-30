You are a senior full-stack software engineer and UI/UX designer. Build a production-ready web application called:
“SpeedPaint Studio”
The app allows users to upload images and automatically generate a speed painting video of the image being drawn step-by-step, simulating real-time drawing strokes.
The system must be:

* Fully functional
* Error-free
* Simple UI
* High-performance
* Export-ready for YouTube content creators
🎯 CORE GOAL
Create a web app that:

1. Lets users upload an image (JPG, PNG, WEBP)
2. Converts the image into a stroke-based drawing animation
3. Plays it back as a speed painting video
4. Allows users to adjust speed/duration
5. Exports high-quality video (MP4/WebM)
🧩 FEATURES
1. IMAGE UPLOAD SYSTEM

* Drag & drop upload area
* Button: “Upload Image”
* Accept formats:
   * JPG
   * PNG
   * WEBP
* Auto preview uploaded image
* Auto-resize image to canvas while maintaining aspect ratio
2. SPEED PAINT ENGINE (CORE FEATURE)
Simulate drawing of the uploaded image using:
Method:

* Convert image into:
   * Edge detection (Canny or similar algorithm)
   * Vector path approximation OR pixel-to-stroke mapping
* Generate progressive drawing sequence
* Simulate brush strokes gradually revealing the image
Requirements:

* Smooth stroke animation
* Adjustable brush size (small, medium, large)
* Adjustable stroke density (low / medium / high detail)
* Optional “artistic mode” (simplified strokes)
3. TIMELINE CONTROLS
User must be able to control:

* 🎚 Speed slider (0.5x – 10x)
* ⏱ Total duration selector (10 sec – 10 min)
* ▶ Play / Pause button
* 🔁 Restart button
* ⏭ Preview scrubber (timeline bar)
4. CANVAS PLAYER

* Real-time drawing canvas
* Shows animation stroke-by-stroke
* Smooth 60 FPS rendering
* Background options:
   * White
   * Transparent
   * Dark mode canvas
5. EXPORT SYSTEM (VERY IMPORTANT)
Export formats:

* MP4 (H.264)
* WebM (fallback)
Export settings:

* Resolution options:
   * 720p
   * 1080p (default)
   * 4K (premium mode structure, but implement placeholder logic)
* Frame rate:
   * 30 FPS default
   * 60 FPS optional
Export method:

* Use browser-based rendering OR FFmpeg WASM
* Ensure no frame drops
* Render timeline frame-by-frame into video buffer
6. UI/UX DESIGN
Style:

* Clean modern creator tool
* Minimal interface like Canva / CapCut
* Dark + light mode toggle
Layout:
Left panel:

* Upload image
* Controls (speed, duration, brush)
Center:

* Canvas preview player
Right panel:

* Export settings
* Download button
7. PERFORMANCE REQUIREMENTS

* Must handle large images (up to 4K input)
* Must not freeze UI during rendering
* Use Web Workers for heavy processing
* Optimize rendering pipeline
8. BONUS FEATURES (IMPORTANT FOR VIRAL TOOL)
Optional but highly recommended:

* Background music upload
* Auto-sync drawing speed to music beats
* AI “smooth stroke enhancement”
* Time-lapse presets:
   * 15 sec TikTok
   * 30 sec Shorts
   * 60 sec YouTube Shorts
* Auto aspect ratio:
   * 9:16 (Shorts)
   * 16:9 (YouTube)
   * 1:1 (Instagram)
9. FILE STRUCTURE (REQUIRED OUTPUT)
Generate clean modular code:

* /frontend
   * CanvasPlayer.jsx
   * UploadPanel.jsx
   * Controls.jsx
   * ExportPanel.jsx
* /engine
   * imageToStrokes.js
   * renderer.js
   * exportVideo.js
* /utils
   * helpers.js
* /workers
   * processingWorker.js
10. CORE LOGIC FLOW

1. User uploads image
2. System analyzes image → generates stroke paths
3. Stroke data stored as animation timeline
4. Canvas renders strokes over time
5. User adjusts speed/duration
6. User exports final video
11. ERROR HANDLING

* Invalid file type → show friendly error
* Large file → compress automatically
* Export failure → retry system
* Prevent memory leaks in canvas rendering
12. FINAL OUTPUT REQUIREMENT
The final app must:

* Work without backend dependency (frontend-first)
* Run in browser
* Be production-ready
* Be usable immediately after deploy
* Be optimized for creators making YouTube content
🧨 END GOAL
A creator should be able to:
Upload image → click play → get speed painting video → export → upload to YouTube Shorts
