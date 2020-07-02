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
5. **[Obrazy](#obrazy)**
6. **[JavaScript](#javascript)**
7. **[Bezpieczeństwo](#bezpieczeństwo)**
8. **[Wydajność](#wydajność-1)**
9. **[Dostępność](#dostępność)**
10. **[SEO](#seo)**
11. **[Tłumaczenia](#tłumaczenia)**

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

* [ ] **Responsive Web Design:** ![High][high_img] Strona korzysta z responsywnego projektowania stron internetowych.
* [ ] **CSS Print:** ![Medium][medium_img] Arkusz stylów wydruku jest dostarczony i jest poprawny na każdej stronie.
* [ ] **Preprocessors:** ![Low][low_img] Twój projekt korzysta z preprocesora CSS (np. [Sass](http://sass-lang.com/), [Less](http://lesscss.org/), [Stylus](http://stylus-lang.com/)).
* [ ] **Unique ID:** ![High][high_img] Jeśli używane są identyfikatory, są one unikalne dla strony.
* [ ] **Reset CSS:** ![High][high_img] Reset CSS (reset, normalizacja lub restart) jest używany i aktualny. *(Jeśli używasz frameworka CSS, takiego jak Bootstrap lub Foundation, normalizacja jest już w nim zawarta.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS prefix:** ![Low][low_img] Wszystkie klasy (lub id- używane w plikach JavaScript) zaczynają się od **js-** i nie są stylizowane na pliki CSS.

```html
<div id="js-slider" class="my-slider">
<!-- Lub -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **embedded or inline CSS:** ![High][high_img] Unikaj za wszelką cenę osadzania CSS w tagach `<style>` lub używania wbudowanego CSS: używaj tylko z ważnych powodów (np. background-image dla slider, critical CSS).
* [ ] **Vendor prefixes:** ![High][high_img] Prefiksy dostawców CSS są używane i są generowane zgodnie ze zgodnością obsługi przeglądarki.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Wydajność

- [ ] **Konkatenacja:** ![High][high_img] Pliki CSS są łączone w jednym pliku *(Nie dla HTTP/2)*.
- [ ] **Minifikacja:** ![High][high_img] Wszystkie pliki CSS są minifikowane.
- [ ] **Non-blocking:** ![Medium][medium_img] Pliki CSS muszą być nieblokujące, aby DOM nie zajmował dużo czasu podczas ładowania.

> * 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
> * 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Nieużywany CSS:** ![Low][low_img] Usuń nieużywany CSS.

> * 🛠 [UnCSS Online](https://uncss-online.com/)
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
> * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### Testowanie CSS

* [ ] **Stylelint:** ![High][high_img] Wszystkie pliki CSS lub SCSS są bez żadnych błędów.

> * 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> * 📖 [Sass guidelines](https://sass-guidelin.es/)

* [ ] **Responsive web design:** ![High][high_img] Wszystkie strony zostały przetestowane w następujących breakpointach: 320px, 768px, 1024px (mogą być bardziej / różne w zależności od danych analitycznych).

* [ ] **Walidator CSS:** ![Medium][medium_img] CSS został przetestowany i odpowiednie błędy zostały poprawione.

> * 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] **Przeglądarki stacjonarne:** ![High][high_img] Wszystkie strony zostały przetestowane we wszystkich obecnych przeglądarkach na komputery (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Przeglądarki mobilne:**  ![High][high_img] Wszystkie strony zostały przetestowane we wszystkich obecnych przeglądarkach mobilnych (Native browser, Chrome, Safari...).
* [ ] **OS:**  ![High][high_img] Wszystkie strony zostały przetestowane na wszystkich obecnych systemach operacyjnych (Windows, Android, iOS, Mac...).

- [ ] **Dokładność projektu:** ![Low][low_img] W zależności od projektu i jakości creatives możesz zostać poproszony o zbliżenie się do projektowania. Możesz użyć niektórych narzędzi do porównania creatives z implementacją kodu i zapewnienia spójności.

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Kierunek czytania:** ![High][high_img] Wszystkie strony muszą zostać przetestowane pod kątem języków LTR i RTL, jeśli wymagają obsługi.

> * 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ powrót do góry](#spis-treści)**

---

## Obrazy

> **Uwagi:** Aby w pełni zrozumieć optymalizację obrazu, sprawdź bezpłatny ebook **[Essential Image Optimization](https://images.guide/)** od Addy Osmani.

### Najlepsze praktyki

* [ ] **Optymalizacja:** ![High][high_img] Wszystkie obrazy są zoptymalizowane do wyświetlania w przeglądarce. Format stron internetowych można zastosować do stron krytycznych (takich jak strona główna).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 Użyj [ImageOptim](https://imageoptim.com/) aby zoptymalizować swoje zdjęcia za darmo.
> * 🛠 Użyj [KeyCDN Image Processing](https://www.keycdn.com/support/image-processing) do optymalizacji obrazu w czasie rzeczywistym.
> * 🛠 Użyj [Kraken.io](https://kraken.io/web-interface), świetna alternatywa zarówno dla optymalizacji png, jak i jpg. Do 1 MB na pliki w abonamencie darmowym.
> * 🛠 [TinyPNG](https://tinypng.com/) losslessly optymalizuje obrazy png, apng (animowane png) i jpg. Dostępna wersja bezpłatna i płatna.
> * 🛠 [ZorroSVG](http://quasimondo.com/ZorroSVG/) jpg-like kompresja dla przezroczystych obrazów przy użyciu maskowania svg.
> * 🛠 [SVGO](https://github.com/svg/svgo) oparte na Nodejs narzędzie do optymalizacji plików grafiki wektorowej SVG.
> * 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) internetowa wersja GUI SVGO do optymalizacji plików svg online.


* [ ] **Picture/Srcset:** ![Medium][medium_img] Używasz picture/srcset, aby zapewnić najbardziej odpowiedni obraz dla bieżącego viewportu użytkownika.

> * 📖 [How to Build Responsive Images with srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Low][low_img] Zapewniasz obrazy układu 2x lub 3x, obsługuje wyświetlanie retina.
* [ ] **Sprite:** ![Medium][medium_img] Małe obrazy znajdują się w pliku ikonki (w przypadku ikon mogą być w obrazku ikonki SVG).
* [ ] **Szerokość i wysokość:** ![High][high_img] Ustaw atrybuty `width` i `height` na `<img>` jeśli znany jest ostateczny rozmiar renderowanego obrazu (można go pominąć przy określaniu rozmiaru CSS).
* [ ] **Alternatywny tekst:** ![High][high_img] Wszystkie `<img>` mają alternatywny tekst, który opisuje obraz wizualnie.

> * 📖 [Alt-texts: The Ultimate Guide](https://axesslab.com/alt-texts/)

* [ ] **Lazy loading:** ![Medium][medium_img] Obrazy są ładowane lazyloaded (zawsze dostępna jest rezerwowa kopia zapasowa).

**[⬆ powrót do góry](#spis-treści)**

---

## JavaScript

### Najlepsze praktyki

* [ ] **JavaScript Inline:** ![High][high_img] Nie masz kodu inline JavaScript (zmieszanego z kodem HTML).
* [ ] **Konkatenacja:** ![High][high_img] Pliki JavaScript są łączone.
* [ ] **Minifikacja:** ![High][high_img] Pliki JavaScript są minifikowane (możesz dodać sufiks `.min`).

> * 📖 [Minify Resources (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **Bezpieczeństwo JavaScript:** ![High][high_img]

> * 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **`noscript` tag:** ![Medium][medium_img] Uzyj tagu `<noscript>` w body HTML, jeśli typ skryptu na stronie nie jest obsługiwany lub skrypty są obecnie wyłączone w przeglądarce. Będzie to pomocne w renderowaniu ciężkich aplikacji, takich jak React.js, po stronie klienta, patrz [przykłady](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498).

```html
<noscript>
  Aby uruchomić tę aplikację, musisz włączyć JavaScript.
</noscript>
```

* [ ] **Non-blocking:** ![Medium][medium_img] Pliki JavaScript są ładowane asynchronicznie za pomocą `async` lub odroczone za pomocą atrybutu `defer`.

> * 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Zoptymalizowane i zaktualizowane biblioteki JS:** ![Medium][medium_img] Wszystkie biblioteki JavaScript używane w twoim projekcie są niezbędne (wolą Vanilla Javascript dla prostych funkcji), zaktualizowane do najnowszej wersji i nie przytłaczają JavaScript niepotrzebnymi metodami.

> * 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
> * 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

* [ ] **Modernizr:** ![Low][low_img] Jeśli musisz kierować określone funkcje, możesz użyć niestandardowego Modernizr, aby dodać klasy do tagu `<html>`.

> * 🛠 [Customize your Modernizr](https://modernizr.com/download?setclasses)

### Testowanie JavaScript

* [ ] **ESLint:** ![High][high_img] Żadne błędy nie są oznaczane przez ESLint (w oparciu o zasady konfiguracji lub normy).

> * 📖 [ESLint - The pluggable linting utility for JavaScript and JSX](https://eslint.org/)

**[⬆ powrót do góry](#spis-treści)**

---

## Bezpieczeństwo

### Zeskanuj i sprawdź swoją stronę internetową

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory by Mozilla](https://observatory.mozilla.org/)

### Najlepsze praktyki

* [ ] **HTTPS:** ![High][high_img] HTTPS jest używany na każdej stronie i dla wszystkich treści zewnętrznych (wtyczek, obrazów...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> * 🛠 [Free SSL Server Test](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] HTTP header jest ustawiony na 'Strict-Transport-Security'.

> * 🛠 [Check HSTS preload status and eligibility](https://hstspreload.org/)
> * 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
> * 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html)

* [ ] **Cross Site Request Forgery (CSRF):** ![High][high_img] Zapewniasz, że żądania wysyłane na twoją stronę są prawidłowe i pochodzą z twojej witryny / aplikacji, aby zapobiec atakom CSRF.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)

* [ ] **Cross Site Scripting (XSS):** ![High][high_img] Twoja strona lub witryna jest wolna od możliwych problemów XSS.

> * 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
> * 📖 [DOM based XSS Prevention Cheat Sheet  - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html)

* [ ] **Content Type Options:** ![Medium][medium_img] Zapobiega próbom mime-sniff przez Google Chrome i Internet Explorer typu zawartości odpowiedzi od zadeklarowanej przez serwer.

> * 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO):** ![Medium][medium_img] Chroni odwiedzających przed atakami typu clickjacking.

> * 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

* [ ] **Content Security Policy:** ![Medium][medium_img] Określa, w jaki sposób treść jest ładowana w twojej witrynie i skąd może być ładowana. Może być również stosowany do ochrony przed atakami typu clickjacking.

> * 📖 [Content Security Policy - An Introduction - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP Cheat Sheet - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP Cheat Sheet - OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
> * 📖 [Content Security Policy Reference](https://content-security-policy.com/)

**[⬆ powrót do góry](#spis-treści)**

---

## Wydajność

### Najlepsze praktyki

- [ ] **Cele do osiągnięcia:** ![Medium][medium_img] Twoje strony powinny osiągnąć następujące cele:
  - First Meaningful Paint poniżej 1 sekundy
  - Time To Interactive poniżej 5 sekund dla konfiguracji "średniej" (Android za 200 USD w wolnej sieci 3G z RTT 400 ms i prędkością transferu 400 kb / s) i poniżej 2 sekund na kolejne wizyty
  - Krytyczny rozmiar pliku poniżej 170Kb gzipped

> * 🛠 [Website Page Analysis](https://tools.pingdom.com)
> * 🛠 [WebPageTest](https://www.webpagetest.org/)
> * 📖 [Size Limit: Make the Web lighter](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

* [ ] **Zminifikowany HTML:** ![Medium][medium_img] Twój HTML jest zminifikowany.

* [ ] **Lazy loading:** ![Medium][medium_img] Obrazy, skrypty i CSS muszą być ładowane z opóźnieniem, aby skrócić czas odpowiedzi bieżącej strony (zobacz szczegóły w odpowiednich sekcjach).

* [ ] **Rozmiar cookie:** ![Medium][medium_img] Jeśli używasz plików cookie, upewnij się, że każdy plik cookie nie przekracza 4096 bajtów, a nazwa domeny nie zawiera więcej niż 20 plików cookie.

> * 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)

* [ ] **Komponenty stron trzecich:** ![Medium][medium_img] Elementy iframe lub komponenty innych firm polegające na zewnętrznym JS (takie jak przyciski udostępniania) są w miarę możliwości zastępowane przez komponenty statyczne, ograniczając w ten sposób połączenia z zewnętrznymi interfejsami API i utrzymując prywatność użytkownika.

> * 🛠 [Simple sharing buttons generator](https://simplesharingbuttons.com/)

### Przygotowywanie nadchodzących żądań

> * 📖 [Explanation of the following techniques](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Low][low_img] DNS usług stron trzecich, które mogą być potrzebne, są rozwiązywane z góry w czasie bezczynności przy użyciu `dns-prefetch`.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnection:** ![Low][low_img] Wyszukiwanie DNS, uzgadnianie TCP i negocjacje TLS z usługami, które będą wkrótce potrzebne, są wykonywane z wyprzedzeniem w czasie bezczynności przy użyciu `preconnect`.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetching:** ![Low][low_img] Zasoby, które będą wkrótce potrzebne (np. leniwie załadowane obrazy) są wymagane z góry w czasie bezczynności przy użyciu `prefetch`.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Low][low_img] Zasoby potrzebne na bieżącej stronie (np. skrypty umieszczone na końcu `<body>`) za pomocą `preload`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Difference between prefetch and preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Test wydajności

* [ ] **Google PageSpeed:** ![High][high_img] Wszystkie twoje strony zostały przetestowane (nie tylko strona główna) i uzyskały wynik co najmniej 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Test your mobile speed with Google](https://testmysite.withgoogle.com)
> * 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Website speed and performance optimization](https://gtmetrix.com/)
> * 🛠 [Speedrank - Improve the performance of your website](https://speedrank.app/)

**[⬆ powrót do góry](#spis-treści)**

---

## Dostępność

> **Uwagi:** Możesz obejrzeć listę odtwarzania [A11ycasts z Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Najlepsze praktyki

- [ ] **Progresywne ulepszanie:** ![Medium][medium_img] Główne funkcje, takie jak główna nawigacja i wyszukiwanie, powinny działać bez włączonej obsługi JavaScript.

> * 📖 [Enable / Disable JavaScript in Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Kontrast kolorów:** ![Medium][medium_img] Kontrast kolorów powinien co najmniej przejść WCAG AA (AAA dla urządzeń mobilnych).

> * 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Nagłówki

* [ ] **H1:** ![High][high_img] Wszystkie strony mają H1, który nie jest tytułem strony internetowej.
* [ ] **Headings:** ![High][high_img] Nagłówki należy stosować prawidłowo i we właściwej kolejności (od H1 do H6).

> * 📹 [Why headings and landmarks are so important -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

### Semantyka

- [ ] **Używane są określone typy danych HTML5:** ![Medium][medium_img] Jest to szczególnie ważne w przypadku urządzeń mobilnych, które wyświetlają niestandardowe klawiatury i widżety dla różnych typów.

> * 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Formularz

* [ ] **Etykieta:** ![High][high_img] Etykieta jest powiązana z każdym elementem formularza wejściowego. Jeśli etykieta nie może zostać wyświetlona, użyj zamiast tego `aria-label`.

> * 📖 [Using the aria-label attribute - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Testy dostępności

* [ ] **Testowanie standardów dostępności:** ![High][high_img] Użyj narzędzia WAVE, aby sprawdzić, czy strona spełnia standardy dostępności.

> * 🛠 [Wave testing](http://wave.webaim.org/)

* [ ] **Nawigacja za pomocą klawiatury:** ![High][high_img] Przetestuj swoją stronę internetową, używając tylko klawiatury w przewidywalnej kolejności. Wszystkie elementy interaktywne są osiągalne i użyteczne.
* [ ] **Screen-reader:** ![Medium][medium_img] Wszystkie strony zostały przetestowane w czytniku ekranu (VoiceOver, ChromeVox, NVDA lub Lynx).
* [ ] **Focus style:** ![High][high_img] Jeśli fokus jest wyłączony, jest zastępowany widocznym stanem w CSS.

> * 📹 [Managing Focus - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ powrót do góry](#spis-treści)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics jest zainstalowany i poprawnie skonfigurowany.

> * 🛠 [Google Analytics](https://analytics.google.com/analytics/web/)
> * 🛠 [GA Checker (and others)](http://www.gachecker.com/)

* [ ] **Logika nagłówków:** ![Medium][medium_img] Tekst nagłówka pomaga zrozumieć treść na bieżącej stronie.

> * 🛠 [Tota11y, tab Headings](http://khan.github.io/tota11y/#Try-it)

* [ ] **sitemap.xml:** ![High][high_img] sitemap.xml istnieje i został przesłany do Google Search Console (wcześniej Google Webmaster Tools).

> * 🛠 [Sitemap generator](https://websiteseochecker.com/html-sitemap-generator/)

* [ ] **robots.txt:** ![High][high_img] robots.txt nie blokuje stron internetowych.

> * 📖 [The robots.txt file](https://varvy.com/robottxt.html)
> * 🛠 Test your robots.txt with [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Dane strukturalne:** ![High][high_img] Strony używające danych strukturalnych są testowane i nie zawierają błędów. Dane strukturalne pomagają crawlerom indeksującym zrozumieć treść na bieżącej stronie.

> * 📖 [Introduction to Structured Data - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 📖 [RDFa - Linked Data in HTML](https://rdfa.info/)
> * 📖 [JSON-LD](https://json-ld.org/)
> * 📖 [Microdata](https://www.w3.org/TR/microdata/)
> * 🛠 Przetestuj swoją stronę za pomocą [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Pełna lista słowników, które można wykorzystać jako dane ustrukturyzowane. [Schema.org Full Hierarchy](http://schema.org/docs/full.html)

* [ ] **Mapa strony HTML:** ![Medium][medium_img] Mapa strony HTML jest dostarczona i jest dostępna poprzez link w stopce witryny.

> * 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)

* [ ] **Pagination link tags:** ![Medium][medium_img] Zapewnij `rel="prev"` i `rel="next"` w celu wskazania stronicowanych treści.

> * 🛠 [Pagination (rel="prev/next") Testing Tool](https://technicalseo.com/seo-tools/rel-prev-next/)

> * 📖 [Pagination guidelines - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Przykład: Pagination link tags for page 2 of a paginated list -->
<link rel="prev" href="https://example.com/?page=1">
<link rel="next" href="https://example.com/?page=3">
```

**[⬆ powrót do góry](#spis-treści)**

---

## Tłumaczenia

Lista kontrolna frontend jest również dostępna w innych językach. Dziękujemy wszystkim tłumaczom za ich wspaniałą pracę!

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
* 🇵🇱 Polish: [mbiesiad/Front-End-Checklist](https://github.com/mbiesiad/Front-End-Checklist)

---

## Front-End Checklist Badge

Jeśli chcesz pokazać, że przestrzegasz zasad Listy kontrolnej frontend, umieść tę odznakę w pliku README!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ powrót do góry](#spis-treści)**

---

## Współtworzenie

**Otwórz issue lub PR, aby zasugerować zmiany lub uzupełnienia.**

### Przewodnik

Repo **Front-End Checklist** składa się z dwóch gałęzi:

#### 1. `master`

Ta gałąź składa się z pliku `README.md` który jest automatycznie odzwierciedlany na stronie [Front-End Checklist](https://frontendchecklist.io).

#### 2. `develop`

Ta gałąź zostanie wykorzystana do wprowadzenia istotnych zmian w strukturze, w razie potrzeby zawartości. Lepiej jest użyć gałęzi głównej, aby naprawić małe błędy lub dodać nowy element.

## Wsparcie

Jeśli masz jakieś pytania lub sugestie, nie wahaj się skorzystać z Gittera lub Twittera:

* [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Autor

**[David Dias](https://github.com/thedaviddias)**

## Współtwórcy

Ten projekt istnieje dzięki wszystkim ludziom, którzy wnoszą swój wkład. [[Contribute]](.github/CONTRIBUTING.md).
<a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors"><img src="https://opencollective.com/front-end-checklist/contributors.svg?width=890" /></a>


## Backers

Dziękuję wszystkim naszym backers! 🙏 [[Become a backer](https://opencollective.com/front-end-checklist#backer)]

<a href="https://opencollective.com/front-end-checklist#backers" target="_blank"><img src="https://opencollective.com/front-end-checklist/backers.svg?width=890"></a>


## Sponsorzy

Wesprzyj ten projekt, zostając sponsorem. Twoje logo pojawi się tutaj wraz z linkiem do twojej witryny. [[Zostań sponsorem](https://opencollective.com/front-end-checklist#sponsor)]

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

## Licencja

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ powrót do góry](#spis-treści)**

[low_img]: data/images/priority/low.svg
[medium_img]: data/images/priority/medium.svg
[high_img]: data/images/priority/high.svg
