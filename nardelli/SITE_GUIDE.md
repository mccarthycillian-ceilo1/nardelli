# Nardelli Site Guide

## Purpose of the site

This is a private guide website for family and friends staying at Nardelli Nespolo in Umbria, near the Tuscan border.

It is not a commercial rental website. Nardelli is a home away from home, shared with family and friends.

The main goals are to:
- help guests settle in quickly
- explain how the house works
- share local recommendations
- make arrival and leaving easier
- help people enjoy Lake Trasimeno, Umbria and Tuscany

## Tone and style

The tone should be:
- warm
- practical
- personal
- welcoming
- clear
- not overly polished or corporate

Avoid making the site sound like a hotel, Airbnb listing, or commercial rental. The house has quirks and personal touches, and that is part of the character.

## Design approach

The site uses a clean guide-style layout:
- simple navigation
- warm green colour palette
- card-based sections
- practical checklists
- hero sections with text and images
- maps at the bottom of recommendation pages

Most pages follow this pattern:
1. H1 page title
2. short intro / hero card
3. practical content sections
4. map if useful

## Page structure

Pages live in:

​
src/pages/

Main pages:

- `index.astro` — welcome / landing page
- `quick-start.astro` — first 10 minutes and arrival setup
- `house.astro` — house, garden, neighbours and map
- `essentials.astro` — Castiglione del Lago essentials and sights
- `restaurants.astro` — food, wine, restaurants and bars
- `day-trips.astro` — half-day and full-day trip ideas
- `water.astro` — beaches, pools and water activities
- `leaving-checklist.astro` — final checklist and goodbye message

## Layout

The shared layout is:

​
src/layouts/layouts.astro

This controls:
- page width
- navigation bar
- active navigation state
- global colours
- body typography
- map sizing
- mobile navigation

When editing the layout, be careful not to break:

​
<Layout ...>
...page content...
</Layout>

Each page’s content must stay inside the opening and closing Layout tags.

## Components

Shared components live in:

​
src/components/

Main components:

### `MapEmbed.astro`

Used to embed Google My Maps.

Example:

​
<MapEmbed
title="Pools & Water Activities"
src="https://www.google.com/maps/d/embed?mid=..."
/>

### `PhotoPlaceholder.astro`

Used where a future photo is planned.

## Photos

Photos used by the site live in:

​
public/photos/

Use local photos where possible instead of hotlinking external images.

Example:

​
<img
src="/photos/Restaurant.jpg"
alt="Food and wine in Umbria and Tuscany"
loading="lazy"
/>

Important:
- filenames are case-sensitive
- avoid spaces in filenames
- keep images reasonably small for web performance

Good file size target:
- most images: 100–600 KB
- avoid multi-MB images if possible

## Maps

Google My Maps are used for:
- Our House & Neighbours
- Castiglione del Lago
- Restaurants
- Day Trips
- Pools & Water Activities

Maps are generally placed near the bottom of each relevant page.

## Key content principles

### Homepage

Should explain:
- what Nardelli is
- that it is not rental accommodation
- that it is a home away from home shared with family and friends
- how the website helps guests

### Quick Start

Should stay practical:
- first 10 minutes
- parking
- keys and lockbox
- electricity
- water and gas mains
- boiler / hot water
- troubleshooting

### Restaurants

Should feel warm and local:
- Umbria and Tuscany food culture
- practical family timing note
- best restaurants and bars
- map at bottom

### Day Trips

Should inspire but stay practical:
- half-day and full-day options
- drive times
- parking notes
- map at bottom

### Leaving Checklist

Should feel warm, not transactional:
- “A Presto (see you soon)” message
- practical checklist
- reminder that the house is shared with family and friends

## Guidance for future AI assistants

When helping update this site:
1. Keep the warm, personal, practical tone.
2. Preserve the existing layout patterns.
3. Do not make it sound like a commercial rental listing.
4. Use local images in `public/photos/` where possible.
5. Check filename casing carefully.
6. Keep maps embedded using `MapEmbed`.
7. Keep edits on `content-updates` until the user is ready to publish.
8. Prefer small, safe changes over large rewrites.
9. If changing layout, check both desktop and mobile.
10. If the site looks broken, first check whether page content is inside `<Layout ..