# Snorlax Raid Master

Standalone, static Pokémon TCG jumbo raid controller. This is a fan-made project, unaffiliated with The Pokémon Company.

## Run

Open `index.html` in a browser. Raid progress is saved in browser localStorage.

## Deploy to Cloudflare Pages

1. Create a GitHub repository and upload `index.html` and `README.md` to its root.
2. Cloudflare dashboard → Workers & Pages → Create application → Pages → Connect to Git.
3. Select the repository, production branch `main`, framework preset `None`, build command blank, output directory `/` (repository root).
4. Save and Deploy. Future commits to `main` automatically deploy.

## Rules prototype

- Separate physical Trainer/Energy deck (boss life) and boss-specific minion deck.
- Five minions on Bench, further summons enter a queue.
- Snorlax's G-Max Fall: 60 + 30 per Benched minion, requiring three Colourless Energy.
- Printed Pokémon and Trainer card effects are resolved physically; the app tracks results.
- Healing can target a minion or be stored as pending protection for Snorlax.
- Stage 1/2 minions enter directly; minions count as Active and Benched.
- Levels adjust damage required per Trainer card discarded.
