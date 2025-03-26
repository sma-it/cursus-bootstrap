---
title: Eindopdracht
---

<div class="header1" id="final-project" markdown="1">
# Eindopdracht: Volledige Website Bouwen
</div>

In dit afsluitende hoofdstuk breng je **alle kennis en onderdelen** uit de voorgaande lessen samen. Je bouwt (of rondt af) een **volledige website** in Bootstrap, met aandacht voor **responsiviteit**, **performance**, **SEO-basics** en **toegankelijkheid**. De website kan bestaan uit meerdere pagina’s met alle componenten die je hebt geleerd: navbars, forms, modals, carousels, en meer.

---

<div class="header2" markdown="1">
## 11.1 Samenvoegen van alle pagina’s en componenten tot één project
</div>

### 1. Verzamel alle pagina’s
In de loop van deze cursus heb je verschillende pagina’s opgezet (bijv. `index.html`, `about.html`, `services.html`, `contact.html`). Zorg dat:
- **Alle bestanden** in je projectmap staan, met **consistente navigatie** (navbar) en **footer**.  
- De naamgeving en structuur **duidelijk** is, bijvoorbeeld in een `/pages/` map als je veel pagina’s hebt.

### 2. Hergebruik van herhalende elementen
- **Header/Nav**: Elke pagina zou dezelfde (of quasi dezelfde) `<nav>`-structuur moeten hebben, zodat de gebruiker gemakkelijk kan navigeren.  
- **Footer**: Gebruik een vergelijkbare `<footer>`-opbouw of kopieer dezelfde HTML naar elk bestand (of maak server-side includes, als je dat kunt).  
- **CSS en JS-bestanden**: Zorg dat elke pagina linkt naar dezelfde **gecompileerde CSS** (als je met Sass werkt) en – indien nodig – dezelfde **Bootstrap JS-bundels**.  

### 3. Check of alle content volledig is
- Heb je **cards**, **carousels**, **modals** of **forms** aangemaakt tijdens eerdere hoofdstukken? Zet ze in de juiste pagina’s of secties waar ze logisch passen.  
- Heb je eventueel nog **dummy-tekst** (lorem ipsum)? Vervang die door zinvollere content, indien je een meer realistisch eindresultaat wilt.  

<div class="note protip">
<p>Protip: Voor je eindopdracht kun je <strong>extra</strong> elementen of pagina’s toevoegen (bijv. FAQ, Portfolio) als je daar tijd voor hebt. Zo onderscheid je je werk en toon je eigen creativiteit.</p>
</div>

---

<div class="header2" markdown="1">
## 11.2 Responsiviteit controleren en verfijnen
</div>

### 1. Inspecteer je layout op verschillende schermgroottes
- **Desktop**: Maximaliseer je browser en kijk of je layout nog aangenaam is.  
- **Tablet/middelgroot**: Verklein je browservenster rond de `768px`-breedte. Let op kolombreedtes, navbar collapse, carousels.  
- **Mobiel/smal**: Bekijk rond `576px` of zelfs `375px`. De navbar moet inklappen, images moeten niet uit het scherm lopen, teksten blijven leesbaar.  

### 2. Pas breakpoints en utility-classes aan
Gebruik indien nodig:
- **`.col-sm-6`, `.col-md-4`** etc. om een betere layout te krijgen op bepaalde resoluties.  
- **`.d-none`, `.d-block`, `.d-md-none`** etc. om specifieke elementen te verbergen of tonen, afhankelijk van de schermgrootte.  
- **`.text-center`, `.ms-auto`, `.mt-3`** om kleine details van spacing of uitlijning te verbeteren.


<div class="note protip">
<p>Protip: Schakel de <em>Device Toolbar</em> in je browser-devtools in om snel te zien hoe je site eruitziet op populaire toestellen als iPhone, iPad, Galaxy, etc.</p>
</div>


---

<div class="header2" markdown="1">
## 11.3 Final touches: performance, SEO-basics, toegankelijkheid
</div>

### 1. Performance
- **Afbeeldingen**: Zijn ze niet te groot? Overweeg het comprimeren van grote JPG’s en PNG’s.  
- **Minify** of **compress** je CSS en JS als je de beste performance wilt. Met Sass en build-tooling kun je vaak met één klik minification inschakelen.  
- **Cachen**: Bij hostingdiensten wordt de CSS/JS vaak automatisch gecachet.  

### 2. SEO-basics
- **HTML `<title>` tag**: Zorg dat elke pagina een betekenisvolle titel heeft.  
- **Meta description**: `<meta name="description" content="Korte omschrijving van de pagina">`.  
- **Semantische HTML-tags**: Gebruik `<header>`, `<main>`, `<section>`, `<footer>`, `<article>` waar mogelijk – zoekmachines waarderen gestructureerde content.  
- **Goede URL-structuur**: Bijv. `mysite.com/about` (als je server-side routing hebt) in plaats van `mysite.com/page2`.

### 3. Toegankelijkheid (A11y)
- **Alt-teksten** bij afbeeldingen: `<img src="..." alt="Beschrijving">`.  
- **Kleurcontrast**: Zorg dat je tekst duidelijk leesbaar is op de achtergrond.  
- **Navigatie per toetsenbord**: Test of je met `Tab` door linkjes en formvelden kunt, en of je modalvensters sluitbaar zijn via het toetsenbord.  
- **ARIA-labels** waar nodig, bijv. `aria-label="Sluiten"` bij knoppen in modals.

<div class="note waarschuwing">
<p>Let op: A11y is een groot onderwerp. Doe er op zijn minst <em>iets</em> aan. Let bv. op <strong>Alt-teksten</strong> en <strong>contrasten</strong>, zodat je site ook bruikbaar is voor wie slechtziend of blind is.</p>
</div>


---

<div class="header2" markdown="1">
## 11.4 Presentatie van de eindresultaten en peer review
</div>

### 1. Laat je website zien
- **Presentatie**: Laat in de klas (of online) zien hoe je site eruitziet en leg kort uit welke componenten je hebt gebruikt.  
- **Navigatie**: Loopt alles vloeiend? Klapt de navbar correct in op kleine schermen?  
- **Interactiviteit**: Laat modals, carousels, tabs, forms en andere dynamische elementen zien.

### 2. Peer review
- **Vraag feedback** van je medestudenten: wat valt op, wat kan beter?  
- **Gemeenschappelijke code-check**: hebben jullie duidelijke commit-berichten, is er een net map- en bestandsstructuur?  
- **Verbetersuggesties**: noteer ideeën voor extra pagina’s, nieuwe functies, of styling-aanpassingen die je in een volgende iteratie kunt uitvoeren.

### 3. Reflectie
Denk na over:
- Wat ging er **goed**? (Bijv. structuur van je code, samenwerking via GitHub)  
- Wat was **moeilijk**? (Bijv. responsiviteit, Sass-setup)  
- Hoe kun je dit in **toekomstige projecten** verbeteren of automatiseren?


<div class="note protip">
<p>Protip: Overweeg je site te publiceren via <strong>GitHub Pages</strong> of een andere hosting, zodat je mede-leerlingen, vrienden of potentiële werkgevers je werk kunnen zien.</p>
</div>


---

### Resultaat
Na dit hoofdstuk heb je een **complete, meervoudige pagina-website** in Bootstrap, met:
1. **Responsieve layout** en meerdere componenten (navbar, forms, cards, modals, etc.).  
2. **Samenwerking** in paren, met branch- en merge-praktijken via GitHub.  
3. **Performance, SEO en toegankelijkheids**-oplossingen voor een professioneel en gebruiksvriendelijk eindresultaat.  

Je bent klaar om je werk te **presenteren** en te **reviewen**. Succes!