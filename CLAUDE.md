# Printex Design – spletna stran (navodila za urejanje s Claude)

Ta repozitorij je celotna spletna stran **Printex Design**. Urejata jo dva človeka, vsak s svojim Claudom (Claude Code na claude.ai/code ali v aplikaciji).

## Kje je stran objavljena
- Javni naslov: **https://printexdesign.netlify.app** (Netlify, projekt `printexdesign`, račun info.printexdesign@gmail.com)
- Objava: Netlify je povezan s tem repozitorijem. Vsak commit na vejo `main` se samodejno objavi v nekaj minutah.
- Pred vsako spremembo naredi `git pull`, da imaš najnovejšo verzijo (stran ureja več ljudi).
- Spremembe commitaj in pushaj na `main` z jasnim opisom v slovenščini.

## Zgradba
- `site/index.html` – vsa stran v eni datoteki (HTML, CSS in JavaScript skupaj).
- `site/img/` – logotip (`logo.png`) in fotografije (`.webp`).
- `netlify.toml` – Netlify objavi samo mapo `site/` (ta datoteka z navodili ni javna).
- Stran ima podstrani, ki se preklapljajo z `#` v naslovu: `#domov`, `#nalepke`, `#table-in-napisi`, `#avtografika`, `#tisk-na-tekstil`, `#kontakt`. Vsaka je `<div class="view" data-view="…">`.
- Animacije uporabljajo knjižnico GSAP s CDN.

## Vsebina in odločitve
- Podjetje: Printex Design. V nogi piše samo »© 2026 Printex Design« (ime s.p. je bilo namenoma odstranjeno).
- Kraj (Ivančna Gorica) je bil namenoma odstranjen s strani.
- Storitve (v tem vrstnem redu): **01 Nalepke, 02 Napisi in table, 03 Avtografika, 04 Tisk na tekstil.**
- NE ponujamo: roll up stojal, digitalnega tiska (letaki, vizitke), 3D nalepk, 3D napisov, foto platen, reklamnih transparentov. Paketov za vozila ni.
- Kontakt: +386 51 273 304, +386 40 539 658, info.printexdesign@gmail.com.
- Galerija pri Avtografiki: kamper (prvi), Koc gradnje, Elektro Zupančič, Hočevar, prikolica. Brez napisov na slikah; registrske tablice so zamegljene.
- Začetna stran: kolaž treh slik – kamper, majice EPJ (logotipi morajo biti vidni), oranžni KTM 233.

## Oblikovanje
- Temna stran v barvah logotipa: ozadje `#100f0d`, bela `#ffffff`, turkizna `#5ec8c1`. Brez drugih barv.
- Pisavi: Unbounded (naslovi), Manrope (besedilo), z Google Fonts.
- Veliki naslovi podstrani imajo turkizno senco (razred `reg`).

## Obrazec za povpraševanje
- Pošilja prek **Web3Forms** naravnost na info.printexdesign@gmail.com.
- Ključ je v `site/index.html` v vrstici `var W3F_KEY='…'` (ključ je javen, to je v redu).
- Polja: ime, kontakt, »Kaj potrebujete?« (brez izbirnega seznama storitev).
- Če pošiljanje ne uspe, stranka dobi gumb »Odpri v e-pošti« in »Kopiraj sporočilo«.
- Obrazec deluje samo na pravi spletni strani (Netlify), ne v predogledu na Claudu.

## Pri urejanju
- Spreminjaj samo to, kar je naročeno; ostalo pusti, kot je.
- Nove fotografije pretvori v `.webp` (širina do ~1100 px) in jih shrani v `site/img/`.
- Na fotografijah vozil zamegli registrske tablice.
- Po spremembi commitaj in pushaj; uporabniku povej, kaj si spremenil.
