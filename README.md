# Linton Evans | My Digital Skillset

An interactive 3D map of my skills. Every skill links back to the role or project where I used it.

## What's on the page

- A short boot sequence, then the constellation builds itself out of a particle swarm
- 8 domains and 73 skills you can orbit, zoom and click
- Pick a skill to see where I've used it, the skills it connects to and any certifications
- Pick a project or a role to light up every skill that went into it
- Search with `/` or Cmd K, a grid view, and a career timeline you can play from my first IT role through to 2026
- Return visits skip the intro. Replay intro brings it back.

## Running it locally

It's one page with no build step. Three.js loads from a CDN.

```bash
cd ~/Dev/3d-cv-portfolio
python3 -m http.server 3000 --bind 127.0.0.1
```

Then open http://127.0.0.1:3000 and add `?skip` to the address to jump past the intro.

## Updating the skills

Everything sits in the data section at the top of the script in `index.html`: `ROLES`, `PROJECTS`, `CERTS`, `DOMAINS` and `STAGES`.

Each skill lists its evidence. `role:n` is line n of that role, `p:id` is a project and `cert:id` is a certification. Connections between skills come from shared evidence, so there's nothing else to keep up to date.

`standalone.html` is a copy of `index.html`. Keep the two the same.

The `src` folder, `vite.config.js` and `package.json` belong to an older version of the site. The page doesn't use them.

## Hosting

GitHub Pages serves `main` at https://vteckz.github.io/skills/

`og-image.jpg` is the link preview image.

---
Built with Three.js
