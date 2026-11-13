# Marks Berjozins - tīmekļa portfolio

Vietne: [https://tankist256.github.io/WEB/](https://tankist256.github.io/WEB/)

HTML un CSS mācību darbi. GitHub Pages izmanto repozitorija `WEB` zarā `main` esošo saknes mapi `/`.

- [Sākumlapa](index.html)
- [Digitālā vizītkarte](vizitkarte/index.html)
- [Profila lapa](Marks%20Berjozins.html)

Sākotnējā repozitorijā bija tikai profila lapa un `style.css`. Vizītkarte pievienota N10 sagatavošanas laikā, izmantojot profilā jau esošo informāciju; agrāka N1 versija repozitorija vēsturē nebija pieejama.

## N10 komentāri

1. **Repozitorijs un vēsture.** Pirms N10 izmaiņām GitHub API un `git log --oneline` abos bija 11 commiti. Pēc klonēšanas darba koks bija tīrs. Izmantots esošais `tankist256/WEB`, tāpēc vietnes adresē ir `/WEB/`.

2. **Sākumlapa.** `index.html` ir mapes noklusējuma sākumlapa: atverot vietnes adresi bez faila nosaukuma, serveris parāda šo failu. Saites `vizitkarte/index.html` un `Marks%20Berjozins.html` ir relatīvas; `%20` apzīmē atstarpi esošā profila faila nosaukumā.

3. **Publicēšana.** Ieslēgts GitHub Pages režīms “Deploy from a branch”, zars `main`, mape `/` (root). Adrese: [https://tankist256.github.io/WEB/](https://tankist256.github.io/WEB/). Pirmā sākumlapa bija pieejama aptuveni 44 sekundēs jeb 0,7 minūtēs pēc Pages ieslēgšanas (pārbaudes intervāls 5 s). [Pirmā Actions izvietošana](https://github.com/tankist256/WEB/actions/runs/43399984763) pabeigta sekmīgi.

4. **Failu ceļi.** Sākotnējie attēli norādīja uz `/home/tankist256/...`, kas GitHub Pages serverī neeksistē. Tie aizstāti ar repozitorijā saglabātu SVG koda vietturi un relatīvu ceļu. Publicētajā vietnē pārbaudīts ceļš sākumlapa → vizītkarte → profils → sākumlapa, sadaļu saites, visi 10 attēli, abi sākumlapas darbu linki un visu trīs lapu CSS. Visi vietējie lapu un resursu pieprasījumi atgrieza HTTP 200; pārlūka pārbaudē nebija 404 vai JavaScript kļūdu.

5. **Telefons.** Chrome pārbaudīti 320 × 740, 390 × 844, 844 × 390 un 1280 × 900 skati: visās trīs lapās nav horizontālas ritjoslas. Pie 390 px profila navigācija ir 2 × 2, galerija ir divās kolonnās un virsraksts ir 26 px; pie 320 px galerija ir vienā kolonnā. Pārbaude īstā telefonā vēl jāveic: atvērt vietni vertikāli un horizontāli un salīdzināt ar 390 px pārlūka skatu. Īstas ierīces novērojumi vēl nav pieejami.

6. **README.** Pievienota klikšķināma vietnes adrese un šie septiņi N10 komentāri. Failu labojumi tiek veikti lokāli un publicēti ar `git push`.

7. **Atjaunināšana.** Pēc pirmās publicēšanas sākumlapas kājenē pievienots `Atjaunināts 13.11.2026`. Jaunais datums tiešsaistē parādījās aptuveni 38 sekundes jeb 0,6 minūtes pēc atsevišķā `git push` sākuma (pārbaudes intervāls 5 s, pieprasījumi bez kešatmiņas). [Datuma atjauninājuma Actions darbs](https://github.com/tankist256/WEB/actions/runs/43400231776). Pēc `git push` GitHub Pages palaiž vietnes būvēšanu un izvietošanu, pēc tam jaunie faili ir pieejami vietnes adresē. Pārlūka kešatmiņas dēļ var būt vajadzīgs `Ctrl+F5`.

## Pārbaude lokāli

Repozitorija mapē palaid `python3 -m http.server 8000` un atver [http://localhost:8000/](http://localhost:8000/).

## Papildu skaidrojumi

- Saite ar sākuma slīpsvītru, piemēram, `/profils/index.html`, ved uz domēna sakni `https://tankist256.github.io/profils/index.html`, nevis projekta mapi `/WEB/`. Tāpēc šajā vietnē izmantoti relatīvi ceļi un esošie failu nosaukumi.
- Git neglabā tukšas mapes. Ja `melnraksti/` nav commitā vai tajā nav publicēta sākumlapas faila, šī adrese var atgriezt 404.
- Kontaktforma profilā ir HTML mācību piemērs; tai nav datu nosūtīšanas servera.
