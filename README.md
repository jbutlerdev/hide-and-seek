# 🔍 Hide and Seek Adventure

A fun browser-based hide and seek game with multiple themed levels!

## 🎮 Play Now

Play the game at: [https://jbutlerdev.github.io/hide-and-seek](https://jbutlerdev.github.io/hide-and-seek)

## 🎯 Game Features

- **4 Themed Levels:**
  - 🎃 Pumpkin Patch - Find cute animals among autumn decorations
  - 🚀 Outer Space - Discover aliens and space objects among the stars
  - 🎪 Playground - Hunt for toys and carnival items
  - 🚜 Farm - Locate farm animals among crops and farm elements

- **Gameplay:**
  - 10 hidden items per level
  - 60-second timer for each level
  - Interactive animations when items are found
  - Decorative elements that add challenge
  - Score tracking and victory/game over screens

## 🚀 How to Play

1. Choose a level from the main menu
2. Click on hidden items to find them
3. Find all 10 items before the 60-second timer runs out
4. Items blend in with decorations - look carefully!
5. Hover over items to see them grow slightly

## 🛠️ Deployment

### GitHub Pages (Current)

This site is automatically deployed to GitHub Pages via GitHub Actions whenever code is pushed to the `main` branch.

**Setup Instructions:**
1. Go to your repository Settings
2. Navigate to Pages (under Code and automation)
3. Under "Build and deployment":
   - Source: Select "GitHub Actions"
4. Push code to main branch
5. The workflow will automatically deploy your site

Your site will be available at: `https://[username].github.io/hide-and-seek`

### Quick (Shopify Internal)

Also deployed at: [https://hide-and-seek.quick.shopify.io](https://hide-and-seek.quick.shopify.io)

To deploy to Quick:
```bash
npm install -g @shopify/quick
quick deploy . hide-and-seek
```

## 📁 Project Structure

```
hide-and-seek/
├── index.html              # Main game file (self-contained)
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions workflow
├── README.md               # This file
├── AGENTS.md              # Quick platform documentation
└── CLAUDE.md              # Project instructions
```

## 🔧 Local Development

Simply open `index.html` in your web browser. No build process required!

## 📝 License

Free to use and modify.
