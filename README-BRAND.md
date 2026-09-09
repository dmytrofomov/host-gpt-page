# FoodLoop — landing and brand kit

Public landing: https://hostgpt.org/ · Brand kit: https://hostgpt.org/brand/

Static GitHub Pages, published from `master:/docs`. Existing `docs/CNAME` points to `hostgpt.org`.

## Public identity

Product name: **FoodLoop**. Current Telegram URL: **https://t.me/plan_eat_ai_bot**.
The Telegram username stays live until the bot itself is renamed. Update `window.SITE` plus static HTML / metadata when the actual address changes.

Main line: **Твоя їжа. Твій ритм.**

Brand rules, downloadable assets, copy examples and image provenance are in `docs/brand/README.md` and `docs/brand/prompts.md`. `docs/brand/index.html` is the public gallery. `docs/brand/foodloop-brand-kit.zip` contains editable sources, photographs, icons and finished promotion images.

## Site files

- `docs/index.html`: Ukrainian landing, static SEO / OG / JSON-LD, current bot links.
- `docs/styles.css`: shared layout and Telegram demo.
- `docs/foodloop.css`: FoodLoop identity, responsive photo hero and editorial section.
- `docs/app.js`: brand binding, sticky CTA, keyboard-accessible demo tabs.
- `docs/brand/`: SVG/PNG identity, 12 SVG icons, 3 original photos, 4 promotion exports.
- `docs/img/foodloop-*.webp`: optimized photos. Original older assets retained for compatibility.

## Regenerate and check

Node dependencies: `sharp`, `playwright`. Browser: installed Chrome, or set `CHROME_PATH`.

```powershell
node scripts/build-brand.cjs
node scripts/check-site.cjs --export
python scripts/package-brand.py
node scripts/check-site.cjs
```

Verification runs a local HTTP server and headless Chrome, checks 1440/768/390/320 px layouts, every demo tab, keyboard controls, FAQ, current Telegram links, image loading, JSON-LD, no-JavaScript content and brand downloads. Screenshots and the report go to ignored `output/`.

## Copy boundaries

Closed beta: text/photo/voice → approximate nutrition draft → user confirmation; diary/goals; own recipes; plan/shopping; data export/deletion. Do not claim medical advice, exact nutritional measurements, automatic imported social-media recipes, guaranteed outcomes, user statistics or an unannounced price. Marketing mockups are illustrative.

The bot code and Telegram account are managed separately. This deployment changes the website and promotional identity.
