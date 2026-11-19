# Tupande Work Planning (Asili field cascade)

A prototype for planning the week down the Asili field structure: Region > Area > Zone > Territory, with
Tupande Agents (credit sales and extension) and Duka Assistants (cash sales at the dukas) working to
separate priority sets. **All data is made up.**

- Live site: served by Vercel from this repository (`index.html` at the root).
- Farm Planner (a separate site): https://asili-listen.vercel.app/planner/ — linked from the Enrolment pillar.

## Work on it

No dependencies, only Node.js.

1. `node test.js` — engine tests; should end with "all passed".
2. `node build.js` — rebuilds `index.html` from `src/`. **Commit the rebuilt `index.html`**: Vercel serves it as it is and runs no build.
3. Open `index.html` in a browser to try it.

Edit files in `src/` (template, styles, engine, app), rebuild, reload.

## Put it on Vercel

1. vercel.com → **Add New… → Project** → import this repository.
2. Framework Preset **Other**, Root Directory `./`, no build command, no environment variables → **Deploy**.
3. Settings → **Deployment Protection** → Vercel Authentication **Standard Protection** (or off), Password Protection off,
   so anyone with the link can open the production address without signing in.
4. Share `https://<project-name>.vercel.app/`.

Every push to the production branch (normally `main`) goes live in a minute or two.

## Saving

The Vercel copy does not save changes: they reset on reload. The claude.ai copy
(`work-planning.artifact.html`, also written by `node build.js`) saves for everyone it is shared with.
