# JS Lightbox, Video & Form Demos

A small collection of vanilla JavaScript demos covering image galleries, video playback state, and form persistence.

## Features

- **Image gallery** — renders a grid of images and opens them in a lightbox (`simplelightbox`) on click
- **Video player** — embeds a Vimeo player, throttled-saves the current playback position to `localStorage`, and resumes from it on reload
- **Feedback form** — persists email/message input to `localStorage` on every change (throttled), restores it on reload, and clears it on submit

## Technology

- Vanilla JavaScript (ES modules)
- Vite build tooling
- simplelightbox for the image lightbox
- @vimeo/player for video embedding and playback events
- lodash.throttle for rate-limiting storage writes
- GitHub Actions workflow deploying the production build to GitHub Pages

## Project structure

```
src/
  01-gallery.html / 01-gallery.js   Image gallery with lightbox
  02-video.html   / 02-video.js     Vimeo player with resume-on-reload
  03-feedback.html/ 03-feedback.js  Form with localStorage persistence
  css/
  partials/header.html
  index.html                        Links to all three demos
```

## Commands

```
npm install     # install dependencies
npm run dev     # start the Vite dev server
npm run build   # build for production (GitHub Pages base path)
npm run preview # preview the production build
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds the project and deploys the `dist` output to the `gh-pages` branch for GitHub Pages.
