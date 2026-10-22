# Java IV — Festivali që përshtatet në çdo ekran

## Çfarë mëson

Flexbox, Grid, media queries dhe pamje responsive.

Referencë tematike: kap. 6–7 të librit.

## Skenari

Programi i një festivali shkencor duhet të lexohet si në telefon ashtu edhe në ekran të gjerë.

## Kërkesat

1. Krijo gjashtë karta aktivitetesh dhe një menu fleksibile.
2. Përdor Grid: një kolonë nën 600 px, dy nga 600 deri në 899 px dhe tri nga 900 px.
3. Kartat kanë titull, kategori, orar dhe lidhje detajesh; teksti i gjatë nuk duhet të dalë jashtë.
4. Përdor imazh fleksibël dhe mos përdor lartësi fikse për tekstin.
5. Testo në 360, 768 dhe 1280 px; ruaj rezultatet në README.

## Rastet e pranimit

- [x] Në 360/768/1280 px shfaqen përkatësisht 1/2/3 kolona.
- [x] Nuk ka scroll horizontal në faqen e plotë.
- [x] Menuja mbetet e përdorshme me tastierë.

## Sfida e transferimit

Një titull 100-karakterësh duhet të përshtatet pa prishur kartën. Kjo sfidë është formuese; nuk jep bonus jashtë rubrikës.

## Dorëzimi dhe GitHub

Puno në JavaIV/ të repository-t individual. Dorëzo kodin, asetet lokale dhe README.md me: çfarë realizove, hapat e hapjes, hyrje → rezultat i pritur → rezultat i marrë për testet, përgjigjen e reflektimit dhe deklarimin e AI/burimeve. Për React dorëzo edhe package.json dhe lockfile; mos dorëzo node_modules/ ose dist/.



## Reflektim individual

Kur do të zgjidhje Flexbox dhe kur Grid?
Flexbox do ta zgjidhja kur më duhet të organizoj elementet në një
drejtim, horizontalisht ose vertikalisht, si menuja e navigimit.
Ai është i përshtatshëm për rreshtimin e elementeve dhe menaxhimin
e hapësirës ndërmjet tyre.
 

## Çfarë realizova

- Krijova gjashtë karta aktivitetesh me titull, kategori, orar dhe lidhje.
- Ndërtova një menu fleksibile me Flexbox.
- Përdora CSS Grid për paraqitjen e kartave.
- Shtova imazhe responsive me `max-width: 100%` dhe `object-fit: cover`.
- Përdora `overflow-wrap: anywhere` për titujt dhe tekstet e gjata.
- Përdora `minmax(0, 1fr)` për të ndihmuar në parandalimin e tejkalimit
  të gjerësisë së kolonave.
- Shtova media queries për ekranet mobile, tablet dhe desktop.
- Shtova lidhjen "Kalo te përmbajtja" dhe treguesit e fokusit për tastierë.
- Nuk përdora lartësi fikse për përmbajtjen tekstuale të kartave.


##  Si hapet projekti

1. Shkarkoni ose klononi repository-n.
2. Hapni dosjen `JavaIV`.
3. Hapni `index.html` në një shfletues si Chrome ose Edge.
4. Për ndryshime në dizajn, modifikoni skedarin `style.css`.
5. Për ndryshime në përmbajtje, modifikoni skedarin `index.html`.

Nuk nevojitet instalimi i paketave ose nisja e një serveri.

### Si testova

Hapa DevTools me F12 dhe aktivizova pajisjet responsive.
Testova gjerësitë 360px, 768px dhe 1280px.
Kontrollova numrin e kolonave, tekstet, imazhet dhe navigimin me tastierë.

Për të kontrolluar nëse faqja ka scroll horizontal, ekzekutova
në Console:

    document.documentElement.scrollWidth <=
    document.documentElement.clientWidth

Rezultati `true` tregon se dokumenti nuk është më i gjerë se viewport-i.