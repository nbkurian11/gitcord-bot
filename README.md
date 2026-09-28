# Gitcord (WIP)

A Discord bot that tracks GitHub coding streaks, built to get friends competing with each other and programming more every day.


## How it works

1. Each member links their GitHub username to their Discord account.
2. Once a day, Gitcord checks everyone's GitHub contribution calendar (the green squares).
3. Each person gets a personal role showing their current streak, like **🔥 Day 42**.
4. Miss a full day with no contributions and your streak resets to **Day 0**.

No manual check-ins. If you pushed code, it counts.

## Features (planned)

- [ ] Automatic streak tracking from GitHub contributions
- [ ] Personal "Day N" role for each member, updated daily
- [ ] `/link` to connect your GitHub account
- [ ] `/streak` to see your current streak
- [ ] `/leaderboard` to see who's on top
- [ ] Daily streak update message

## Tech stack

- Python 3
- [discord.py](https://discordpy.readthedocs.io/)
- GitHub GraphQL API
- SQLite

## Setup

1. Clone the repo:
```bash
   git clone https://github.com/nbkurian11/gitcord-bot.git
   cd gitcord-bot
```
2. Create and activate a virtual environment:
```bash
   python -m venv .venv
   .venv\Scripts\activate        # Windows
   source .venv/bin/activate     # Mac/Linux
```
3. Install dependencies:
```bash
   pip install -r requirements.txt
```
4. Create a `.env` file in the project root:
```
   DISCORD_TOKEN=your-bot-token
   GUILD_ID=your-server-id
   GITHUB_TOKEN=your-github-token
```
5. Run the bot:
```bash
   python bot.py
```

## Notes on how GitHub counts contributions

- Commits only count if they're pushed to a repo's **default branch** (usually `main`) and made with an email linked to your GitHub account.
- To count private repo activity, enable **"Include private contributions"** in your GitHub profile settings.



