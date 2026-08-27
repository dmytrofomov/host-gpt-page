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

Це **не** PlanEat AI з App Store. У копі лендінга це сказано прямо.

## Прод (майбутнє)

Робоча назва продукту: **FoodLoop**.

Щоб змінити бренд на сайті, досить:

1. Поля `window.SITE` на початку `index.html` (`brand`, `brandLong`, `domain`, `botUrl`, `botHandle`).
2. Файл `CNAME` (окремим кроком, не в цьому коміті) + `robots.txt` / `sitemap.xml` під новий хост.

Скрипт унизу `index.html` біндить `[data-site]` і оновлює title / OG / canonical / JSON-LD з цих полів.

## Візуал

- Лого: `logo.png` (pixel bowl + check, 640×640)
- Фон `#0d1f18`, акцент `#3dcc7a`, teal `#2a9d8f`, текст `#e8f0ea`
- Шрифти: Manrope + IBM Plex Mono (Google Fonts)

## Чесні рамки копі (не розмивати)

**Є в beta:** текст / фото / голос → КБЖВ → confirm; `/day` `/goals` `/history`; рецепти; `/plan` `/shopping` `/logplan`; експорт і видалення.

**Немає / не обіцяти:** медицина; PlanEat AI iOS; live-імпорт Instagram / TikTok; AI-дієтолог.

**Приватність:** сира їжа, промпти, Telegram-айді та фото не йдуть у телеметрію.

Немає вигаданих метрик, рейтингів і «тисяч користувачів». Немає тексту HostGPT як хостинг/оренда — домен лише адреса цього лендінга.
