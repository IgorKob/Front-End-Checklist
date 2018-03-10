[![Front-End Checklist Logo](https://github.com/thedaviddias/Front-End-Checklist/blob/master/src/img/banners/front-end-checklist-banner-light.jpg?raw=true)](https://frontendchecklist.io)

<h2 align="center"><a href="http://frontendchecklist.io">Front-End Checklist</a></h2>

<p align="center">
  <em>The Front-End Checklist це вичерпний список елементів сайта або HTML сторінки, котрі мають бути перевірені перед випуском в production</em>
</p>

[![Join the chat at https://gitter.im/Front-End-Checklist/Lobby](https://badges.gitter.im/Front-End-Checklist/Lobby.svg)](https://gitter.im/Front-End-Checklist/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
[![Backers on Open Collective](https://opencollective.com/front-end-checklist/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/front-end-checklist/sponsors/badge.svg)](#sponsors)
[![Contributors](https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg)](https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors)
[![StackShare](https://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/thedaviddias/front-end-checklist)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Він заснований на багаторічному досвіді front-end розробників і, окрім цього, включає в себе частини інших відкритих checklist-ів.

## Зміст

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[Web-шрифти](#web-шрифти)**
4. **[CSS](#css)**
5. **[Картинки](#Картинки)**
6. **[JavaScript](#javascript)**
7. **[Безпека](#Безпека)**
8. **[Продуктивність](#Продуктивність)**
9. **[Доступність](#Доступність)**
10. **[SEO](#seo)**

## Як цим користуватися?

Усі пункти **Front-End Checklist** обов'язкові для більшості сайтів, проте деякі елементи можуть бути менш важливі або взагалі пропущені (наприклад, якщо вам не потрібнен RSS для адмінки додатка). Ми обрали 3 рівня гнучкості:

* ![Low][low_img] означає, що пункт **рекомендований**, проте може бути пропущений в деяких випадках.
* ![Medium][medium_img] елемент **вкрай рекомендований** і може бути пропущений тільки в дуже специфічних ситуаціях. Невиконання деяких пунктів може мати негативні наслідки, наприклад, з точки зору продуктивності або SEO.
* ![High][high_img] такий пункт **обов'язковий**. Може зламати сторінку або призвести до проблем з доступністю (accessibility) і SEO. Перевіряйте такі елементи в першу чергу.

Деякі коментарі забезпечені іконками, щоб ви краще розуміли, який контент або допомогу можна знайти:

* 📖: документація або стаття
* 🛠: онлайн інструменти / утиліти для перевірки
* 📹: медіа- або відеоконтент

> Якщо хочете зробити внесок до ***Front-End Checklist App***, прочитайте [README_APP file](https://github.com/thedaviddias/Front-End-Checklist/blob/master/README_APP.md).

---

## Head

> **Примітка:** Можна подивитися [список усього](https://github.com/joshbuchea/HEAD), що може бути в `<head>` HTML документа.

### Мета-теги

* [ ] **Doctype:** ![High][high_img] Doctype стосується HTML5 і знаходиться нагорі HTML сторінок.

```html
<!doctype html> <!-- HTML5 -->
```

> * 📖 [Визначення кодування (англ.) - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

*Наступні 3 мета-тега (Charset, X-UA Compatible and Viewport) мають бути розташовані на самому початку `<head>`.*

* [ ] **Charset:** ![High][high_img] Кодування (UTF-8) задане правильно.

```html
<!-- Задати кодування документа -->
<meta charset="utf-8">
```

* [ ] **X-UA-Compatible:** ![Medium][medium_img] Тег X-UA-Compatible присутній.

```html
<!-- Проінструктує Internet Explorer використовувати останній двигунець рендерингу -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

> * 📖 [Задати режим сумісності Internet Explorer (англ.)](https://msdn.microsoft.com/en-us/library/jj676915(v=vs.85).aspx)

* [ ] **Viewport:** ![High][high_img] Viewport заданий правильно.

```html
<!-- Задати viewport для responsive дизайну -->
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

* [ ] **Title:** ![High][high_img] Заданий на всіх сторінках (SEO: Google розраховує ширину символів в title і обрізує приблизно від 472 до 482 пікселів. Тому межа довжини title близько 55 символів).

```html
<!-- Document Title -->
<title>Назва коротша за 55 символів</title>
```

> * 📖 [Title - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
> * 🛠 [SERP Snippet Generator](https://www.sistrix.com/serp-snippet-generator/)

* [ ] **Description:** ![High][high_img] Description заданий, унікальний і коротший за 150 символів.

```html
<!-- Meta Description -->
<meta name="description" content="Опис сторінки коротший за 150 символів">
```

> * 📖 [Meta Description - HTML - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Adding_an_author_and_description)

* [ ] **Favicons:** ![Medium][medium_img] Іконки відображають коректно. Якщо у вас тільки один `favicon.ico`, покладіть його в корінь сайта. Звичайно вам не треба нічого додавати в розмітку. Проте, хорошою практикою вважається робити посилання як в прикладі нижче. На сьогоднішній день **рекомендований PNG формат** замість `.ico`(роздільна здатність: 32x32px).

```html
<!-- Стандартний favicon -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Рекомендований формат favicon -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

> * 🛠 [Favicon Generator](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> * 📖 [Favicon шпаргалка](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Web App Meta:** ![Low][low_img] Задані мета-теги для Apple

```html
<!-- Apple Touch Icon (не менше, за 200x200px) -->
<link rel="apple-touch-icon" href="/custom-icon.png">

<!-- Розгорнути веб-додаток на повний екран -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Задає стиль для Status Bar (можливі значення дивись за посиланням Supported Meta Tags нижче) -->
<!-- Не має ефекта, якщо не виставлений попередній тег -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```

> * 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
> * 📖 [Supported Meta Tags](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

- [ ] **Windows Tiles:** ![Low][low_img] Windows tiles задані.

```html
<!-- Microsoft Tiles -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Мінімальний необхідний `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

> * 📖 [Browser configuration schema reference](https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx)

* [ ] **Canonical:** ![Medium][medium_img] Використовуйте `rel="canonical"` щоб уникнути дублювання контента.

```html
<!-- Допомогає уникнути проблем з дубльованим контентом -->
<link rel="canonical" href="http://example.com/2017/09/a-new-article-to-red.html">
```

> * 📖 [Use canonical URLs - Search Console Help - Google Support](https://support.google.com/webmasters/answer/139066?hl=en)
> * 📖 [5 common mistakes with rel=canonical - Google Webmaster Blog](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### HTML теги

* [ ] **Атрибут lang:** ![High][high_img] Атрибут `lang` заданий у відповідності до мови сторінки.

```html
<html lang="en">
```

* [ ] **Атрибут direction:** ![Medium][medium_img] Напрямок тексту заданий в цьому атрибуті тега `html`. Також цей атрибут може бути застосований до інших тегів.

```html
<html dir="rtl">
```

> * 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

* [ ] **Альтернативна мова:** ![Low][low_img] Тег мови заданий і відповідає мові сторінки.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es">
```

* [ ] **Умовні коментарі:** ![Low][low_img] Умовні коментарі задані для IE, якщо вимагається.

> * 📖 [About conditional comments (Internet Explorer) - MSDN - Microsoft](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **RSS feed:** ![Low][low_img] Якщо ваш проект є блогом чи містить сторінки, переконайтесь, що RSS налаштований.

* [ ] **Критичні CSS стилі задані inline:** ![Medium][medium_img] Критичний CSS (critical CSS) — CSS, який задає стилі контента видимого одразу поки відбувається процес завантаження сторінки ("above the fold content"). Мініфікуйте такий CSS і вставте всередині `<style></style>` перед завантаженням решти стилів.
> * 🛠 Інструмент для автоматизації: [Critical by Addy Osmani on GitHub](https://github.com/addyosmani/critical)

* [ ] **Порядок CSS:** ![High][high_img] Усі CSS файли мають завантажуватися перед будь-якими JavaScript файлами в `<head>`. (За вийнятком випадків, коли JS файли завантажуються асинхроно вгорі сторінки).

### Социальные сети

***Facebook OG*** і ***Twitter Cards*** вкрай рекомендовані для усіх сайтів. Додайте теги для інших соц. мереж, якщо плануєте відображатися в них коретно.

* [ ] **Facebook Open Graph:** ![Low][low_img] Усі теги All Facebook Open Graph (OG) протестовані, жоден не пропущений і інформація в них вірна. Картинки мають бути хоча б 600 x 315 пікселів. Рекомендована роздільна здатність 1200 x 630 пікселів.

> **Примітка:** Використовуйте `og:image:width` і `og:image:height` щоб вказати роздільну здатність для павука (the crawler) для того, щоб картинки могли бути відрендерені одразу ж. Інакше знадобиться асинхронне підвантаження і обробка.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<!-- Наступні теги не обов'язкові, але рекомендовані -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

> * 📖 [A Guide to Sharing for Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> * 📖 [Best Practices - Sharing](https://developers.facebook.com/docs/sharing/best-practices/)
> * 🛠 Протестуйте сторінку з [Facebook OG testing](https://developers.facebook.com/tools/debug/)

* [ ] **Twitter Card:** ![Low][low_img]

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

> * 📖 [Getting started with cards — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> * 🛠 Перевірте сторінку з [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ нагору](#Зміст)**

---

## HTML

### Найкращі практики

* [ ] **Семантичні елементи HTML5:** ![High][high_img] Семантичні елементи HTML5 використовуються потрібним чином (header, section, footer, main...).

> * 📖 [HTML Reference](http://htmlreference.io/)

* [ ] **Сторінки помилок:** ![High][high_img] Сторінки помилок 404 і 5xx існують. Не забувайте, що в сторінки помилок 5xx мають бути ввімкнені їх стилі, щоб обійтися без підвантаження з сервера.

* [ ] **Noopener:** ![Medium][medium_img] Посилання на зовнішні ресурси з `target="_blank"` мають мати атрибут `rel="noopener"`, щоб запобігти фішинговим атакам типу tab nabbing. Якщо треба підтримувати старі версії Firefox, використовуйте `rel="noopener noreferrer"`.

> * 📖 [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Видалення коментарів:** ![Low][low_img] Непотрібний код має бути видалений перед відправленням в production.

### Тестування HTML

* [ ] **W3C сумісність:** ![High][high_img] Всі сторінки мають бути перевірені W3C валідатором.

> * 🛠 [W3C validator](https://validator.w3.org/)

* [ ] **HTML Lint:** ![High][high_img] Інструменти, які допомогают аналізувати проблеми в HTML.

> * 🛠 [Dirty markup](https://dirtymarkup.com/)

> * 🛠 [Sonar a linting tool for the web](https://sonarwhal.com/)

* [ ] **Перевірка посилань:** ![High][high_img] Немає зламаних посилань, немає помилок 404.

> * 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

* [ ] **Перевірка на Adblock:** ![Medium][medium_img] Сайт коректно відображується з ввімкненимм блокувальними реклами на кшталт Adblock. Можете показати спеціальне повідомлення з проханням вимкнути подібні плагіни.



**[⬆ нагору](#Зміст)**

---

## Web-шрифти

> **Примітка:** Використання web-шрифтів може викликати мерехтіння або зникнення тексту (FOUT — Flash of Unstyled Text, FOIT - Flash of Invisible Text). Тому переконайтесь, що заданий резервний шрифт, або використовуйте завантажувальник шрифтів щоб тримати ситуацію під контролем.
> * 📖 [Google Technical considerations about webfonts](https://developers.google.com/fonts/docs/technical_considerations)

* [ ] **Формати web-шрифтів:** ![High][high_img] WOFF, WOFF2 і TTF підтримуються усіма браузерами.

> * 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - TrueType and OpenType font support](https://caniuse.com/#feat=ttf)
> * 📖 [Using @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Розмір web-шрифтів:** ![High][high_img] Розмір шрифтів сумарно не перевищує 2 MB.

* [ ] **Завантажувальник web-шрифтів:** ![Low][low_img] Контролюйте завантаження шрифтів за допомогою завантажувальника.

> * 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ нагору](#Зміст)**

---

## CSS

> **Примітка:** Ознайомтесь з [CSS guidelines](https://cssguidelin.es/) и [Sass Guidelines](https://sass-guidelin.es/), яких притримуються більшість розробників. Якщо у вас є сумніви щодо CSS властивостей, відвідайте [CSS Reference](http://cssreference.io/). Окрім цього погляньте на короткий гайд [Code Guide](http://codeguide.co/).

* [ ] **Чутливий (responsive) веб-дизайн:** ![High][high_img] Дизайн має бути чутливим.
* [ ] **CSS для друку:** ![Medium][medium_img] Стилі для друку задані і працюють коректно.
* [ ] **Препроцесори:** ![Low][low_img] Використовуйте CSS препроцесори (наприклад [Sass](http://sass-lang.com/), [Less](http://lesscss.org/), [Stylus](http://stylus-lang.com/)).
* [ ] **Унікальні ID:** ![High][high_img] Якщо використовуються Id, переконайтесь, що вони унікальні в межах сторінки.
* [ ] **Скидання (reset) CSS:** ![High][high_img] Використовуються актуальні версії інструментів для нормалізації CSS (reset, normalize или reboot). *(Якщо використовуєте CSS фреймворк типу Bootstrap або Foundation, Normalize вже в них ввімкнений.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS префікси:** ![Low][low_img] Всі класи і id, які використовуються в JS файлах, починаються з префікса **js-** і не беруть участь у призначенні стилів.

```html
<div id="js-slider" class="my-slider">
<!-- Або -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **Embedded або inline CSS:** ![High][high_img] Будь-якою ціною уникайте впровадження CSS в `<style>` теги (embeding) чи inline стилів. Застосовуйте такі підходи лише в особливих випадках, наприклад background-image для слайдера або critical CSS (див. вище).
* [ ] **Вендорні префікси:** ![High][high_img] CSS вендорні префікси використовуються і генеруються у відповідності до браузерів, що підтримуються.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Продуктивність CSS

- [ ] **Конкатенація:** ![High][high_img] CSS файли зконкатеновані в один файл. *(Не для HTTP/2)*.
- [ ] **Мініфікація:** ![High][high_img] Всі CSS файли мініфіковані.
- [ ] **Неблокуючий CSS:** ![Medium][medium_img] CSS файли мать бути такими, що не блокують DOM, щоб уникнути втрат часу.

> * 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
> * 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Невикористовуваний CSS:** ![Low][low_img] Видаліть стилі, що не використовуються.

> * 🛠 [UnCSS Online](https://uncss-online.com/)
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### Тестування CSS

* [ ] **Stylelint:** ![High][high_img] В CSS чи SCSS файлах немає помилок.

> * 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> * 📖 [Sass guidelines](https://sass-guidelin.es/)

* [ ] **Чутливий web-дизайн:** ![High][high_img] Всі сторінки були протестовані на наступних контролбни точках: 320px, 768px, 1024px (може бути більше в залежності від проекта).

* [ ] **CSS валідатор:** ![Medium][medium_img] CSS був протестований, помилки виправлені.

> * 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] **Desktop браузери:** ![High][high_img] Всі сторінки були протестовані на всіх desktop браузерах, що підтримуються (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Мобільні браузери:**  ![High][high_img] Всі сторінки були протестовані на всі мобільних браузерах, що підтримуються (Native browser, Chrome, Safari...).
* [ ] **ОС:**  ![High][high_img] Всі сторінки були протестовані на всіх ОС, що підтримуються (Windows, Android, iOS, Mac...).

- [ ] **Точна відповідність макету:** ![Low][low_img] В залежності від проекта і якості макета, перед вами може стояти задача зробити розмітку такою, що ідеально відповідає дизайну. Використовуйте спеціальні інструменти для перевірки вашої реалізації на відповідність макету. 

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Напрям тексту:** ![High][high_img] Всі сторінки мають бути протестовані в LTR і RTL мовах, якщо вони підтримуються.

> * 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ нагору](#Зміст)**

---

## Картинки

> **Примітка:** Для повного розуміння оптимізації картинок прочитайте безкоштовну електронну книгу **[Essential Image Optimization](https://images.guide/)** от Addy Osmani.

### Найкращі практики

* [ ] **Оптимізація:** ![High][high_img] Всі картинки оптимізовані для рендеринга в браузері. Формат WebP може бути використаний для критичних сторінок, наприклад, домашньої сторінки (Homepage).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 Використовуйте [ImageOptim](https://imageoptim.com/) для безкоштовної оптимізації картинок.
> * 🛠 Використовуйте [Kraken.io](https://kraken.io/web-interface) якк круту альтернативу для оптимізації png і jpg. До 1 Mb безкоштовно.
> * 🛠 Використовуйте [TinyPNG](https://tinypng.com/) для оптимізації png, apng (анімований png) і jpg без втрати якості. Є як платна, так і безкоштовна версія.
> * 🛠 [ZorroSVG](http://quasimondo.com/ZorroSVG/) jpg-подібне стиснення для прозорих картинок з використанням svg масок.
> * 🛠 [SVGO](https://github.com/svg/svgo) інструмент під Nodejs для оптимізації SVG файлів. 
> * 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) web версія SVGO для онлайн оптимізації SVG файлів.

* [ ] **Picture/Srcset:** ![Medium][medium_img] Використовуйте picture/srcset щоб задати найбільш відповідну картинку для поточного viewport.

> * 📖 [How to Build Responsive Images with srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Low][low_img] Ви використовуєте картинки більшого розміру 2x або 3x для підтримки дисплеїв retina.
* [ ] **Спрайти:** ![Medium][medium_img] Дрібні картинки об'єднані в спрайт файл. У випадку іконок це може бути SVG файл.
* [ ] **Width и Height:** ![High][high_img] Задайте атрибути `width` і `height` для `<img>` якщо розміри картинки зазделегідь відомі. Може бути пропущений для встановлення розмірів через CSS.
* [ ] **Альтернативний текст:** ![High][high_img] Для всіх `<img>` заданий альтернативниый текст, котрий описує картинку.

> * 📖 [Alt-texts: The Ultimate Guide](https://axesslab.com/alt-texts/)

* [ ] **Ліниве завантаження (lazy loading):** ![Medium][medium_img] Застосовується lazy loading для картинок (заданий резервний noscript).

**[⬆ нагору](#Зміст)**

---

## JavaScript

### Найкращі практики

* [ ] **JavaScript Inline:** ![High][high_img] Не використовується inline JavaScript (змішаний з HTML).
* [ ] **Конкатенація:** ![High][high_img] JavaScript файли зконкатеновані в один.
* [ ] **Мініфікація:** ![High][high_img] JavaScript файли мініфіковані. Можете додати суфікс `.min`.

> * 📖 [Minify Resources (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **Безпека JavaScript:** ![High][high_img]

> * 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **`noscript` tag:** ![Medium][medium_img] Використовуйте `<noscript>` всередині `<body>` щоб задати контент для ситуацій, коли скрипти не підтримуються або вимкнені в браузере. Корисно для Single Page Application (React, Angular і т.п.)
[Приклад](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498)

```html
<noscript>
  Для роботи додатка необхідно увімкнути JavaScript.
</noscript>
```

* [ ] **Неблокуючий JS:** ![Medium][medium_img] JavaScript файли завантажуються асинхронно з використанням атрибута `async` або відкладено з `defer`.

> * 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Оптимізовані і актуальні версії JS бібліотек:** ![Medium][medium_img] Переконайтесь, що всі JS библиотеки, що завнтажуються, дійсно необхідні, позбавтесь тих, що не використовуються. Нескладний функціонал краще реалізовувати на чистому (vanilla) JavaScript. Використовуйте останні версії бібліотек. В них менше помилок і вони безпечніші у порівнянні з застарілими версіями.

> * 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
> * 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

* [ ] **Modernizr:** ![Low][low_img] За допомогою кастомного Modernizr можна додавати класи до `<html>`.

> * 🛠 [Customize your Modernizr](https://modernizr.com/download?setclasses)

### Тестування JavaScript

* [ ] **ESLint:** ![High][high_img] ESLint не видав помилок, перевіряя ваш код. Можна використовувати вашу власну конфігурацію або стандартні правила.

> * 📖 [ESLint - The pluggable linting utility for JavaScript and JSX](https://eslint.org/)

**[⬆ нагору](#Зміст)**

---

## Безпека

### Проскануйте і перевірте ваш веб-сайт

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory by Mozilla](https://observatory.mozilla.org/)
> * [ASafaWeb - Automated Security Analyser for ASP.NET Websites](https://asafaweb.com/)

### Найкращі практики

* [ ] **HTTPS:** ![Medium][medium_img] HTTPS використовується на всіх сторінках, а також для усього стороннього контента (плагіни, картинки...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> * 🛠 [Free SSL Server Test](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] Виставлений HTTP заголовок 'Strict-Transport-Security'.

> * 🛠 [Check HSTS preload status and eligibility](https://hstspreload.org/)
> * 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> * 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

* [ ] **Захист від фальсифікації міжсайтових запитів (Cross Site Request Forgery - CSRF):** ![High][high_img] Ви гарантуєте, що запити на ваш сервер робляться саме вашим веб-сайтом, щоб уникнути атак CSRF.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)

* [ ] **Міжсайтовий скриптинг (Cross Site Scripting - XSS):** ![High][high_img] Ваш веб-сайт захищений від вразливостей XSS.

> * 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
> * 📖 [DOM based XSS Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

* [ ] **Заголовок Content-Type:** ![Medium][medium_img] Запобігти mime-sniff (аналіз контента і підміна заголовка content-type) в Google Chrome і Internet Explorer.

> * 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO):** ![Medium][medium_img] Захистіть своїх користуваів від атак типу clickjacking.

> * 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

* [ ] **Політика безпеки контента (Content Security Policy):** ![Medium][medium_img] Задайте правила, які визначають, який контент і звідки дозволено завантажувати на ваш сайт. Також це допоможе захиститися проти атак clickjacking.

> * 📖 [Content Security Policy - An Introduction - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP Cheat Sheet - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP Cheat Sheet - OWASP](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)
> * 📖 [Content Security Policy Reference](https://content-security-policy.com/)

**[⬆ нагору](#Зміст)**

---

## Продуктивність

### Найкращі практики

- [ ] **Вага сторінки:** ![High][high_img] Вага кожної сторінки має бути від 0 до 500 KB.

> * 🛠 [Website Page Analysis](https://tools.pingdom.com)
> * 🛠 [WebPageTest](https://www.webpagetest.org/)
> * 📖 [Size Limit: Make the Web lighter](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Мініфікація:** ![Medium][medium_img] Ваш HTML мініфікований.

* [ ] **Ліниве завантаження (Lazy loading):** ![Medium][medium_img] Використовуйте lazy loading для завантаження картинок, скриптів і CSS щоб зменшити час ініціалізації сторінки. Дивість детальніше у відповідних секціях чеклиста.

* [ ] **Розмір cookie:** ![Medium][medium_img] Якщо використовуєте cookies, переконайтесь, що їх розмір не перевищує 4096 байт. Також один домен не повинен використовувати більше 20 cookies.

> * 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)

* [ ] **Сторонні компоненти (Third party components):** ![Medium][medium_img] Iframe і сторонні компоненти, які покладаються на JS з інших доменів (на кшталт кнопок "Поділитися"), мають бути, за можливістю, замінені на ваші статичні компоненти, щоб зменшити число запитів і уникнути можливого витоку даних ваших користувачів.

> * 🛠 [Simple sharing buttons generator](https://simplesharingbuttons.com/)

### Підготовка майбутніх запитів (preparing upcoming requests)

> * 📖 [Explanation of the following techniques](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Low][low_img] DNS сторонніх компонентів позначені в `dns-prefetch`, щоб браузер міг розібратися з цими DNS заздалегідь.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnect:** ![Low][low_img] Використовуйте `preconnect`, щоб браузер міг здйснити DNS lookup, TCP handshake і TLS negotiation заздалегідь під час простоювання браузера.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetch:** ![Low][low_img] З використанням `prefetch` ресурси, котрі скоро можуть знадобитися, наприклад картинки с lazy loading, будуть підвантажені заздалегідь під час простоювання браузера.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preload:** ![Low][low_img] `preload` заздалегідь підвантажує ресурси, потрібні для поточної сторінки, наприклад, скрипти наприкінці `<body>`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Difference between prefetch and preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Тестування продуктивності

* [ ] **Google PageSpeed:** ![High][high_img] Всі сторінки протестовані і мають рейтинг хоча б 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Test your mobile speed with Google](https://testmysite.withgoogle.com)
> * 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Website speed and performance optimization](https://gtmetrix.com/)

**[⬆ нагору](#Зміст)**

---

## Доступність

> **Примітка:** Ознайомтесь з плейлистом [A11ycasts with Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Найкращі практики

- [ ] **Прогресивне покращення:** ![Medium][medium_img] Основний функціонал, наприклад навігація і пошук, мають працювати при вимкненому JavaScript.

> * 📖 [Enable / Disable JavaScript in Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Контрастність кольорів:** ![Medium][medium_img] Контрастність має відповідати WCAG AA (AAA для мобільних пристроїв).

> * 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Заголовки

* [ ] **H1:** ![High][high_img] На всіх сторінках є H1, який відрізняється від title сторінки.
* [ ] **Заголовки:** ![High][high_img] Заголовки мають йти в правильному порядку (від H1 до H6).

> * 📹 [Why headings and landmarks are so important -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

#### ARIA landmarks

- [ ] **Role banner:** ![High][high_img] У `<header>` проставлений `role="banner"`.
- [ ] **Role navigation:** ![High][high_img] у `<nav>` проставлений `role="navigation"`.
- [ ] **Role main:** ![High][high_img] У `<main>` проставлений `role="main"`.

> * 📖 [Using ARIA landmarks to identify regions of a page](https://www.w3.org/WAI/GL/wiki/Using_ARIA_landmarks_to_identify_regions_of_a_page)
> * 📖 [ARIA roles categorization](https://www.w3.org/TR/wai-aria/roles#roles_categorization)

### Семантика

- [ ] **Спеціальні типи input для HTML5:** ![Medium][medium_img] Це особливо важливо для мобільних пристроїв, так як там використовуються різні клавіатури для різних типів даних, що вводяться.

> * 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Форми

* [ ] **Label:** ![High][high_img] `<label>` заданий для кожного елемента форми. Якщо його застосувати не можна, використовуйте `aria-label`.

> * 📖 [Using the aria-label attribute - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Тестування доступності

* [ ] **Перевірка на відповідність стандартам:** ![High][high_img] Використовуйте інструмент WAVE для перевірки.

> * 🛠 [Wave testing](http://wave.webaim.org/)

* [ ] **Клавіатурна навігація:** ![High][high_img] Пройдіться по вашему сайту, використовуючи лише клавиатуру. Всі інтерактивні елементи мають быть доступні.
* [ ] **Screen-reader:** ![Medium][medium_img] Перевірте усі сторінки в программах для читання екрану (screen-reader) таких как VoiceOver, ChromeVox, NVDA чи Lynx.
* [ ] **Стилі для фокусу:** ![High][high_img] Якщо фокус заборонений, до елемента під фокусом мають застосовуватися спеціальні стилі.

> * 📹 [Managing Focus - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ нагору](#Зміст)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics встановлений і налаштований.
* [ ] **Логичні заголовки:** ![Medium][medium_img] Текст заголовків допомогає зрозуміти контент сторінки.
* [ ] **sitemap.xml:** ![High][high_img] sitemap.xml існує і заданий в Google Search Console (раніше Google Webmaster Tools).
* [ ] **robots.txt:** ![High][high_img] robots.txt не блокує сторінки.

> * 🛠 Перевірте robots.txt с [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Структуровані дані (Structured Data):** ![High][high_img] На сторінках використовуються перевірені і правильні структуровані дані. Вони допомогають павукам (crawlers) зрозуміти контент сторінки.

> * 📖 [Introduction to Structured Data - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 🛠 Перевірте свою сторінку з [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Повний список слів, що використовуються в структурованих даних [Schema.org Full Heirarchy](http://schema.org/docs/full.html)
> * 📖 [RDFa - Linked Data in HTML](https://rdfa.info/)
> * 📖 [JSON-LD](https://json-ld.org/)
> * 📖 [Microdata](https://www.w3.org/TR/microdata/)

* [ ] **HTML карта сайту:** ![Medium][medium_img] HTML карта сайту існує і доступна за посиланням в підвалі стоірнки.

> * 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)

* [ ] **Pagination теги:** ![Medium][medium_img] Задайте `rel="prev"` і `rel="next"` щоб показати, що контент розбитий на сторінки.

> * 🛠 [Pagination (rel="prev/next") Testing Tool](https://technicalseo.com/seo-tools/rel-prev-next/)

> * 📖 [Pagination guidelines - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Приклад: Pagination link tags для сторінки 2 з списку сторінок -->
<link rel="prev" href="https://example.com/?page=1">
<link rel="next" href="https://example.com/?page=3">
```

**[⬆ нагору](#Зміст)**

---

## Переклад

Front-End Checklist також доступний іншими мовами. Дякуємо усім перекладачам за приголомшливу роботу!

* 🇯🇵 Японська: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
* 🇪🇸 Іспанська: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
* 🇨🇳 Китайська: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
* 🇰🇷 Корейська: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
* 🇧🇷 Португальська: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
* 🇻🇳 В'єтнамська: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
* 🇹🇼 Традиціонна китайська: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)
* 🇫🇷 Французська: [ynizon/Front-End-Checklist](https://github.com/ynizon/Front-End-Checklist)
* 🇷🇺 Російська: [ungear/Front-End-Checklist](https://github.com/ungear/Front-End-Checklist)
* 🇹🇷 Турецька: [eraycetinay/Front-End-Checklist](https://github.com/eraycetinay/Front-End-Checklist)
* 🇩🇪 Німецька: [xfuture603/Front-End-Checklist](https://github.com/xFuture603/Front-End-Checklist)

---

## Front-End Checklist Badge

Вставте цей бейдж у ваш файл README, якщо хочете показати, що слідуєте цьому чеклисту!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ нагору](#Зміст)**

---

## Сприяння

**Створіть issue чи pull request щоб запропонувати зміну чи доповнення**

### Керівництво

Репозиторій **Front-End Checklist** складається з двох гілок:

#### 1. `master`

Ця гілка складаєтсья з файла `README.md`, який автоматично відображається на сайті [Front-End Checklist](http://frontendchecklist.com/).

#### 2. `develop`

Ця гілка використовуватиметься для внесення значних змін в структуру чи контент. Для усунення дрібних помилок і створення нових елементів переважно використовувати гілку master.

## Підтримка

Якщо у вас є питання чи побажання, без роздумів пишіть в Gitter або Twitter:

* [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Автор

**[David Dias](https://github.com/thedaviddias)**

## Помічники

Проект існує завдяки допомозі спільноти. [[Зробити внесок]](CONTRIBUTING.md).
<a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors"><img src="https://opencollective.com/front-end-checklist/contributors.svg?width=890" /></a>

## Прихильники

Дякую усім нашим прихильникам! 🙏 [[Стати прихильником](https://opencollective.com/front-end-checklist#backer)]

<a href="https://opencollective.com/front-end-checklist#backers" target="_blank"><img src="https://opencollective.com/front-end-checklist/backers.svg?width=890"></a>


## Патрони

Підтримати цей проект ставши патроном. Ваш логотип буде відображатися тут з посиланням на ваш сайт. [[Стати патроном](https://opencollective.com/front-end-checklist#sponsor)]

<a href="https://opencollective.com/front-end-checklist/sponsor/0/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/1/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/2/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/3/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/4/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/5/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/6/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/7/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/8/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/9/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/9/avatar.svg"></a>

## Ліцензія

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ нагору](#Зміст)**

[low_img]: https://front-end-checklist.now.sh/low.svg
[medium_img]: https://front-end-checklist.now.sh/medium.svg
[high_img]: https://front-end-checklist.now.sh/high.svg

Syncronized with commit 07b7ba6
