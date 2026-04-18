# Velvet Pour Landing Page

A polished React landing page showcasing animated cocktail bar content. This project uses Vite for fast bundling, Tailwind CSS for styling, and GSAP for advanced scroll and text animations.

## Table of Contents

- [Summary](#summary)
- [Tech Stack](#tech-stack)
- [Structure](#structure)
- [Component Details](#component-details)
- [Data and Content](#data-and-content)
- [Styling and Assets](#styling-and-assets)
- [Getting Started](#getting-started)
- [Available Scripts](#available-scripts)
- [How to Customize](#how-to-customize)
- [Notes](#notes)

## Summary

The app renders a multi-section landing page for a cocktail concept called **Velvet Pour**. It combines:

- animated hero typography and video playback
- scroll-triggered section transitions
- an interactive cocktail menu with slide controls
- responsive layout for desktop and mobile

The page focuses on immersive visuals and motion rather than backend data.

## Tech Stack

- React 19
- Vite
- Tailwind CSS 4
- GSAP with `@gsap/react`
- `react-responsive`

## Structure

### Root Files

- `src/main.jsx`
  - mounts the React app using `createRoot`
  - imports global styles from `src/index.css`
- `src/App.jsx`
  - registers GSAP plugins (`ScrollTrigger`, `SplitText`)
  - renders the main application sections

### Components

- `src/components/Navbar.jsx`
- `src/components/Hero.jsx`
- `src/components/Cocktails.jsx`
- `src/components/About.jsx`
- `src/components/Art.jsx`
- `src/components/Menu.jsx`
- `src/components/Contact.jsx`

### Shared Content

- `constants/index.js`
  - stores navigation links, cocktail data, feature lists, opening hours, and social links

### Assets

- `public/fonts/` — custom font files
- `public/images/` — icons, backgrounds, textures, and UI images
- `public/videos/` — hero background video

## Component Details

### `Navbar.jsx`

- Uses `useGSAP` to animate the navigation bar background when scrolling.
- Contains logo and section navigation links.
- Navigation targets internal page IDs like `#cocktails`, `#about`, and `#contact`.

### `Hero.jsx`

- Displays the main headline: `MOJITO`.
- Uses `SplitText` to animate text characters and lines.
- Includes a muted video background that progresses based on scroll.
- Animates decorative leaf images using GSAP scroll triggers.

### `Cocktails.jsx`

- Shows two lists: popular cocktails and mocktails.
- Maps data from `constants/cocktailLists` and `constants/mockTailLists`.
- Adds parallax motion to leaf accents while scrolling.

### `About.jsx`

- Introduces the brand story and values.
- Animates heading and image grid elements into view.
- Displays customer rating and review summary.

### `Art.jsx`

- Highlights the creative bar experience.
- Renders two lists of qualities from shared constant arrays.
- Uses scroll-triggered masking and fade animations.
- Includes a masked cocktail image reveal effect.

### `Menu.jsx`

- Implements an interactive cocktail carousel.
- Allows users to switch between cocktails using navigation buttons and tabs.
- Uses React state to manage the selected cocktail index.
- Animates image and text transitions with GSAP.

### `Contact.jsx`

- Displays location, contact details, opening times, and socials.
- Animates section copy and leaf graphics on scroll.
- Uses shared constants for opening hours and social icons.

## Data and Content

The application content is centralized in `constants/index.js`.

Key exported arrays and objects:

- `navLinks` — section navigation items
- `cocktailLists` — popular cocktail menu items
- `mockTailLists` — mocktail menu items
- `featureLists` / `goodLists` — highlights for the Art section
- `openingHours` — footer business hours
- `socials` — social link icons and URLs
- `allCocktails` — menu slider entries with images and descriptions

This makes it simple to update copy, prices, and section content without editing component logic.

## Styling and Assets

### `src/index.css`

- imports Google fonts and Tailwind CSS
- defines custom theme CSS variables and utilities
- styles layout, grid behavior, and custom classes used across components
- contains component-level selectors under `@layer components`

### Public Assets

- fonts are loaded from `public/fonts/`
- images in `public/images/` include leaves, drink photos, icons, and decorative textures
- video background is loaded from `public/videos/output.mp4`

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm

### Install

```bash
npm install
```

### Run Development Server

```bash
npm run dev
```

Then open the local URL shown in the terminal.

## Available Scripts

- `npm run dev` — start Vite development server
- `npm run build` — create a production build
- `npm run preview` — preview the production build locally
- `npm run lint` — run ESLint across the project

## How to Customize

### Update text and menu content

Edit `constants/index.js`:

- change `navLinks` titles and IDs
- update `cocktailLists` or `mockTailLists`
- modify `allCocktails` images, names, and descriptions
- adjust `openingHours` and `socials`

### Change animations

Edit component animation hooks in:

- `src/components/Hero.jsx`
- `src/components/Cocktails.jsx`
- `src/components/About.jsx`
- `src/components/Art.jsx`
- `src/components/Menu.jsx`
- `src/components/Contact.jsx`

### Adjust styling

Edit `src/index.css`:

- change theme variables under `@theme`
- add or modify Tailwind utilities
- update component style blocks inside `@layer components`

## Notes

- The app relies entirely on frontend rendering and static assets.
- `SplitText` is used for text animation and is imported from `gsap/all`.
- The `Menu` component uses a circular index system to keep slide navigation continuous.
- Some links in `constants/index.js` are placeholders and can be replaced with real URLs.

---

For deeper changes, start by editing the content in `constants/index.js` and then adjust section-specific styles or animation timelines as needed.

give a Star ⭐ if you like 
