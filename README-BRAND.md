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

- Файли: `docs/index.html` (розмітка + `window.SITE`), `docs/styles.css`, `docs/app.js` (бінд бренду, хедер, reveal, таби телефону). Без збірки — статичний GitHub Pages з `docs/`.
- Лого: `img/icon.svg` (pixel bowl + check, з `foodbot/assets/brand/planeat-icon.svg`) у хедері / футері / CTA; `img/avatar.png` — аватар бота в мокапі Telegram; `logo.png` — favicon/apple-touch-icon
- Фон `#faf7f1` / тінт `#f3eee4`, поверхня `#fff`, чорнило `#14201a`, приглушене `#5f6b64`, ліс `#163226` / `#12281F`, акцент `#1f7a45`, м’ята `#4FD98A` / `#e3f7eb`, жовток `#ffc94d`, томат `#ff7a5c`, волосся `#e8e2d6`
- Шрифти: Manrope 800 для заголовків і тіла; Fraunces italic лише для акцентного слова в h1/h2 (`<em>`). Один Google Fonts stylesheet
- Hero: світлий, з м’якими glow-плямами (м’ята / жовток / томат) і крапковою сіткою; праворуч — реалістичний мокап телефону з Telegram-чатом і CSS-хореографією (фото → typing → чернетка → тап → «Страву записано» + прогрес дня)
- Стрічка-тікер під hero — приклади фраз, які реально можна надіслати боту («борщ + хліб», «як завжди», «там ще сметана»)
- Розділи: Як працює (3 кроки) → Можливості (bento 7 карток) → Всередині бота (телефон з 4 сценами: лог / день / план / покупки, автоперемикання, пауза при hover/фокусі, `?scene=plan` відкриває сцену) → Принципи (темна секція) → Чим не є → FAQ → CTA-картка → футер
- Сцени телефону та підписи кнопок — копія рядків з каталогів бота (`FoodBot.Infrastructure/Localization/Catalogs`), не вигаданий UI
- Фото: `img/hero.jpg` (пузир з фото в чаті), `img/plate.jpg` (bento «Лог»), `img/market.jpg` («Чим не є»); шаринг: `img/og.jpg`
- `color-scheme: light`, `theme-color` = ліс `#12281F`; `prefers-reduced-motion` вимикає всі анімації

## Чесні рамки копі (не розмивати)

**Є в beta:** текст / фото / голос → КБЖВ → confirm; день і цілі; свої рецепти; план і покупки; експорт і видалення.

**На публічному лендінгу не згадувати:** слеш-команди; телеметрію / сирий текст / фото-архів; PlanEat AI (iOS) / App Store.

**Немає / не обіцяти:** медицина; live-імпорт Instagram / TikTok; AI-дієтолог.

Немає вигаданих метрик, рейтингів і «тисяч користувачів». Немає тексту HostGPT як хостинг/оренда — домен лише адреса цього лендінга.
