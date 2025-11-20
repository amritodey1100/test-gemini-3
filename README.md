Amrito Dey — Kinetic Profile (v3)An immersive, cinematic web portfolio featuring a reactive 3D neural globe, glitch aesthetics, and a synchronized audio engine.This project is a single-file web experience designed to showcase a personal brand with high-end visual effects, requiring zero build tools or complex installation.⚡ Key Features3D Visual Core: A rotating "Neural Globe" built with Three.js that reacts to mouse movement (parallax effect).Cinematic Audio Engine:Supports custom background music (MP3).Generates real-time sound effects (glitches, impacts, typing sounds) using the Web Audio API.Retro-Futurism: CRT scanline overlays, chromatic aberration (RGB split), and neon glow effects.Automated Timeline: A sequenced storytelling engine that transitions through different "Scenes" (Intro, Skills, Ventures, Vision).Responsive: Fully fluid design that works on desktops and mobile devices.🚀 Quick StartPrerequisitesA modern web browser (Chrome, Edge, Firefox, Safari).A code editor (VS Code, Notepad++, etc.) if you want to customize it.InstallationDownload the file: Save the provided index.html to a folder on your computer.Add Music:Download your desired background music (e.g., soundtrack.mp3).Place the .mp3 file in the exact same folder as index.html.Link the Music:Open index.html in your text editor.Search for the audioCore object (around line ~450).Update the filename:// Change 'your-music-file.mp3' to your actual file name

this.bgMusic = new Audio('soundtrack.mp3'); 

Run: Double-click index.html to open it in your browser. Click "INITIALIZE" to start the experience.🛠️ Customization Guide1. Changing the Text/StoryThe content is managed by the Scene Manager at the bottom of the script. Look for the const scenes = \[...] array.Each scene has a render function where you can edit the HTML:{

&nbsp; // Scene 0: INTRO

&nbsp; at: 0, // Time in milliseconds when this scene starts

&nbsp; render: (el) => {

&nbsp;   el.innerHTML = `

&nbsp;     <!-- Edit your HTML content here -->

&nbsp;     <h1 class="font-tech ...">YOUR NAME HERE</h1>

&nbsp;   `;

&nbsp;   audioCore.playSfx('boom'); // Optional: Play a sound effect

&nbsp; }

}

2\. Adjusting TimingTo make a scene stay longer or shorter, adjust the at: property of the next scene.Example: If Scene 1 starts at 3500 (3.5s) and Scene 2 starts at 8500 (8.5s), Scene 1 will be visible for 5 seconds.3. Changing ColorsThe project uses CSS Variables and Tailwind classes.Global Colors: Edit the :root variables in the <style> tag::root {

&nbsp; --cyan: #00f3ff;  /\* Primary Accent \*/

&nbsp; --purple: #bc13fe; /\* Secondary Accent \*/

&nbsp; --bg: #030304;     /\* Background \*/

}

4\. Audio SettingsYou can tweak the volume in the audioCore.init function:this.bgMusic.volume = 0.4; // 0.0 (Silent) to 1.0 (Max)

📦 Tech StackHTML5 \& CSS3: Core structure and styling.Tailwind CSS (CDN): Utility classes for layout and typography.Three.js (CDN): 3D rendering for the background globe and particles.Web Audio API: For generating real-time SFX and audio processing.Google Fonts: Inter, JetBrains Mono, and Orbitron.⚠️ Troubleshooting"The music isn't playing!"Ensure the .mp3 file is in the same folder.Ensure the filename in the code matches the file exactly (case-sensitive).Did you click "INITIALIZE"? Browsers block audio from playing automatically; user interaction is required."The 3D globe isn't showing."Check your internet connection. The script loads Three.js from a CDN (cdnjs.cloudflare.com).📄 LicenseThis project is free to use and modify for your personal portfolio.Created by Amrito Dey's AI Assistant

