# Analiza sličnih aplikacija za razvoj TransCorea

**Predmet:** Razvoj softvera 1 (2026/27). **Analizirani proizvod:** TransCore — informacioni sistem jedne transportne firme. **Datum pregleda javno objavljenih izvora:** 03.11.2026.

## 1. Cilj i metoda

Pregledane su javno dostupne funkcionalnosti i promotivni prikazi tri web rješenja. Poređenje služi za identifikaciju korisnih obrazaca interfejsa i funkcija. **Nije sprovedeno korisničko testiranje tih proizvoda niti postoji pristup njihovim zatvorenim administratorskim ekranima.**

## 2. Putninalog.ba

**Izvor:** https://putninalog.ba/

Platforma opisuje kreiranje, odobravanje, arhiviranje i pretraživanje putnih naloga, evidenciju vozila i vozača, statusa te upozorenja o registraciji i servisima. Javni prikazi obuhvataju listu naloga i pregled vozila.

**Primjenjivo na TransCore:** tabela naloga s pretragom i filterima (issues #4, #8 kroz liste); pregled vozila s rokom registracije (#3, #7); početna kontrolna ploča s upozorenjima (#18). **Razlika:** putni nalog PN-3/PN-4 nije isto što i transportni nalog s obaveznim CMR postupkom.

## 3. CargoTMS

**Izvori:** https://cargotms.ro/?lang=en i https://cargotms.ro/order-management?lang=en

Javno opisani moduli su pregled i dodjela transportnih naloga, statusi, evidencija vozila i vozača, CMR dokumentacija, troškovi i finansijski prikazi. Javni katalog prikazuje galeriju slika koje provajder označava kao snimke platforme.

**Primjenjivo na TransCore:** strukturisani detalji naloga, dozvoljene promjene statusa, veza dokumentacije i jednog transporta (issues #4–#12), finansijski sažetak (#13–#17). **Izvan opsega TransCorea:** SaaS multi-company, portali klijenata/prevoznika, izdavanje faktura i napredni planeri.

## 4. APN — Putni i radni nalozi

**Izvori:** https://apn.ba/ i https://apn.ba/putni-nalozi/

APN javno opisuje evidenciju putnih naloga, vozila, kilometraže, troškova, odobravanja i PDF arhive. Posebno su relevantni jasni statusi naloga i povezivanje vozača s vozilom.

**Primjenjivo na TransCore:** razumljiv korisnički tok od kreiranja do zatvaranja naloga, unos kilometraže (#9), prikaz troškova (#13–#15) i PDF dokument (#16–#17). **Razlika:** APN pokriva i opće putne/radne naloge, a naš fokus je transport robe i pregled CMR-a.

## 5. Poređenje

| Kriterij | Putninalog.ba | CargoTMS | APN | TransCore — projektni cilj |
|---|---|---|---|---|
| Evidencija vozila/vozača | Javno navedeno | Javno navedeno | Javno navedeno | Da |
| Planiranje naloga | Putni nalozi | Transportni nalozi | Putni nalozi | Da |
| Provjera termina i registracije | Upozorenja javno opisana; preklapanje nije potvrđeno | Nije potvrđeno tačno pravilo preklapanja | Nije potvrđeno tačno pravilo preklapanja | Obavezno: zabrana konfliktnih dodjela |
| CMR odbijanje i verzije | Nije potvrđeno | CMR arhiva opisana; detalji verzionisanja nisu potvrđeni | Nije potvrđeno | Obavezno: razlog i prethodne verzije |
| Finansijski pregled | Prikazi izvještaja | Troškovi / dobit po nalogu | Troškovi | Dogovorena cijena minus evidentirani troškovi |
| PDF | Da | Da | Da | Nalog i finansijski izvještaj |
| Zaštićen pristup vozača | Uloge javno opisane | Portal vozača javno opisan | Uloge javno opisane | Samo dodijeljeni nalozi |

**Zaključak:** Za TransCore treba preuzeti principe preglednosti, a ne opseg drugih sistema. Posebna vrijednost našeg projekta su zabrana vremenskih preklapanja, provjera registracije za planirani termin i zatvaranje tek nakon prihvaćenog CMR-a.

## 6. Izvori

1. Putninalog.ba — https://putninalog.ba/ (pristup: 03.11.2026)
2. CargoTMS — https://cargotms.ro/?lang=en (pristup: 03.11.2026)
3. CargoTMS / Order Management — https://cargotms.ro/order-management?lang=en (pristup: 03.11.2026)
4. APN — https://apn.ba/ (pristup: 03.11.2026)
5. APN / Putni nalozi — https://apn.ba/putni-nalozi/ (pristup: 03.11.2026)

**Ograničenje:** informacije su preuzete iz javnih opisa. Nisu potvrđene neobjavljene mogućnosti, cijene ni privatni ekrani.
