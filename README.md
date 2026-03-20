# Robotics Engineering Portfolio Template

A stunning, immersive, and fully responsive single-page portfolio template built purely using HTML, CSS, and Vanilla JavaScript. Specially designed for hardware, mechatronics, and robotics engineers to showcase their complex projects, custom media galleries, and technical proficiencies.

## Features
- **Interactive SVG Robot Hero**: A dynamic, cursor-tracking robot greets visitors in the hero section!
- **Dynamic JavaScript Project Grid**: Projects are natively mapped and generated directly from an easy-to-update `PROJECTS` Javascript object.
- **Skill-Based Interactive Filtering**: Custom stylized category filters (Perception, Controls, Simulation, Hardware, Wearables, Embodied AI) seamlessly filter projects in real-time.
- **Intelligent Media Modal Engine**: Clicking on any project card summons a beautiful detail modal. Any MP4 videos, images, or PDFs you list in your `PROJECTS` data array will automatically be compiled into an integrated smart media display (with video loop auto-playback and native responsive scaling).
- **Dark/Light Mode Syncing**: Engineered with an inverted color-correction CSS pipeline so that native `<img>` and `<video>` tags retain their original hues under multiple screen layouts, without getting washed out!

## Getting Started

### 1. Download & Launch
1. Clone or download this repository.
2. Open a terminal in the root folder and start a fast local server:
    ```bash
    python -m http.server 8000
    ```
3. Open `localhost:8000` in your web browser.

### 2. Customizing Data (`index.html`)
The entire application logic and data source is unified within `index.html`. 

To replace my projects with yours, scroll down to the bottom of the `<script>` tag inside `index.html`. You will find the `<script> ... /* ══ DATA ══ */` section. 
You can populate the following arrays:
*   **`DOMAINS`**: Contains all mapping logic for the filter bar. Define your categories, their background colors, base colors, and CSS cursor icons here.
*   **`PROJECTS`**: Add your work as a Javascript object dictionary!
    ```javascript
    {
      title: 'Your Epic Project Name', 
      year: 'JAN 2026 — PRESENT',
      desc: 'Short subheader explaining the project stack.',
      bullets: 'Bullet point 1|Bullet point 2', // Separate bullets by the "|" character
      tags: 'ROS,Gazebo,MATLAB,Control', 
      domains: ['controls', 'sim'], // Map to domains listed in DOMAINS array
      media: ['asserts/sim_video.mp4', 'asserts/system_architecture.png'] 
    }
    ```

### 3. Adding Your Project Media
1. Drop all your photos (`.png`, `.jpg`) and videos (`.mp4`, `.MOV`, `.gif`) or documents (`.pdf`) into the `asserts`/`assets` directory.
2. In your `PROJECTS` array inside `index.html`, declare the local file path directly in the `media: ['...', '...']` list as shown above. The modal Javascript engine will handle dynamically laying everything out natively when clicked!

## Deployment
Because this site is built 100% locally with vanilla HTML, CSS, and JS (with no node_modules or build dependencies!), you can host it *completely free* in just two clicks via **GitHub Pages**! 
Just push your project structure to a repository titled `username.github.io` and toggle GitHub Pages in your Repository Settings.

---
*Created and refined by Ashwik Manoj Tatineni*