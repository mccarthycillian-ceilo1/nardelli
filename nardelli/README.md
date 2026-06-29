# Nardelli Website

Private guide website for family and friends staying at Nardelli Nespolo.

## Purpose

This site helps family and friends settle into the house, understand how things work, and enjoy the local area around Lake Trasimeno, Umbria and Tuscany.

It is not a commercial rental website. The tone should remain warm, personal and practical.

## Tech stack

- Astro static website
- GitHub repository for source code and backups
- Netlify for hosting and deployment
- Google My Maps for embedded location maps

## Local development

From Terminal:

​
cd ~/nardelli
git checkout content-updates
npm run dev

Then open the local URL shown in Terminal, usually:

​
http://localhost:4321/

## Main folders

Pages:

​
src/pages/

Layout:

​
src/layouts/layouts.astro

Components:

​
src/components/

Photos and static files:

​
public/photos/

## Key pages

- `src/pages/index.astro` — homepage / welcome page
- `src/pages/quick-start.astro` — arrival instructions and first 10 minutes
- `src/pages/house.astro` — Our House page
- `src/pages/essentials.astro` — Castiglione del Lago essentials and sights
- `src/pages/restaurants.astro` — restaurants, bars, food and wine recommendations
- `src/pages/day-trips.astro` — day trip ideas
- `src/pages/water.astro` — beaches, pools and water activities
- `src/pages/leaving-checklist.astro` — leaving checklist and goodbye message

## Adding photos

Save images into:

​
public/photos/

Then reference them like:

​
<img src="/photos/House.jpeg" alt="Nardelli house" loading="lazy" />

Important: filenames are case-sensitive.

For example:

​
House.jpeg

is different from:

​
house.jpeg

## Development workflow

Make edits on:

​
content-updates

Commit and push:

​
cd ~/nardelli
git checkout content-updates
git add -A
git commit -m "Describe change"
git push

## Publishing live

To publish changes to the live Netlify site:

​
cd ~/nardelli
git checkout content-updates
git pull
git checkout main
git pull
git merge content-updates
git push

Pushing to `main` triggers the Netlify production deploy.

## Live site

Netlify production URL:

​
https://lucent-medovik-6b2644.netlify.app/

## Common issues

### Image does not load

Check:
- the image is inside `public/photos/`
- the filename and extension match exactly
- the case matches exactly

### Layout breaks

Check:
- page content is inside `<Layout ...> ... </Layout>`
- there is no empty `<Layout ...></Layout>` before the page content
- every `<style>` block has one opening `<style>` and one closing `</style>`

### Terminal says `zsh: command not found: #`

This means a comment line beginning with `#` was pasted into Terminal. Ignore it and run only the actual commands.
​
