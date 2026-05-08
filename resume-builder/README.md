# ResumeForge — 110 Professional Resume Templates

A fully client-side resume builder with 110+ categorized templates, live preview, and PDF download.

## Features
- 110+ professionally designed templates
- 7 categories: Corporate, Tech, Creative, Medical, Academic, Modern, Bold, Elegant
- 3 layouts: Classic, Minimal, Sidebar
- Live canvas preview
- One-click PDF export
- No backend needed — 100% static HTML

## Deploy to Railway

### Option 1 — Static Site (Recommended)
1. Push this folder to a GitHub repo
2. Go to [railway.app](https://railway.app) → New Project → Deploy from GitHub
3. Select your repo
4. Railway auto-detects static HTML — set start command to: `npx serve .`
5. Done! Your site is live.

### Option 2 — With Express server
If you want a proper server:

```bash
npm init -y
npm install express
```

Create `server.js`:
```javascript
const express = require('express');
const path = require('path');
const app = express();
app.use(express.static(__dirname));
app.get('*', (req, res) => res.sendFile(path.join(__dirname, 'index.html')));
app.listen(process.env.PORT || 3000);
```

Add to `package.json`:
```json
"scripts": { "start": "node server.js" }
```

Push to GitHub → Deploy on Railway.

## Template Categories
| Category | Count | Best For |
|----------|-------|---------|
| Corporate | 20 | Finance, Consulting, Business |
| Tech | 20 | Engineering, Dev, Data Science |
| Creative | 15 | Design, Art, Media |
| Medical | 10 | Healthcare, Science |
| Academic | 10 | Research, Academia |
| Modern | 15 | General purpose |
| Bold | 10 | Stand-out applications |
| Elegant | 10 | International, Luxury |

## Local Development
Just open `index.html` in any browser — no build step needed.
