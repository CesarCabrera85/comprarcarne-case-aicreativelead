COMPRARCARNE.ES BUSINESS CASE — FILES FOR ABACUS.AI

ABACUS_PROMPT.txt        -> the task, step by step. Start here. (Comes AFTER the Arturos package: CesarCabrera85/arturos-case-aicreativelead)
public/                  -> copy this folder into the root of the aicreativelead.com repository, merging with the existing public/ folder.
                            It only ADDS new folders: public/images/cases/comprarcarne/ (76 final, web-optimized images) and
                            public/media/cases/comprarcarne/comprarcarne-hero-loop-720p.mp4 (silent loop for the case hero and the /work card).
                            The film with sound is the master already on the site, /media/comprar-carne-spot-2026.mp4.
REAL CLIENT WORK -> second featured case on /work and the Home, right after Arturos (case of the month), above Zayra. Every change in EN and ES.
instructions/            -> ABACUS_COMPRARCARNE_INTEGRATION.md (full specification), comprarcarne-case.css (only new CSS), copy.json (all texts EN/ES),
                            metrics.json (the only figures allowed), seo_meta.json, JSON-LD EN/ES, alt_texts.csv,
                            snippets/ (ready markup for the case page, /work, Home, related links, Insights, sitemap and llms.txt).
previews/                -> serve the repository with any static server and open: the case page, the /work block and the Home block (EN and ES).
                            previews/_site/ = copies of the live site CSS + the Arturos CSS.

All paths in the snippets, the JSON-LD and seo_meta.json already point to /images/cases/comprarcarne/..., /media/cases/comprarcarne/...
and /media/comprar-carne-spot-2026.mp4.
