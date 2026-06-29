# Nardelli Website Toolkit

This is a high-level summary of the tools used to create and maintain the Nardelli website.

## Documentation files in this project

This project includes a few plain-English documentation files to help future-you, or a future AI assistant, understand and maintain the site.

- `README.md` — practical project overview: how the site is structured, how to run it locally, where pages/photos live, and how to publish changes.
- `SITE_GUIDE.md` — content and design guide: explains the purpose of the site, tone of voice, page structure, layout patterns, and guidance for future edits.
- `MAINTENANCE.md` — step-by-step maintenance checklist: common commands, how to edit, commit, push, publish, and troubleshoot common issues.
- `TOOLKIT.md` — high-level summary of the tools and services used to create and maintain the site, including Astro, VS Code, Terminal, Git, GitHub, Netlify, Google My Maps, and AI assistance.

## Notion AI / AI assistant

Used as the main coding and content assistant.

Main uses:
- writing and refining website copy
- generating Astro code snippets
- troubleshooting errors
- guiding Git and Terminal commands
- planning page structure and layout
- documenting the site for future maintenance

## Astro

The website framework.

Astro is used to create the static website pages. Each page lives in `src/pages/` and uses `.astro` files.

## VS Code

The code editor.

Used to:
- open the project folder
- edit `.astro`, `.md`, and other files
- manage page content
- add and update documentation files

## Terminal

Command-line tool on Mac.

Used to:
- run the site locally
- use Git commands
- check files
- commit and push changes
- merge updates into main

Common command:

​
npm run dev

## Git

Version control system.

Used to:
- track changes
- save versions of the site
- work on a branch before publishing
- merge updates into the live branch

Main branches:
- `content-updates` — working branch
- `main` — production branch

## GitHub

Online home for the code repository.

Used to:
- back up the website code and photos
- store commit history
- connect to Netlify for deployment

If changing laptop in future, clone the GitHub repository to recover the site.

## Netlify

Hosting and deployment platform.

Used to:
- host the live website
- automatically deploy when `main` is pushed

Live site:

​
https://lucent-medovik-6b2644.netlify.app/

## Google My Maps

Used to create custom maps for:
- restaurants
- day trips
- water activities
- house and neighbours
- Castiglione del Lago

The maps are embedded into the site using iframe links through the `MapEmbed` component.

## Google Maps links

Used for:
- parking locations
- restaurants
- beaches
- day trip destinations

These are included as normal links in the website copy.

## Public photos folder

Website images are stored in:

​
public/photos/

This makes them available on the website using paths like:

​
/photos/House.jpeg

## GitHub + photos

Photos inside `public/photos/` are safe once committed and pushed to GitHub.

If changing laptop, the photos will come back when the repository is cloned.

## Google Drive or iCloud Photos

Useful for storing original high-resolution photo backups.

Not recommended as the primary source for website images, because shared links can break or have permissions issues.

Best approach:
- keep original photos in Google Drive or iCloud if desired
- keep optimized website versions in `public/photos/`
- commit website versions to GitHub

## Netlify live review

After publishing to `main`, review the site on:
- desktop
- iPhone Safari
- mobile navigation
- image loading
- embedded maps
- video playback on Quick Start page
​

