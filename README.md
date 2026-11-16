# VistAI

VistAI is an AI commentary and 360° VR experience app built with [A-Frame](https://aframe.io/). Explore immersive video scenes with selectable AI-generated commentary voices.

## Features

- 360° video playback with mouse, touch, and device-orientation camera controls
- Switchable first and second video versions
- Selectable male and female commentary for each video version
- Responsive control panel that can be minimized
- No build step or package installation required

## Run locally

Because browsers restrict media playback and local file access, serve the repository with a small local web server:

```bash
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000) in a browser. Click the page if the browser blocks video autoplay, then use the control panel to select a video and commentary track.

## Project structure

```text
.
├── index.html
├── assets/
│   ├── audio/
│   │   ├── commentary-man-v1.mp3
│   │   ├── commentary-man-v2.mp3
│   │   ├── commentary-woman-v1.mp3
│   │   └── commentary-woman-v2.mp3
│   └── video/
│       ├── video-360-v1.mp4
│       └── video-360-v2.mp4
└── README.md
```

The A-Frame library is loaded from its CDN in `index.html`; all media assets are served locally.

## Browser support

Use a modern browser with WebGL and media playback support. Device orientation controls may require permission on mobile devices and are subject to browser security policies.
