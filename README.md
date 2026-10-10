# A.K Barber: концепт сайту (головна + меню)

Статичний сайт без збірки. Дизайн за ТЗ (розділ 20): темна графітова база, латунний акцент #C9A227, Hanken Grotesk для інтерфейсу, Bodoni Moda для заголовків.

## Структура

```
index.html                 Головна (усі 11 блоків з розділу 4 ТЗ)
services/index.html        Послуги
barbers/index.html         Майстри
gallery/index.html         Галерея (фільтри працюють)
pricing/index.html         Ціни (акордеон)
about/index.html           Про нас
contact/index.html         Контакти (форма в демо-режимі)
assets/css/tokens.css      Токени з ТЗ (кольори, радіуси, відступи, типографіка)
assets/css/base.css        Компоненти й розкладка
assets/js/site.js          Меню-шухляда, статус «Open/Closed», фільтри галереї, карусель, форма
assets/fonts/              Шрифти (локально, без Google Fonts)
robots.txt                 Disallow: / (демо)
```

Сторінки з ТЗ, яких тут ще немає: /book, /services/{slug}, /barbers/{slug}, /locations, /gift-cards, /shop, /blog, /reviews, /faq, /careers, /legal/*, /account/*.

## Публікація на Cloudflare Pages

1. Cloudflare dashboard, Workers & Pages, Create, Pages, Upload assets.
2. Завантажте вміст цієї папки (так, щоб `index.html` лежав у корені).
3. Назва проєкту дасть адресу `назва.pages.dev`.

Або через консоль: `npx wrangler pages deploy . --project-name=ak-barber-demo`

## Перед показом власнику

- Усі жовті підкреслені тексти в дужках (`[£XX]`, `[Barber name]`, `[email address]`, `@handle`) це плейсхолдери. Їх треба замінити реальними даними.
- Реальні дані: назва, адреса, телефон, години, рейтинг 5.0 (101 відгук) і три уривки відгуків із Google Maps.
- Послуги Shave і Kids узяті з ТЗ, їх наявність треба підтвердити. Блоки Parking і Walk-ins welcome з ТЗ не додано, бо це не підтверджено.
- Кнопка «Book now» ведеться на дзвінок (`tel:`). Коли з'явиться онлайн-запис, її слід перемкнути на /book.
- На сторінках стоїть `noindex`. Для бойового запуску прибрати його і вміст robots.txt.
- Фото й відео в слотах (hero, майстри, галерея, соцмережі) замінити реальними.
