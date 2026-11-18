# EN-DIZAJN — sajt (statička verzija za Vercel)

Čist HTML, CSS i JavaScript. Nema build koraka, nema zavisnosti.

## Struktura

```
index.html            početna (hero „Dva sveta“, O nama, Za vaš dom, Za dečiju sobu, Inspiracija, newsletter)
katalog.html          katalog + stranica proizvoda i konfigurator (/katalog?model=zeka)
404.html              stranica za grešku
vercel.json           čisti URL-ovi (/katalog), keširanje, sigurnosna zaglavlja
assets/css/main.css   svi tokeni (boje, tipografija, pokreti) i komponente — jedan fajl za podešavanje
assets/css/fonts.css  lokalni fontovi (Cormorant Garamond, Hanken Grotesk; latin + latin-ext)
assets/js/main.js     zaglavlje, meni, animacije, kursor, newsletter
assets/js/katalog.js  podaci o modelima, filteri, konfigurator
assets/img/           obrađene slike (NN.webp + verzije 640 i 1024 px)
```

## Objava na Vercelu

**Najbrže (bez naloga na GitHubu):**
1. Raspakujte ZIP.
2. Instalirajte Vercel CLI: `npm i -g vercel`
3. U raspakovanom folderu pokrenite `vercel`, zatim `vercel --prod`.
   Kod pitanja o podešavanjima: Framework „Other“, Build Command prazno, Output Directory `.`

**Preko GitHuba (preporučeno za dugoročno održavanje):**
1. Postavite sadržaj foldera u novi GitHub repozitorijum.
2. Na vercel.com: Add New → Project → izaberite repozitorijum.
3. Framework Preset: **Other**. Build i Output ostavite prazno. Deploy.
   Svaki push na `main` automatski objavljuje novu verziju.

**Domen:** Vercel → Project → Settings → Domains. Posle dodavanja domena zamenite
`[[PLACEHOLDER: domen]]` u `robots.txt` i `sitemap.xml`.

## Pre puštanja u javnost (otvorene stavke)

Sve što nije potvrđeno je na sajtu vidljivo označeno kao `[[PLACEHOLDER: …]]`:
- cene i cenovnik, naziv kreveta sa mišjim ušima;
- biblioteka štofova (tonovi su privremeni), politika slanja uzoraka;
- materijal i konstrukcija, garancija, rok izrade, rok i cena dostave, načini plaćanja;
- telefon, Viber, WhatsApp, email, adresa, radno vreme, PIB/MB i pravni tekstovi;
- servis za newsletter (forma je sada samo prikaz, ne šalje podatke — `assets/js/main.js`, TODO);
- vektorski logo (sada je rekonstrukcija monograma);
- prave fotografije iz domova kupaca (Realizacije), profesionalno snimanje, potvrda da li su slike renderi i dozvola za korišćenje.

Linkovi Materijali i Atelje, kao i korpa, još nemaju svoje stranice (vode na `#`).
