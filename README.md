<h1 align="center">
<br>
  <img src="https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/data/images/logo-front-end-checklist.jpg" alt="Front-End Checklist" width="130">
  <br>
    <br>
  Checklista Frontend
  <br>
</h1>

<h4 align="center">Lista kontrolna frontend to wyczerpująca lista wszystkich elementów, które potrzebujesz mieć / musisz przetestować przed uruchomieniem witryny/strony HTML w produkcji.</h4>

<p align="center">
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome">
  </a>
    <a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg?style=flat-square" alt="Contributors">
  </a>
  <a href="https://github.com/thedaviddias/Front-End-Checklist/">
    <img src="https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg?style=flat-square" alt="Front‑End_Checklist followed">
  </a>
    <a href="https://creativecommons.org/publicdomain/zero/1.0/">
    <img src="https://img.shields.io/badge/license-CC0-green.svg?style=flat-square" alt="CC0">
  </a>
</p>

<p align="center">
  <a href="#how-to-use">Jak korzystać</a> • <a href="#contributing">Współtworzenie</a> • <a href="https://frontendchecklist.io">Strona</a> • <a href="https://www.producthunt.com/posts/front-end-checklist">Product Hunt</a>
</p>
<p align="center">
    <span>Inne Checklisty:</span>
    <br>
  <a href="https://github.com/thedaviddias/Front-End-Performance-Checklist#---------front-end-performance-checklist-">🎮 Front-End Performance Checklist</a> • <a href="https://github.com/thedaviddias/Front-End-Design-Checklist#front-end-design-checklist">💎 Front-End Design Checklist</a>
</p>


Opiera się ona na wieloletnim doświadczeniu programistów frontend, a dodatki pochodzą z innych list kontrolnych typu open source.

## Spis treści

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[Webfonts](#webfonts)**
4. **[CSS](#css)**
5. **[Images](#images)**
6. **[JavaScript](#javascript)**
7. **[Security](#security)**
8. **[Performance](#performance-1)**
9. **[Accessibility](#accessibility)**
10. **[SEO](#seo)**
11. **[Translations](#translations)**

---

## Jak korzystać?

Wszystkie elementy w **Checkliście Front-End** są wymagane w przypadku większości projektów, ale niektóre elementy można pominąć lub nie są one niezbędne (w przypadku administracyjnej aplikacji internetowej może nie być potrzebny na przykład kanał RSS). Wybieramy 3 poziomy elastyczności:

* ![Niski][low_img] oznacza, że element jest **zalecany**, ale można go pominąć w niektórych szczególnych sytuacjach.
* ![Średni][medium_img] oznacza, że element jest **wysoce zalecany** i może zostać ostatecznie pominięty w niektórych naprawdę szczególnych przypadkach. Niektóre elementy, jeśli zostaną pominięte, mogą mieć negatywne skutki pod względem wydajności lub SEO.
* ![Wysoki][high_img] oznacza, że elementu **nie można pominąć** z jakiegokolwiek powodu. Możesz spowodować dysfunkcję strony lub problemy z dostępnością lub SEO. Priorytetem testów muszą być najpierw te elementy.

Niektóre materiały zawierają emotikony, które pomagają zrozumieć, jaki rodzaj treści / pomocy można znaleźć na liście kontrolnej:

* 📖: dokumentacja lub artykuł
* 🛠: narzędzie online / narzędzie testujące
* 📹: treści multimedialne lub wideo

> Możesz przyczynić się do ***Front-End Checklist App*** czytając [plik README_APP](https://github.com/thedaviddias/Front-End-Checklist/blob/master/README_APP.md), który wyjaśnia wszystko odnośnie projektu.

---

## Head

> **Uwagi:** Możesz znaleźć [listę wszystkiego](https://github.com/joshbuchea/HEAD) co powinno znaleźć się w `<head>` dokumentu HTML.

### Meta tag

* [ ] **Doctype:** ![High][high_img] Doctype to HTML5 i znajduje się na górze wszystkich stron HTML.

```html
<!doctype html> <!-- HTML5 -->
```

> * 📖 [Determining the character encoding - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

*Następne 2 meta tagi (Charset oraz Viewport) muszą być na pierwszym miejscu w head.*

* [ ] **Charset:** ![High][high_img] Charset (UTF-8) jest zadeklarowany poprawnie.

```html
<!-- Ustaw kodowanie znaków dla dokumentu -->
<meta charset="utf-8">
```

* [ ] **Viewport:** ![High][high_img] Viewport jest zadeklarowany poprawnie.

```html
<!-- Viewport do responsywnego projektowania stron internetowych -->
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

* [ ] **Title:** ![High][high_img] Tytuł jest używany na wszystkich stronach (SEO: Google oblicza szerokość pikseli znaków użytych w tytule i odcina od 472 do 482 pikseli. Średni limit znaków wynosiłby około 55 znaków).

```html
<!-- Tytuł dokumentu -->
<title>Tytuł strony z mniej niż 55 znaków</title>
```

> * 📖 [Title - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
> * 🛠 [SERP Snippet Generator](https://www.sistrix.com/serp-snippet-generator/)

* [ ] **Opis:** ![High][high_img] Opis meta jest podany, jest unikalny i nie ma więcej niż 150 znaków.

```html
<!-- Opis Meta -->
<meta name="description" content="Opis strony, mniej niż 150 znaków">
```

> * 📖 [Meta Description - HTML - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Adding_an_author_and_description)

* [ ] **Favicons:** ![Medium][medium_img] Każdy favicon został utworzony i wyświetla się poprawnie. Jeśli masz tylko `favicon.ico`, umieść go w katalogu głównym swojej witryny. Zwykle nie musisz używać żadnych znaczników. Jednak nadal dobrą praktyką jest łączenie się z nią za pomocą poniższego przykładu. Dzisiaj, **format PNG jest zalecany** zamiast formatu `.ico` (wymiary: 32x32px).

```html
<!-- Standardowy favicon -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Zalecany format favicon -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

> * 🛠 [Favicon Generator](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> * 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Web App Meta:** ![Low][low_img] Metatagi Apple są obecne.

```html
<!-- Apple Touch Icon (przynajmniej 200x200px) -->
<link rel="apple-touch-icon" href="/custom-icon.png">

<!-- Aby uruchomić aplikację internetową na pełnym ekranie -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Status Bar Style (zobacz Supported Meta Tags poniżej dla dostępnych wartości) -->
<!-- Nie działa, chyba że masz poprzedni metatag -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```

> * 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
> * 📖 [Supported Meta Tags](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

- [ ] **Windows Tiles:** ![Low][low_img] Kafelki Windows są obecne i połączone.

```html
<!-- Kafelki Windows -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Minimalnie wymagany znacznik xml dla pliku `browserconfig.xml` wygląda następująco:

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

* [ ] **Canonical:** ![Medium][medium_img] Use `rel="canonical"` aby uniknąć powielania treści.

```html
<!-- Pomaga zapobiegać powielaniu problemów z treścią -->
<link rel="canonical" href="http://example.com/2017/09/a-new-article-to-read.html">
```

> * 📖 [Use canonical URLs - Search Console Help - Google Support](https://support.google.com/webmasters/answer/139066?hl=en)
> * 📖 [5 common mistakes with rel=canonical - Google Webmaster Blog](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### Tagi HTML

* [ ] **Atrybut języka:** ![High][high_img] Atrybut `lang` twojej witryny jest określony i związany z językiem bieżącej strony.

```html
<html lang="en">
```

* [ ] **Atrybut direction:** ![Medium][medium_img] Kierunek odczytu jest określony na znaczniku HTML (może być użyty na innym znaczniku HTML).

```html
<html dir="rtl">
```

> * 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

* [ ] **Alternatywny język:** ![Low][low_img] Tag języka twojej witryny jest określony i powiązany z językiem bieżącej strony.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es">
```

* [ ] **x-default:** ![Low][low_img] Tag języka twojej witryny dla międzynarodowych stron docelowych.

```html
<link rel="alternate" href="https://example.com/" hreflang="x-default" />
```

> * 📖 [x-default - Google](https://webmasters.googleblog.com/2013/04/x-default-hreflang-for-international-pages.html)


* [ ] **Komentarze warunkowe:** ![Low][low_img] W razie potrzeby komentarze warunkowe są dostępne dla IE.

> * 📖 [About conditional comments (Internet Explorer) - MSDN - Microsoft](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **Kanał RSS:** ![Low][low_img] Jeśli twój projekt jest blogiem lub zawiera artykuły, podano link RSS.

* [ ] **CSS Critical:** ![Medium][medium_img] Krytyczny CSS (lub "above the fold") zbiera wszystkie CSS użyte do renderowania widocznej części strony. Jest osadzony przed głównym wywołaniem CSS i między `<style> </style>` w jednym wierszu (zminimalizowanym).

> * 🛠 [Critical by Addy Osmani on GitHub](https://github.com/addyosmani/critical) automatyzuje to.

* [ ] **CSS order:** ![High][high_img] Wszystkie pliki CSS są ładowane przed plikami JavaScript w `<head>`. (Z wyjątkiem przypadku, gdy czasami pliki JS są ładowane asynchronicznie na górze strony).

### Social meta

Wizualizuj i generuj automatycznie nasze społecznościowe metatagi za pomocą [Meta Tags](https://metatags.io/)

***Facebook OG*** i ***Twitter Cards*** są, dla każdej strony, wysoko zalecane. Inne tagi mediów społecznościowych można rozważyć, jeśli kierujesz na nie określoną uwagę i chcesz zapewnić ich wyświetlanie.

* [ ] **Facebook Open Graph:** ![Low][low_img] Cały Facebook Open Graph (OG) jest przetestowany i niczego nie brakuje, ani nie ma niepoprawnych informacji. Obrazy muszą mieć co najmniej 600 x 315 pikseli, chociaż zaleca się 1200 x 630 pikseli.

> **Uwagi:** Używanie `og:image:width` oraz `og:image:height` określi wymiary obrazu dla crawlera, aby mógł natychmiast renderować obraz bez konieczności asynchronicznego pobierania i przetwarzania.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<!-- Kolejne tagi są opcjonalne, ale zalecane -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

> * 📖 [A Guide to Sharing for Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> * 📖 [Best Practices - Sharing](https://developers.facebook.com/docs/sharing/best-practices/)
> * 🛠 Test your page with the [Facebook OG testing](https://developers.facebook.com/tools/debug/)

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
> * 🛠 Test your page with the [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ powrót do góry](#spis-treści)**

---

## HTML

### Najlepsze praktyki

* [ ] **Elementy semantyczne HTML5:** ![High][high_img] Elementy semantyczne HTML5 są używane odpowiednio (header, section, footer, main...).

> * 📖 [HTML Reference](http://htmlreference.io/)

* [ ] **Strony błędów:** ![High][high_img] Istnieje błąd strony 404 i 5xx. Pamiętaj, że strony błędów 5xx muszą mieć zintegrowany CSS (brak zewnętrznego połączenia na bieżącym serwerze).

* [ ] **Noopener:** ![Medium][medium_img] W przypadku korzystania z zewnętrznych linków z `target="_blank"`, twój link powinien mieć atrybut `rel="noopener"` aby zapobiec przechwytywaniu kart. Jeśli potrzebujesz obsługi starszych wersji Firefoxa, użyj `rel="noopener noreferrer"`.

> * 📖 [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Wyczyść komentarze:** ![Low][low_img] Niepotrzebny kod należy usunąć przed wysłaniem strony do produkcji.

### Testowanie HTML

* [ ] **Zgodny z W3C:** ![High][high_img] Wszystkie strony należy przetestować za pomocą walidatora W3C, aby zidentyfikować możliwe problemy w kodzie HTML.

> * 🛠 [Walidator W3C](https://validator.w3.org/)

* [ ] **HTML Lint:** ![High][high_img] Korzystam z narzędzi, które pomagają mi analizować wszelkie problemy, które mogą wystąpić w kodzie HTML.

> * 🛠 [Dirty markup](https://www.10bestdesign.com/dirtymarkup/)

> * 🛠 [webhint](https://webhint.io/)

* [ ] **Link checker:** ![High][high_img] Na mojej stronie nie ma niedziałających linków, sprawdź, czy nie wystąpił błąd 404.

> * 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

* [ ] **Test Adblockerów:** ![Medium][medium_img] Twoja strona wyświetla poprawnie twoje treści z włączonymi adblockerami (możesz dostarczyć wiadomość zachęcającą ludzi do wyłączenia ich adblockera).

> * 📖 [Use AdBlocking in your Dev Environment](https://andreicioara.com/use-adblocking-in-your-dev-environment-48db500d9b86)


**[⬆ powrót do góry](#spis-treści)**

---

## Webfonts

> **Uwagi:** Używanie czcionek internetowych może powodować flashowanie niestylowanego tekstu / flashowanie niewidocznego tekstu - rozważ użycie czcionek zastępczych i/lub użycie programów ładujących czcionki internetowe do kontrolowania zachowania.
> * 📖 [Google Technical considerations about webfonts](https://developers.google.com/fonts/docs/technical_considerations)

* [ ] **Format webfont:** ![High][high_img] WOFF, WOFF2 oraz TTF są obsługiwane przez wszystkie nowoczesne przeglądarki.

> * 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - TrueType and OpenType font support](https://caniuse.com/#feat=ttf)
> * 📖 [Using @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Rozmiar Webfont:** ![High][high_img] Rozmiary webfont nie przekraczają 2 MB (wszystkie warianty w zestawie).

* [ ] **Webfont loader:** ![Low][low_img] Kontroluj zachowanie ładowania za pomocą modułu ładującego webfont

> * 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ powrót do góry](#spis-treści)**

---

## CSS

> **Uwagi:** Rzuć okiem na [Wytyczne CSS](https://cssguidelin.es/) oraz [Wytyczne Sass](https://sass-guidelin.es/) obserwowane przez większość programistów Front-End. Jeśli masz wątpliwości co do właściwości CSS, możesz odwiedzić [CSS Reference](http://cssreference.io/). Jest też krótki [Code Guide](http://codeguide.co/) dla spójności.

* [ ] **Responsive Web Design:** ![High][high_img] The website is using responsive web design.
* [ ] **CSS Print:** ![Medium][medium_img] A print stylesheet is provided and is correct on each page.
* [ ] **Preprocessors:** ![Low][low_img] Your project is using a CSS preprocessor (e.g [Sass](http://sass-lang.com/), [Less](http://lesscss.org/), [Stylus](http://stylus-lang.com/)).
* [ ] **Unique ID:** ![High][high_img] If IDs are used, they are unique to a page.
* [ ] **Reset CSS:** ![High][high_img] A CSS reset (reset, normalize or reboot) is used and up to date. *(If you are using a CSS Framework like Bootstrap or Foundation, a Normalize is already included into it.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS prefix:** ![Low][low_img] All classes (or id- used in JavaScript files) begin with **js-** and are not styled into the CSS files.

```html
<div id="js-slider" class="my-slider">
<!-- Or -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **embedded or inline CSS:** ![High][high_img] Avoid at all cost embedding CSS in `<style>` tags or using inline CSS: only use for valid reasons (e.g. background-image for slider, critical CSS).
* [ ] **Vendor prefixes:** ![High][high_img] CSS vendor prefixes are used and are generated accordingly with your browser support compatibility.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Performance

- [ ] **Concatenation:** ![High][high_img] CSS files are concatenated in a single file *(Not for HTTP/2)*.
- [ ] **Minification:** ![High][high_img] All CSS files are minified.
- [ ] **Non-blocking:** ![Medium][medium_img] CSS files need to be non-blocking to prevent the DOM from taking time to load.

> * 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
> * 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Unused CSS:** ![Low][low_img] Remove unused CSS.

> * 🛠 [UnCSS Online](https://uncss-online.com/)
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
> * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### CSS testing

* [ ] **Stylelint:** ![High][high_img] All CSS or SCSS files are without any errors.

> * 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> * 📖 [Sass guidelines](https://sass-guidelin.es/)

* [ ] **Responsive web design:** ![High][high_img] All pages were tested at the following breakpoints: 320px, 768px, 1024px (can be more / different according to your analytics).

* [ ] **CSS Validator:** ![Medium][medium_img] The CSS was tested and pertinent errors were corrected.

> * 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] **Desktop Browsers:** ![High][high_img] All pages were tested on all current desktop browsers (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Mobile Browsers:**  ![High][high_img] All pages were tested on all current mobile browsers (Native browser, Chrome, Safari...).
* [ ] **OS:**  ![High][high_img] All pages were tested on all current OS (Windows, Android, iOS, Mac...).

- [ ] **Design fidelity:** ![Low][low_img] Depending on the project and the quality of the creatives, you may be asked to be close to the design. You can use some tools to compare creatives with your code implementation and ensure consistency.

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Reading direction:** ![High][high_img] All pages need to be tested for LTR and RTL languages if they need to be supported.

> * 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ powrót do góry](#spis-treści)**

---

## Images

> **Uwagi:** For a complete understanding of image optimization, check the free ebook **[Essential Image Optimization](https://images.guide/)** from Addy Osmani.

### Best practices

* [ ] **Optimization:** ![High][high_img] All images are optimized to be rendered in the browser. WebP format could be used for critical pages (like Homepage).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 Use [ImageOptim](https://imageoptim.com/) to optimise your images for free.
> * 🛠 Use [KeyCDN Image Processing](https://www.keycdn.com/support/image-processing) for image optimization in real time.
> * 🛠 Use [Kraken.io](https://kraken.io/web-interface) awesome alternative for both png and jpg optimization. Up to 1mb per files on free plan.
> * 🛠 [TinyPNG](https://tinypng.com/) losslessly optimises png, apng (animated png) and jpg images. Free and paid version available.
> * 🛠 [ZorroSVG](http://quasimondo.com/ZorroSVG/) jpg-like compression for transparent images using svg masking.
> * 🛠 [SVGO](https://github.com/svg/svgo) a Nodejs-based tool for optimizing SVG vector graphics files.
> * 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) a web-based GUI version of SVGO for optimising your svgs online.


* [ ] **Picture/Srcset:** ![Medium][medium_img] You use picture/srcset to provide the most appropriate image for the current viewport of the user.

> * 📖 [How to Build Responsive Images with srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Low][low_img] You provide layout images 2x or 3x, support retina display.
* [ ] **Sprite:** ![Medium][medium_img] Small images are in a sprite file (in the case of icons, they can be in an SVG sprite image).
* [ ] **Width and Height:** ![High][high_img] Set `width` and `height` attributes on `<img>` if the final rendered image size is known (can be omitted for CSS sizing).
* [ ] **Alternative text:** ![High][high_img] All `<img>` have an alternative text which describes the image visually.

> * 📖 [Alt-texts: The Ultimate Guide](https://axesslab.com/alt-texts/)

* [ ] **Lazy loading:** ![Medium][medium_img] Images are lazyloaded (A noscript fallback is always provided).

**[⬆ powrót do góry](#spis-treści)**

---

## JavaScript

### Best practices

* [ ] **JavaScript Inline:** ![High][high_img] You don't have any JavaScript code inline (mixed with your HTML code).
* [ ] **Concatenation:** ![High][high_img] JavaScript files are concatenated.
* [ ] **Minification:** ![High][high_img] JavaScript files are minified (you can add the `.min` suffix).

> * 📖 [Minify Resources (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **JavaScript security:** ![High][high_img]

> * 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **`noscript` tag:** ![Medium][medium_img] Use `<noscript>` tag in the HTML body if a script type on the page is unsupported or if scripting is currently turned off in the browser. This will be helpful in client-side rendering heavy apps such as React.js, see [examples](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498).

```html
<noscript>
  You need to enable JavaScript to run this app.
</noscript>
```

* [ ] **Non-blocking:** ![Medium][medium_img] JavaScript files are loaded asynchronously using `async` or deferred using `defer` attribute.

> * 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Optimized and updated JS libraries:** ![Medium][medium_img] All JavaScript libraries used in your project are necessary (prefer Vanilla Javascript for simple functionalities), updated to their latest version and don't overwhelm your JavaScript with unnecessary methods.

> * 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
> * 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

* [ ] **Modernizr:** ![Low][low_img] If you need to target some specific features you can use a custom Modernizr to add classes in your `<html>` tag.

> * 🛠 [Customize your Modernizr](https://modernizr.com/download?setclasses)

### JavaScript testing

* [ ] **ESLint:** ![High][high_img] No errors are flagged by ESLint (based on your configuration or standards rules).

> * 📖 [ESLint - The pluggable linting utility for JavaScript and JSX](https://eslint.org/)

**[⬆ powrót do góry](#spis-treści)**

---

## Security

### Scan and check your web site

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory by Mozilla](https://observatory.mozilla.org/)

### Best practices

* [ ] **HTTPS:** ![High][high_img] HTTPS is used on every page and for all external content (plugins, images...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> * 🛠 [Free SSL Server Test](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] The HTTP header is set to 'Strict-Transport-Security'.

> * 🛠 [Check HSTS preload status and eligibility](https://hstspreload.org/)
> * 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
> * 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html)

* [ ] **Cross Site Request Forgery (CSRF):** ![High][high_img] You ensure that requests made to your server-side are legitimate and originate from your website / app to prevent CSRF attacks.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)

* [ ] **Cross Site Scripting (XSS):** ![High][high_img] Your page or website is free from XSS possible issues.

> * 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
> * 📖 [DOM based XSS Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html)

* [ ] **Content Type Options:** ![Medium][medium_img] Prevents Google Chrome and Internet Explorer from trying to mime-sniff the content-type of a response away from the one being declared by the server.

> * 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO):** ![Medium][medium_img] Protects your visitors against clickjacking attacks.

> * 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

* [ ] **Content Security Policy:** ![Medium][medium_img] Defines how content is loaded on your site and from where it is permitted to be loaded. Can also be used to protect against clickjacking attacks.

> * 📖 [Content Security Policy - An Introduction - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP Cheat Sheet - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
> * 📖 [Content Security Policy Reference](https://content-security-policy.com/)

**[⬆ powrót do góry](#spis-treści)**

---

## Performance

### Best practices

- [ ] **Goals to achieve:** ![Medium][medium_img] Your pages should reach these goals:
  - First Meaningful Paint under 1 second
  - Time To Interactive under 5 seconds for the "average" configuration (a $200 Android on a slow 3G network with 400ms RTT and 400kbps transfer speed) and under 2 seconds for repeat visits
  - Critical file size under 170Kb gzipped

> * 🛠 [Website Page Analysis](https://tools.pingdom.com)
> * 🛠 [WebPageTest](https://www.webpagetest.org/)
> * 📖 [Size Limit: Make the Web lighter](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

* [ ] **Minified HTML:** ![Medium][medium_img] Your HTML is minified.

* [ ] **Lazy loading:** ![Medium][medium_img] Images, scripts and CSS need to be lazy loaded to improve the response time of the current page (See details in their respective sections).

* [ ] **Cookie size:** ![Medium][medium_img] If you are using cookies be sure each cookie doesn't exceed 4096 bytes and your domain name doesn't have more than 20 cookies.

> * 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)

* [ ] **Third party components:** ![Medium][medium_img] Third party iframes or components relying on external JS (like sharing buttons) are replaced by static components when possible, thus limiting calls to external APIs and keeping your user's activity private.

> * 🛠 [Simple sharing buttons generator](https://simplesharingbuttons.com/)

### Preparing upcoming requests

> * 📖 [Explanation of the following techniques](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Low][low_img] DNS of third-party services that may be needed are resolved in advance during idle time using `dns-prefetch`.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnection:** ![Low][low_img] DNS lookup, TCP handshake and TLS negotiation with services that will be needed soon is done in advance during idle time using `preconnect`.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetching:** ![Low][low_img] Resources that will be needed soon (e.g. lazy loaded images) are requested in advance during idle time using `prefetch`.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Low][low_img] Resources needed in the current page (e.g. scripts placed at the end of `<body>`) in advance using `preload`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Difference between prefetch and preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Performance testing

* [ ] **Google PageSpeed:** ![High][high_img] All your pages were tested (not only the homepage) and have a score of at least 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Test your mobile speed with Google](https://testmysite.withgoogle.com)
> * 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Website speed and performance optimization](https://gtmetrix.com/)
> * 🛠 [Speedrank - Improve the performance of your website](https://speedrank.app/)

**[⬆ powrót do góry](#spis-treści)**

---

## Accessibility

> **Uwagi:** You can watch the playlist [A11ycasts with Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Best practices

- [ ] **Progressive enhancement:** ![Medium][medium_img] Major functionality like main navigation and search should work without JavaScript enabled.

> * 📖 [Enable / Disable JavaScript in Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Color contrast:** ![Medium][medium_img] Color contrast should at least pass WCAG AA (AAA for mobile).

> * 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Headings

* [ ] **H1:** ![High][high_img] All pages have an H1 which is not the title of the website.
* [ ] **Headings:** ![High][high_img] Headings should be used properly and in the right order (H1 to H6).

> * 📹 [Why headings and landmarks are so important -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

### Semantics

- [ ] **Specific HTML5 input types are used:** ![Medium][medium_img] This is especially important for mobile devices that show customized keypads and widgets for different types.

> * 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Form

* [ ] **Label:** ![High][high_img] A label is associated with each input form element. In case a label can't be displayed, use `aria-label` instead.

> * 📖 [Using the aria-label attribute - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Accessibility testing

* [ ] **Accessibility standards testing:** ![High][high_img] Use the WAVE tool to test if your page respects the accessibility standards.

> * 🛠 [Wave testing](http://wave.webaim.org/)

* [ ] **Keyboard navigation:** ![High][high_img] Test your website using only your keyboard in a previsible order. All interactive elements are reachable and usable.
* [ ] **Screen-reader:** ![Medium][medium_img] All pages were tested in a screen-reader (VoiceOver, ChromeVox, NVDA or Lynx).
* [ ] **Focus style:** ![High][high_img] If the focus is disabled, it is replaced by visible state in CSS.

> * 📹 [Managing Focus - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ powrót do góry](#spis-treści)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics is installed and correctly configured.

> * 🛠 [Google Analytics](https://analytics.google.com/analytics/web/)
> * 🛠 [GA Checker (and others)](http://www.gachecker.com/)

* [ ] **Headings logic:** ![Medium][medium_img] Heading text helps to understand the content in the current page.

> * 🛠 [Tota11y, tab Headings](http://khan.github.io/tota11y/#Try-it)

* [ ] **sitemap.xml:** ![High][high_img] A sitemap.xml exists and was submitted to Google Search Console (previously Google Webmaster Tools).

> * 🛠 [Sitemap generator](https://websiteseochecker.com/html-sitemap-generator/)

* [ ] **robots.txt:** ![High][high_img] The robots.txt is not blocking webpages.

> * 📖 [The robots.txt file](https://varvy.com/robottxt.html)
> * 🛠 Test your robots.txt with [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Structured Data:** ![High][high_img] Pages using structured data are tested and are without errors. Structured data helps crawlers understand the content in the current page.

> * 📖 [Introduction to Structured Data - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 📖 [RDFa - Linked Data in HTML](https://rdfa.info/)
> * 📖 [JSON-LD](https://json-ld.org/)
> * 📖 [Microdata](https://www.w3.org/TR/microdata/)
> * 🛠 Test your page with the [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Complete list of vocabularies that can be used as structured data. [Schema.org Full Hierarchy](http://schema.org/docs/full.html)

* [ ] **Sitemap HTML:** ![Medium][medium_img] An HTML sitemap is provided and is accessible via a link in the footer of your website.

> * 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)

* [ ] **Pagination link tags:** ![Medium][medium_img] Provide `rel="prev"` and `rel="next"` to indicate paginated content.

> * 🛠 [Pagination (rel="prev/next") Testing Tool](https://technicalseo.com/seo-tools/rel-prev-next/)

> * 📖 [Pagination guidelines - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Example: Pagination link tags for page 2 of a paginated list -->
<link rel="prev" href="https://example.com/?page=1">
<link rel="next" href="https://example.com/?page=3">
```

**[⬆ powrót do góry](#spis-treści)**

---

## Translations

The Front-End Checklist is also available in other languages. Thanks for all translators and their awesome work!

* 🇯🇵 Japanese: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
* 🇪🇸 Spanish: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
* 🇨🇳 Chinese: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
* 🇰🇷 Korean: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
* 🇧🇷 Portuguese: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
* 🇻🇳 Vietnamese: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
* 🇹🇼 Traditional Chinese: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)
* 🇫🇷 French: [ynizon/Front-End-Checklist](https://github.com/ynizon/Front-End-Checklist)
* 🇷🇺 Russian: [ungear/Front-End-Checklist](https://github.com/ungear/Front-End-Checklist)
* 🇹🇷 Turkish: [eraycetinay/Front-End-Checklist](https://github.com/eraycetinay/Front-End-Checklist)
* 🇩🇪 German: [xfuture603/Front-End-Checklist](https://github.com/xFuture603/Front-End-Checklist)

---

## Front-End Checklist Badge

If you want to show you are following the rules of the Front-End Checklist, put this badge on your README file!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ powrót do góry](#spis-treści)**

---

## Contributing

**Open an issue or a pull request to suggest changes or additions.**

### Guide

The **Front-End Checklist** repository consists of two branches:

#### 1. `master`

This branch consists of the `README.md` file that is automatically reflected on the [Front-End Checklist](https://frontendchecklist.io) website.

#### 2. `develop`

This branch will be used to make some significant changes to the structure, content if needed. It is preferable to use the master branch to fix small errors or add a new item.

## Support

If you have any question or suggestion, don't hesitate to use Gitter or Twitter:

* [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Author

**[David Dias](https://github.com/thedaviddias)**

## Contributors

This project exists thanks to all the people who contribute. [[Contribute]](.github/CONTRIBUTING.md).
<a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors"><img src="https://opencollective.com/front-end-checklist/contributors.svg?width=890" /></a>


## Backers

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/front-end-checklist#backer)]

<a href="https://opencollective.com/front-end-checklist#backers" target="_blank"><img src="https://opencollective.com/front-end-checklist/backers.svg?width=890"></a>


## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](https://opencollective.com/front-end-checklist#sponsor)]

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

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ powrót do góry](#spis-treści)**

[low_img]: data/images/priority/low.svg
[medium_img]: data/images/priority/medium.svg
[high_img]: data/images/priority/high.svg
