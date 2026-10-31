# Qernix Discord bot

This bot manages simulated balances only. No real cryptocurrency is transferred.

## Python hosting

Use Python 3.11 or newer. Import this repository into your host.

Install command: `pip install -r requirements.txt`

Startup command: `python bot.py`

Set private environment variables in your host's panel:

- `DISCORD_TOKEN`: your current Discord bot token
- `WALLET_API`: `https://qernix-alpha.vercel.app`
- `WALLET_API_KEY`: the same private key configured in the Qernix Vercel project

Do not commit tokens or environment files. Stop your local bot before starting the hosted copy to avoid duplicate replies. Keep one replica running. The `ExodusCopy` directory stores the alert history and local ledger; keep this directory on persistent storage to avoid duplicate old panic announcements after restarts.

## Commands

`/send coin amount wallet` queues a simulated transfer. Use `exodus` for flku or `exodus2` for x. The desktop app polls the shared Vercel API and applies a 10-second delay.

On Bot-Hosting.net the free plan currently requires manual renewal every four days; check the provider's current plan terms.
