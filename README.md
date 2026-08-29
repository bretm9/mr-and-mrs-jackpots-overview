# Mr. & Mrs. Jackpots — a vintage-Vegas wedding site with a built-in jukebox

> Our wedding invitation site: a single-page React app with entirely hand-authored animation — neon-flicker headings, scroll-reveal sections, card-suit marquees, a live countdown, scattered polaroids — and a floating music player that embeds our playlist with real now-playing metadata. Zero UI framework.

🔗 **Live site:** https://mr-and-mrs-jackpots.vercel.app

This repo is an overview of a closed-source project. The source is private — I'm happy to walk through it in an interview.

<p align="center">
  <img src="screenshots/hero.jpg" width="900" alt="Hero with countdown and polaroids">
</p>

---

## Overview

We're getting married at a vintage Vegas chapel on Halloween 2026, and the invitation needed to feel like the venue: neon, retro type, a little bit of showmanship. The site is one React page with no component library and no animation library — every effect is CSS keyframes and small hooks — so the design could be exactly what we wanted rather than what a framework offered.

## Screenshots

| The venue | The details |
|---|---|
| ![Venue](screenshots/venue.jpg) | ![Details](screenshots/details.jpg) |

| Hotel suggestions | When & where (itinerary) |
|---|---|
| ![Hotels](screenshots/hotels.jpg) | ![Itinerary](screenshots/itinerary.jpg) |

<p>
  <img src="screenshots/mobile-hero.jpg" width="220" alt="Mobile hero">
</p>

## Features

- **Hero** with neon-flicker script headings, a live countdown to the ceremony, and scattered polaroids with hand-written captions.
- **Scroll-reveal sections** (IntersectionObserver): the venue, ceremony/reception/dress-code details, hotel suggestions, and a two-day itinerary.
- **Card-suit marquees** that ribbon between sections.
- **Jukebox** — a floating music player that embeds our wedding playlist via the **YouTube IFrame API**, with true now-playing title/artist metadata, play/pause/skip, and a slide-in panel.
- **Admin mode** — a password-gated editor with **drag-and-drop itinerary editing**, so the schedule can be adjusted without a deploy.
- Fully responsive down to phone widths.

## Technologies

React 19 · Vite · CSS-in-JS + keyframe animations · IntersectionObserver · YouTube IFrame Player API · Vercel

## Engineering notes

- **No framework, on purpose.** The whole visual language — flicker timing, marquee speed, polaroid scatter, countdown typography — is bespoke CSS and state; it's a good example of what I can do with the platform alone.
- **The YouTube IFrame API is fiddly** about load order, autoplay policy, and metadata; the player wraps it in a small state machine so the UI always reflects the real playback state.
- Photos are pre-sized and lazy-loaded so the hero stays fast on mobile.

## Status

Built March–April 2026 (40 commits). Live and in use by our guests.

## Process

Built solo with Claude Code as a pair-programmer; design direction by the two of us.

---

*Bret Merritt · [GitHub](https://github.com/bretm9) · [LinkedIn](https://www.linkedin.com/in/bret-merritt) · merrittbret9@gmail.com*
