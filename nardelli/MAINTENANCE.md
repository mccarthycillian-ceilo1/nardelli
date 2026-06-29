# Nardelli Website Maintenance

## Before editing

Open Terminal:

​
cd ~/nardelli
git checkout content-updates
git pull
npm run dev

Open the local development URL shown in Terminal.

Usually:

​
http://localhost:4321/

## Editing pages

Most edits are made in:

​
src/pages/

Common pages:
- homepage: `src/pages/index.astro`
- Quick Start: `src/pages/quick-start.astro`
- Our House: `src/pages/house.astro`
- Castiglione: `src/pages/essentials.astro`
- Restaurants: `src/pages/restaurants.astro`
- Day Trips: `src/pages/day-trips.astro`
- Pools & Water: `src/pages/water.astro`
- Leaving: `src/pages/leaving-checklist.astro`

## Adding a new photo

1. Add the image to:

​
public/photos/

2. Use a simple filename, e.g.:

​
LakeTrasimeno.jpeg

3. Reference it in a page:

​
<img src="/photos/LakeTrasimeno.jpeg" alt="Lake Trasimeno" loading="lazy" />

4. Check locally with:

​
npm run dev

## Image checklist

If an image does not load:
- check the file is in `public/photos/`
- check the exact filename
- check capital letters
- check the extension `.jpg`, `.jpeg`, `.png`, etc.

Example:

​
House.jpeg

is not the same as:

​
house.jpeg

## Saving changes to GitHub

Check what changed:

​
git status

Commit and push to the working branch:

​
git add -A
git commit -m "Describe change"
git push

## Publishing to live site

Only do this when ready to update the public Netlify site.

​
cd ~/nardelli
git checkout content-updates
git pull
git checkout main
git pull
git merge content-updates
git push

Pushing to `main` triggers the Netlify deploy.

## Checking for uncommitted changes

​
git status

If it says:

​
working tree clean

there is nothing uncommitted.

## Checking for unpushed commits

​
git fetch
git status

If Git says the branch is ahead of origin, run:

​
git push

## Common problems

### Terminal says `zsh: command not found: #`

This happens if a comment line beginning with `#` was pasted into Terminal. Run only the actual command lines.

### Page content appears outside layout

Check that the page is structured like:

​
<Layout title="..." currentPath={Astro.url.pathname}>
...page content...
</Layout>

Do not accidentally write:

​
<Layout title="..." currentPath={Astro.url.pathname}></Layout>

with the content after it.

### Style block error

A page should have:

​
<style>
/ CSS here /
</style>

Do not put `</style>` before the CSS.

### Navigation active state not working

Each page should pass:

​
currentPath={Astro.url.pathname}

to the Layout:

​
<Layout title="..." currentPath={Astro.url.pathname}>

## Useful commands

Run local site:

​
npm run dev

Check branch:

​
git branch --show-current

Switch branch:

​
git checkout content-updates

Check changed files:

​
git status

Commit:

​
git add -A
git commit -m "Update copy"
git push
