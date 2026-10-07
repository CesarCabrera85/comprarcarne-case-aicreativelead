# INSTRUCTIONS FOR ABACUS.AI
# COMPRARCARNE.ES BUSINESS CASE ON AICREATIVELEAD.COM

Version 1.0 · prepared 08/10/2026 · owner: César Cabrera Boggio (AI Creative Lead)

> **Scope in one line:** create `/work/comprarcarne` and `/es/work/comprarcarne` with the SAME components and visual
> system as `/work/zayra` and `/work/arturos`, and connect them from `/work`, `/es/work`, the Home, the Arturos and
> Zayra cases, two Insights articles, the sitemap and `llms.txt`. Preview URL first; production only after César approves.
>
> **Prerequisite:** this package comes AFTER the Arturos package
> (https://github.com/CesarCabrera85/arturos-case-aicreativelead). If Arturos is not implemented yet, implement it first,
> then this one. Arturos stays the CASE OF THE MONTH.
>
> **Always both languages.** Every change exists in English AND Spanish. Never ship one language without the other.
>
> **The film must be seen.** A silent loop plays in the case hero and the /work card from the first second; the full
> film with sound is in section 07 of the case.

---

## 1. What the project is

**comprarcarne.es — The box is here / Ha llegado la cajita** is a TV commercial for **comprarcarne.es**, an online
butcher's from Málaga that delivers fresh meat, vacuum-packed and chilled, across mainland Spain. It is **real client
work**: AI Creative Lead has led the brand's creative direction since its launch in 2024. The film is already on the
site (`/media/comprar-carne-spot-2026.mp4`, row "COMPRAR CARNE SPOT 2026" in the schedule).

Story: Mum and the kids order "la cajita" on the phone → wait → doorbell → the brand's real box arrives → vacuum-packed
chuletón → pan → everyone at the table → comprarcarne.es end card. 16 shots, 21 s (end card included).

**Hard rules (non-negotiable)**

1. **Real client, real facts.** Present it as client work, never as a concept. Use only the figures in `metrics.json`.
   **Never publish client business data** (revenue, number of customers, growth, orders), audience, views or sales.
2. **No prices and no delivery-time promises** on these pages. No AI tool or model names.
3. **The creative brief / generation prompt of the spot is confidential.** It is not in this repository and must never be
   published or paraphrased beyond the copy in `copy.json`.
4. **Do not add claims** that are not in `copy.json` (e.g. number of children in every shot, "no music", "always well done").
5. **Same design as Zayra and Arturos.** Case accent = comprarcarne.es magenta. Brand colour is `#C30056`; on the page it is
   `#F0006A` (same hue, lifted for AA text contrast on black, button text black). ON AIR dot, red "LEAD" and `.btn-red`
   (`#FF3B30`) stay as they are.
6. **Children:** every character is AI-generated; the page says so in the closing note and the FAQ. Keep it.

---

## 2. Files in this repository

```
public/images/cases/comprarcarne/      76 files, final and web-optimized — copy as-is into the site's public/
  comprarcarne-hero-poster.avif|.webp|.jpg + -960.webp   hero (LCP), loop/film poster, /work card, Home strip
  comprarcarne-og-1200x630.jpg                            Open Graph + Twitter
  comprarcarne-shot-map.jpg|.webp + -960.webp             section 06 (the 16 shots on one sheet)
  comprarcarne-shot-01 … 16 (+ 06b) .jpg|.webp + -400/-800.webp   all shots (1600x900)
public/media/cases/comprarcarne/
  comprarcarne-hero-loop-720p.mp4      silent loop, 6.3 s, 1280x720, H.264, no audio, fast-start, 1.3 MB
                                       (the box at the door → opening → vacuum pack → pan → "wow" → platter → first bites)
instructions/
  ABACUS_COMPRARCARNE_INTEGRATION.md   this document (wins over anything else if they differ)
  comprarcarne-case.css                the ONLY new CSS (scoped .case-comprarcarne + small blocks for /work and Home)
  copy.json                            every string EN/ES + shot captions + palette + links
  metrics.json                         the only figures allowed
  seo_meta.json                        title, description, canonical, hreflang, OG, Twitter — EN and ES
  schema_work_comprarcarne_en.jsonld   JSON-LD EN (replace PUBLISH_DATE_ISO8601)
  schema_work_comprarcarne_es.jsonld   JSON-LD ES (replace PUBLISH_DATE_ISO8601)
  alt_texts.csv                        alt text EN/ES for every image
  snippets/                            case <main> EN/ES, /work featured cases EN/ES (4 cards), Home featured case EN/ES,
                                       schedule-row link, related links, Insights sentences, sitemap entries, llms.txt line
previews/                              serve the repo with any static server: case EN/ES, /work block EN/ES, Home block EN/ES.
                                       _site/ = copies of the live CSS + arturos-case.css (already on the site after Arturos).
```

Video:
- **Film with sound (player, section 07):** the master already on the site, `/media/comprar-carne-spot-2026.mp4`
  (1280x720, H.264/AAC, 21.3 s). Do not re-upload it.
- **Silent loop (case hero, /work card):** `/media/cases/comprarcarne/comprarcarne-hero-loop-720p.mp4` from this repository.

---

## 3. The case page — `/work/comprarcarne` and `/es/work/comprarcarne`

Same route pattern and inner-page shell as `/work/zayra` and `/work/arturos`. The content of `<main>` is
`snippets/case_main_en.html` / `case_main_es.html` (final site paths, alt texts and copy in place).
Wrapper: `<div class="zayra-scope case-comprarcarne">` + `comprarcarne-case.css` (load it only where it is used).

| # | id | h2 (EN / ES) | .idx (EN / ES) | Component |
|---|---|---|---|---|
| — | hero | **H1** `COMPRARCARNE.ES` + *The box is here / Ha llegado la cajita* | `CASE 03 · AI TV COMMERCIAL · CLIENT · 2026` / `CASO 03 · SPOT DE TV CON IA · CLIENTE · 2026` + `00:00 → 00:21` | `.hero` — poster + silent loop |
| — | chainbar | Brief · Story · Cast · Product · Shot by shot · Film · Client · Production | Brief · Historia · Reparto · Producto · Plano a plano · Film · Cliente · Producción | `.chainbar` |
| — | facts | Client · Type · Delivered · Client since | Cliente · Tipo · Entregado · Cliente desde | `.facts` |
| 01 | project | The project / El proyecto | 01 / PROJECT · PROYECTO | `.two` + end-card image |
| 02 | challenge | The challenge / El reto | 02 / PROBLEM · PROBLEMA | `.big` + `.ticks` |
| 03 | direction | Creative direction / Dirección creativa | 03 / DECISION · DECISIÓN | `.chapters.c6` (6 moments) + `.palette` (6) + `.rules` (production rules) |
| 04 | cast | A family the colour of the house. / Una familia del color de la casa. | 04 / CAST · REPARTO | `.idgrid` (4) |
| 05 | product | The box is the hero. / La caja es la protagonista. | 05 / PRODUCT · PRODUCTO | `.idgrid` (4) + `.frames.f2` (food) |
| 06 | shots | 16 shots, one countdown. / 16 planos, una cuenta atrás. | 06 / SHOT BY SHOT · PLANO A PLANO | `.board.dark` (shot map) + `.frames` (16 captions) |
| 07 | film | The film / El film | 07 / FILM | `.films.solo` |
| 08 | client | A client, not a test. / Un cliente, no una prueba. | 08 / CLIENT · CLIENTE | client card (`.press` style) + link to comprarcarne.es |
| 09 | result | The production / La producción | 09 / RESULT · RESULTADO | `.nums.n3` (6 figures) |
| 10 | proves | What this proves for your brand. / Qué demuestra para tu marca. | 10 / FOR YOUR BRAND · PARA TU MARCA | `.brand3` |
| 11 | faq | Questions about AI commercials for brands / Preguntas sobre spots con IA para marcas | 11 / FAQ · PREGUNTAS | `.faq` |
| — | book | disclosure note (AI-generated characters, no real children filmed) | | `.note` |
| — | closing | Send us the brief. / Envíanos el brief. | | existing `section.closing` + related: Arturos case · Zayra case · The 8-stage chain |

Details:
- **One H1** (hero). Crumb: Home / Work / comprarcarne.es (ES: Inicio / Trabajo / comprarcarne.es).
- **Hero video:** `<video autoplay muted loop playsinline preload="metadata" data-bgvideo="1" aria-hidden="true" poster="/images/cases/comprarcarne/comprarcarne-hero-poster.webp" src="/media/cases/comprarcarne/comprarcarne-hero-loop-720p.mp4">`
  over the poster (same handling as the Zayra/Arturos hero; poster only with `prefers-reduced-motion`).
  "Watch the film" jumps to section 07: `<video controls playsinline preload="none" width="1280" height="720" poster="/images/cases/comprarcarne/comprarcarne-hero-poster.webp">`
  with `<source src="/media/comprar-carne-spot-2026.mp4" type="video/mp4">`. Never autoplay with sound.
- **Client link** (section 08): `https://comprarcarne.es/`, `target="_blank" rel="noopener"`.
- **Images:** `<picture>` WebP srcset (400/800/1600w) → JPG `<img>` with width/height; lazy everywhere except the hero.
- **"Send us the brief"** uses the existing booking (`/#book`), like the other cases. No new form.
- **EN/ES toggle** swaps `/work/comprarcarne` ↔ `/es/work/comprarcarne`.
- **Analytics (optional):** `data-evt="comprarcarne_cta_click"` (data-loc `case_hero`, `case_closing`, `work_card`,
  `home_feature`) and `data-evt="play_comprarcarne_master"` — keep them only if the existing gtag helper reads data-evt
  generically. Do not touch `generate_lead` or consent.

## 4. SEO for the two new pages

| | EN | ES |
|---|---|---|
| URL | /work/comprarcarne | /es/work/comprarcarne |
| title | comprarcarne.es case: an AI TV commercial for a real client \| AI Creative Lead | Caso comprarcarne.es: spot de TV con IA para un cliente real \| AI Creative Lead |
| description | (seo_meta.json) | (seo_meta.json) |
| html lang / canonical | en / self | es / self |
| hreflang | en, es, x-default (= en) | same |
| OG / Twitter | og:type article, `comprarcarne-og-1200x630.jpg` 1200x630, og:video `/media/comprar-carne-spot-2026.mp4`, summary_large_image | same, og:locale es_ES |

**JSON-LD:** inject `schema_work_comprarcarne_en.jsonld` / `_es.jsonld`, replacing `PUBLISH_DATE_ISO8601` (2 places)
with the real publish date: `CreativeWork` (creator/publisher `#org`, contributor `#cesar`, about/sponsor = the client),
`Organization` (comprarcarne.es, the client), `VideoObject` (master, PT21S, director `#cesar`), `FAQPage` (identical to the
visible FAQ), `BreadcrumbList`. Do not redefine the existing `#org` / `#cesar`.

## 5. Internal linking (all EN + ES)

1. **/work and /es/work — Featured cases (4 cards, 2 × 2).** Replace `section#featured-cases` with
   `snippets/work_featured_cases_{en,es}.html`: **Arturos first** (case of the month, unchanged), **comprarcarne.es second**
   (magenta, tag "CLIENT WORK" / "CLIENTE REAL", silent loop), **Zayra third**, **Miguel Cartujo fourth (now CASE 04 / CASO 04)**.
   Header idx `CASE STUDIES — 04` / `CASOS DE ESTUDIO — 04`. Needs the "/work" block of `comprarcarne-case.css` (`.fcases.four`).
2. **/work and /es/work — The schedule.** The row `COMPRAR CARNE SPOT 2026` gets a crawlable link to the case
   (`snippets/schedule_row_link.html`), same `.wcase` style as the ARTURO SPOT 2026 row. Keep the row's behaviour.
3. **Home (/ and /es).** Replace the content of `section#featured-case` with `snippets/home_featured_case_{en,es}.html`:
   Arturos stays the main block (case of the month); **the comprarcarne.es strip goes right under it, above the Zayra strip**.
   Needs the "Home" block of `comprarcarne-case.css`. Give every new text node `data-en` / `data-es` (copy.json → work_card).
4. **/work/arturos, /es/work/arturos, /work/zayra, /es/work/zayra:** add "comprarcarne.es case" / "Caso comprarcarne.es"
   to `nav.related` (`snippets/related_links.html`). The comprarcarne case already links to Arturos and Zayra.
5. **Insights:** add the sentence + link from `snippets/insights_links.md` at the end of the 2 articles listed there.

## 6. Sitemap, llms.txt, IndexNow

- **sitemap.xml:** add the two entries of `snippets/sitemap_urls.xml` (same format as Zayra/Arturos).
- **llms.txt:** under "## Key pages", after the Arturos line, add `* ` + the line in `snippets/llms_txt_line.txt`; update "Last updated".
- **IndexNow:** after the production deploy, submit /work/comprarcarne, /es/work/comprarcarne, /work, /es/work, / and /es
  through the existing IndexNow setup. If there is none, tell César.

## 7. Checks on the preview URL (all must pass, EN and ES)

1. Both URLs return 200; one H1; title/description from §4; correct `lang`; self canonical; 3 hreflang.
2. The silent loop autoplays muted in the hero and the /work card (desktop, iOS Safari, Android Chrome); the section-07 player
   has poster, controls and sound and never autoplays with sound.
3. JSON-LD valid in Google Rich Results Test and validator.schema.org.
4. /work: Arturos, comprarcarne.es, Zayra, Miguel Cartujo (CASE 04), 2 × 2 on desktop, stacked below 1000 px.
   Home: Arturos block, then comprarcarne.es strip, then Zayra strip. Related links on Arturos and Zayra. 2 Insights links.
5. Only the figures in `metrics.json`; no client business data, prices, delivery times or AI tool names; nothing from the
   spot's creative prompt.
6. Responsive 375 / 768 / 1280 / 1440: no horizontal scroll (the long H1 must fit).
7. Lighthouse mobile on /work/comprarcarne: Performance ≥ 85, SEO ≥ 95, Accessibility ≥ 90. No console errors, zero 404s.
8. Both URLs in sitemap.xml and llms.txt; IndexNow submitted after production.

Send César the preview URL, screenshots (375 and 1440, EN and ES) of the case, the /work block and the Home block, the
Lighthouse scores and the list of changed files. **Production only after his written approval.**
