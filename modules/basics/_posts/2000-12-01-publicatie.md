---
title: Publicatie
---

<div class="header1" id="publish-finish" markdown="1">
# Publicatie & Afronding
</div>

In dit laatste hoofdstuk leer je hoe je jouw (voltooide) website kunt **publiceren** via GitHub Pages, zodat deze online toegankelijk is. Daarnaast nemen we kort de **geleerde lessen** door en wijzen we je op **verder studiemateriaal** voor wie zich verder wil verdiepen in Bootstrap en front-end development.

---

<div class="header2" markdown="1">
## 12.1 Website online zetten (GitHub Pages)
</div>

Als je je eindproject in een **GitHub-repository** hebt staan, kun je het met een paar klikken publiceren via **GitHub Pages**. Zo kun je gemakkelijk een **publieke URL** maken, die je kunt delen met docenten, klasgenoten en iedereen die je werk wil zien.

### 1. Repository-instellingen
1. Ga naar je repository op GitHub (bijv. `github.com/<gebruikersnaam>/<repositorynaam>`).  
2. Klik op **Settings** (tab bovenin).  
3. Zoek in de zijbalk of onder “Code and automation” naar **Pages** (afhankelijk van de GitHub-interface kan dit iets verschillen).  
4. Selecteer onder “Branch” de **main-branch** (of een andere branch waarin je productiesite staat).  
5. Klik op **Save**.

### 2. Juiste folder selecteren
Als je al je **HTML-bestanden** (zoals `index.html`) in de **hoofdfolder** van je repository hebt staan, kun je “Root” als folder kiezen. Heb je ze in een map `/docs`, dan kies je die. 

### 3. Publicatie
Na enkele seconden tot minuten krijg je in de Pages-sectie een **URL** te zien, bijvoorbeeld:  
```
https://<gebruikersnaam>.github.io/<repositorynaam>/
```
Daar staat nu je eindproject online!

**Opmerking**: GitHub Pages werkt alleen met **statisch** materiaal (HTML, CSS, JS). Heb je een back-end nodig (bijv. PHP, Node-server), dan zul je andere hostingmethoden moeten gebruiken.

<div class="note protip">
<p>Protip: Wil je je site in een eigen domein publiceren? Dan kun je in GitHub Pages een “custom domain” instellen. Dit vereist wat extra DNS-configuratie, maar is zeker mogelijk.</p>
</div>


---

<div class="header2" markdown="1">
## 12.2 Reflectie: wat hebben we geleerd?
</div>

Nu je alle hoofdstukken en opdrachten hebt doorlopen, is het belangrijk om te reflecteren op je **leerproces**:

1. **Bootstrap Grondbeginselen**  
   - Gebruik van het **Grid-systeem** voor responsieve layouts.  
   - Kennis van **Utility-classes** (marges, kleuren, typografie).  
   - Inzetten van **Components** zoals navbars, forms, carousels, modals, enz.

2. **Sass en Thematisering**  
   - Aan de hand van de **Sass-bronbestanden** kon je variabelen aanpassen (`$primary`) en je eigen CSS structureren.  
   - Je leerde hoe je de **CDN-benadering** vergelijkt met het **zelf downloaden** van Bootstrap.

3. **Git en GitHub**  
   - Werken in **branches** (feature, bugfix) voor overzicht en stabiliteit.  
   - **Pull requests** en **code review**: hoe je elkaars werk controleert en feedback geeft.  
   - **Merge-conflicten** oplossen wanneer je in dezelfde bestanden werkt.

4. **Samenwerking**  
   - Teamwork in paren, taakverdeling, elkaars code reviewen.  
   - Communicatie over wie wat wanneer doet om conflicten te minimaliseren.

5. **Eindresultaat**  
   - Een **volledige website** met meerdere pagina’s, responsive design, herbruikbare componenten en gepersonaliseerd met eigen kleuren.  
   - Publicatie via **GitHub Pages** zodat de site wereldwijd toegankelijk is.



---

<div class="header2" markdown="1">
## 12.3 Verdere leermogelijkheden (Documentatie, Bootstrap geavanceerde topics, etc.)
</div>

Hoewel je nu al een heel eind komt met Bootstrap, is er altijd meer te ontdekken:

1. **Officiële documentatie**:  
   - [getbootstrap.com/docs](https://getbootstrap.com/docs) – de meest uitgebreide en up-to-date bron.  
   - Speciale aandachtspunten: **Accessibility**, **Utilities**, **Extend**-documentatie.  

2. **Geavanceerde onderwerpen**  
   - **Bootstrap Icons** of andere iconpacks (Font Awesome, Iconify).  
   - **Custom Build**: selectief importeren van alleen de Bootstrap-componenten die je nodig hebt, zodat je bestand kleiner wordt.  
   - **JavaScript Customizing**: verder inspelen op modals, carousels, events en triggers.  
   - **Bootstrap 5 + Vue/React**: integratie met moderne frameworks voor dynamische single-page-apps.

3. **Andere frameworks**  
   - **Tailwind CSS** (utility-first), **Bulma**, **Foundation**, **Material UI** (voor React), etc. – elk met andere filosofieën en features.

4. **Back-end en databanken**  
   - **PHP** of **Node.js** voor server-side logica, en **SQL** of **MongoDB** voor databanken.  
   - Eventuele frameworks als **Laravel**, **Express**, **Django**, etc.

5. **Web Performance en Ops**  
   - **Minification**, **bundling**, **tree-shaking** om sites sneller te maken.  
   - **Hosting** (Netlify, Vercel, AWS, etc.), Continuous Integration (GitHub Actions), enz.

---

**Conclusie**  
Je hebt nu de kernconcepten en praktijkervaring van **Bootstrap 5** beheerst, van basale layout tot geavanceerde componenten en personalisatie met **Sass**. Je begrijpt hoe je via **GitHub** kunt samenwerken en je project kunt publiceren op **GitHub Pages**. 

Ga vooral **experimenteren**, **leren** en **up-to-date** blijven met nieuwe ontwikkelingen, want de wereld van webdevelopment evolueert voortdurend!  
