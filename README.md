# Player-Facing Campaign Wiki

A reusable, player-facing D&D 5e campaign wiki built with [Quartz](https://quartz.jzhao.xyz/). The pages in `content/` are a starting structure for adventure logs, the dramatis personae, locations, factions, lore, and handouts. Replace the prompts with details your players are cleared to know.

## Get started

1. Use GitHub's **Use this template** button if it is available, or clone this repository into a new one.
2. Install the dependencies with `npm install`.
3. Edit `content/start-here.md` and `content/campaign-guide.md` for your table.
4. Preview the wiki locally with `npx quartz build --serve`.

The starter configuration is in `quartz.config.default.yaml`. Update `pageTitle` and `baseUrl` there before publishing. See the [Quartz hosting guide](https://quartz.jzhao.xyz/hosting) for deployment options.

## Included pages

- Start Here and a campaign guide
- Adventure log and a reusable session page
- Dramatis personae, locations, factions, lore, and handout indexes with reusable page templates

## GM-only material: keep it out of the public repo

This project is configured for a **player-facing public site**. Do not put secrets, unrevealed plot details, or private player information in published pages.

- If you need local GM notes, place them in `content/gm-only/`. Quartz ignores that folder during builds, and Git ignores it so it will not be committed by accident.
- Verify the folder is ignored with `git check-ignore content/gm-only/` before adding notes. Do not force-add it, and do not put GM-only assets elsewhere under `content/`.
- Build filters only affect the generated site; they do not protect files committed to Git or present in Git history. For sensitive material, keep it outside this repository.
- Do not rely on password-protected/encrypted pages as secure GM storage. Client-side encryption is not a substitute for keeping secrets out of the public source repository.

Quartz's original documentation and source code remain available in `docs/` and `quartz/`.
