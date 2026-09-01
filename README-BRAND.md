# Brand — landing-site

Статичний лендінг під GitHub Pages. **CNAME у цей каталог не класти**, поки не буде окремого рішення по домену.

## Зараз (public)

| Поле | Значення |
|---|---|
| `brand` | PlanEat |
| `brandLong` | PlanEat у Telegram |
| `domain` | https://hostgpt.org/ |
| `botUrl` | https://t.me/plan_eat_ai_bot |
| `botHandle` | @plan_eat_ai_bot |
| Статус | closed beta |

## Прод (майбутнє)

Робоча назва продукту: **FoodLoop**.

Щоб змінити бренд на сайті, досить:

1. Поля `window.SITE` на початку `index.html` (`brand`, `brandLong`, `domain`, `botUrl`, `botHandle`).
2. Файл `CNAME` (окремим кроком, не в цьому коміті) + `robots.txt` / `sitemap.xml` під новий хост.

Скрипт унизу `index.html` біндить `[data-site]` і оновлює title / OG / canonical / JSON-LD з цих полів.

## Візуал

- Лого: `logo.png` (pixel bowl + check, 640×640) — лише дрібно в хедері / favicon, не як hero
- Папір `#f6f0e6`, картка `#fffaf2`, чорнило `#1c1a16`, приглушене `#6b6458`, ліс `#163226` / `#12281F`, акцент `#1f7a45`, м’ята `#4FD98A`, волосся `#e4d9c8`
- Шрифти: Fraunces (заголовки) + Manrope (тіло), один Google Fonts stylesheet
- Hero: кухонний натюрморт `img/hero.jpg` + CSS-чат у стилі Telegram (не гігантське лого)
- Інші стілли: `img/plate.jpg`, `img/market.jpg`; шаринг: `img/og.jpg`
- Телефон на лендінгу має 4 сцени (лог / день / план / покупки) — копія з каталогів бота, не вигаданий UI
- `color-scheme: light`, `theme-color` = ліс `#12281F`

## Чесні рамки копі (не розмивати)

**Є в beta:** текст / фото / голос → КБЖВ → confirm; день і цілі; свої рецепти; план і покупки; експорт і видалення.

**На публічному лендінгу не згадувати:** слеш-команди; телеметрію / сирий текст / фото-архів; PlanEat AI (iOS) / App Store.

**Немає / не обіцяти:** медицина; live-імпорт Instagram / TikTok; AI-дієтолог.

Немає вигаданих метрик, рейтингів і «тисяч користувачів». Немає тексту HostGPT як хостинг/оренда — домен лише адреса цього лендінга.
