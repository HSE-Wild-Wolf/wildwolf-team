@AGENTS.md

## How changes go live (read first)

This app is live at https://wildwolf-team.vercel.app. Vercel deploys it automatically from GitHub: anything pushed to the `main` branch of HSE-Wild-Wolf/wildwolf-team goes live within a couple of minutes. Until Vercel's production branch for wildwolf-team is switched to main, it still deploys from claude/warehouse-daily-brief-inventory-lkhapf.

- Start each session with `git pull` so you have the latest code.
- Work directly on `main`. Don't create other branches or pull requests unless the user asks: work on other branches only makes a preview and never goes live.
- When a change is finished, commit it and push to `main`. That push is the deploy. Then tell the user the live link.
- For now, also run `git push origin main:claude/warehouse-daily-brief-inventory-lkhapf` after pushing, because that branch is still the one Vercel puts live. Drop this step once Vercel is switched to main.
- Never deploy with the Vercel CLI (`vercel`, `vercel --prod`) from this folder. A hand deploy skips GitHub and gets overwritten by the next push.
- Never commit `.env*` files or API keys. Secrets live in the Vercel project's Environment Variables.
- This project's folder on the main computer is C:\Users\atown\Wild Wolf\wildwolf-team.
