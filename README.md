# List Reel — a Claude skill

A Claude skill for making short vertical **"20 Things" list reels**: 20 Loading Animations, 20 Button Hover Effects, 20 App Onboarding Screens and so on. Each example plays for about a second while a numbered list fills in, and the reel ends on a grid of every example.

The skill doesn't come with a fixed look. It asks for your own colours, fonts and handle, and lets you pick from four layouts, so your reels look like yours.

## Install

**Claude apps (claude.ai, desktop):**

1. Download `list-reel.zip` from the [latest release](../../releases/latest), or zip the `list-reel` folder yourself.
2. Open **Settings → Capabilities → Skills** and upload the zip.

**Claude Code:**

```bash
git clone https://github.com/crownzdesigns-gif/list-reel-skill.git
cp -r list-reel-skill/list-reel ~/.claude/skills/
```

## Use

Ask Claude something like:

> Make a list reel about 20 card hover effects.

Claude will ask for your topic, brand kit and layout, draft the list for you to approve, then build and render the reel.

## What's inside

```
list-reel/
└── SKILL.md   # the instructions Claude follows
```

## License

MIT. Use it and make it your own.
