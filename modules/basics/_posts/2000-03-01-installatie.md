---
title: Bootstrap Installatie & Structuur
---

<div class="header1" id="bootstrap" markdown="1">
# Bootstrap Installatie & Structuur
</div>

In dit hoofdstuk leer je hoe je Bootstrap kunt toevoegen aan je webproject en hoe je de basisstructuur van een Bootstrap-pagina opzet. We bespreken de voor- en nadelen van **CDN** (Content Delivery Network) en een **lokale installatie**, en geven best practices voor het werken met Bootstrap.

---

<div class="header2" markdown="1">
## Manieren om Bootstrap te integreren (CDN vs. lokale installatie)
</div>

### 1. CDN (Content Delivery Network)
Een **CDN** is een netwerk van servers over de hele wereld. Wanneer je de Bootstrap-bestanden laadt via een CDN, zorgt dit voor:
- **Snellere laadtijden** voor gebruikers die de bestanden al eens hebben gedownload via dezelfde CDN (bijv. op een andere website). De bestanden kunnen dan al in de browsercache zitten.  
- **Minder onderhoud** aan je project, omdat je zelf geen bestanden hoeft bij te houden.  

Om Bootstrap via een CDN te gebruiken, plaats je in de `<head>` van je HTML-bestand een link naar de officiële Bootstrap CSS en (optioneel) de JS-bundel. Bijvoorbeeld:

```html
<link 
  rel="stylesheet" 
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" 
  integrity="sha384-..." 
  crossorigin="anonymous"
/>
<script 
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js" 
  integrity="sha384-..." 
  crossorigin="anonymous">
</script>
```

<div class="note protip">
<p>Protip: Door gebruik te maken van een CDN hoeft een gebruiker de Bootstrap CSS niet opnieuw te downloaden als deze al in de cache staat. Dit verkort de laadtijd van je website.</p>
</div>

### 2. Lokale installatie
Wil je liever **niet afhankelijk** zijn van een externe dienst, of heb je bijvoorbeeld geen stabiele internettoegang tijdens de ontwikkeling, dan kun je de Bootstrap-bestanden lokaal hosten:

1. **Download** de Bootstrap-bundel via de [officiële website](https://getbootstrap.com/).  
2. **Plaats** de CSS- en JS-bestanden in een lokale map (bijv. `css/` en `js/`).  
3. **Link** er in je HTML-bestand naar, bijvoorbeeld:
   ```html
   <link rel="stylesheet" href="css/bootstrap.min.css">
   <script src="js/bootstrap.bundle.min.js"></script>
   ```

Het voordeel hiervan is dat je **geen extern verkeer** hoeft toe te staan. Nadelen zijn dat je zelf verantwoordelijk bent voor updates en dat gebruikers die je site nog niet bezocht hebben, de bestanden altijd volledig moeten downloaden.

---

<div class="header2" markdown="1">
## Basis-Bootstrap-structuur en best practices
</div>

Om optimaal van Bootstrap gebruik te maken, is er een aantal basisregels en -onderdelen die je in bijna elke pagina zult gebruiken:

1. **Doctype en responsive meta-tag**  
   Zorg dat je bovenaan je HTML-document de juiste doctype en de meta-tag voor mobiel hebt:
   ```html
   <!DOCTYPE html>
   <html lang="nl">
     <head>
       <meta charset="utf-8">
       <meta name="viewport" content="width=device-width, initial-scale=1">
       <title>Mijn Bootstrap-pagina</title>
       <!-- Bootstrap CSS (CDN of lokaal) -->
     </head>
     <body>
       ...
     </body>
   </html>
   ```

2. **Container**  
   In Bootstrap gebruik je een `.container` (of `.container-fluid`) om de inhoud netjes gecentreerd te houden en om te zorgen dat de layout op verschillende schermformaten goed wordt weergegeven:
   ```html
   <div class="container">
     <h1>Welkom!</h1>
     <p>Dit is een eerste test met Bootstrap.</p>
   </div>
   ```

3. **Grid-systeem**  
   Het hart van Bootstrap is het **Grid-systeem**, waarmee je je content in kolommen kunt verdelen die zich aanpassen aan de schermgrootte. Je start meestal met een `row` en deelt deze vervolgens in kolommen, zoals:
   ```html
   <div class="row">
     <div class="col-md-6">Linker kolom</div>
     <div class="col-md-6">Rechter kolom</div>
   </div>
   ```
   We gaan hier in latere hoofdstukken dieper op in.

4. **Utility Classes**  
   Bootstrap biedt talloze ‘utility classes’ (bijv. `mt-3`, `p-2`, `text-center`, etc.) om snel zaken als marges en uitlijning aan te passen. Zo kun je veel styling regelen zonder zelf uitgebreide CSS te schrijven.

5. **Mobile-first principe**  
   Bootstrap hanteert een **mobiele-first** benadering: de layout is standaard geoptimaliseerd voor kleine schermen en schaalt mee naar grotere schermen. Zorg er daarom voor dat je **niet** te veel vaste pixels gebruikt en gebruik de breakpoints (`sm`, `md`, `lg`, `xl`, `xxl`) slim.

<div class="note oefening">
<p>
<b>Oefening:</b> Maak een nieuwe <code>index.html</code> met de juiste Bootstrap CDN-koppelingen in de <code>&lt;head&gt;</code>. Plaats een <code>.container</code> met één <code>.row</code> en twee <code>.col</code>-elementen. Kijk wat er gebeurt als je het browservenster verkleint of vergroot.
</p>
</div>


Door op deze manier met Bootstrap aan de slag te gaan, heb je een stevige basis voor het bouwen van mooie, responsieve pagina’s. In de volgende hoofdstukken gaan we dieper in op het **Grid-systeem**, **componenten** en andere handige Bootstrap-onderdelen.



<div class="header2" markdown="1">
## Bootstrap documentatie: hoe en waar vind je wat?
</div>

De **officiële documentatie** is de meest uitgebreide en actuele bron om snel onderdelen en codevoorbeelden te vinden. Je kunt deze altijd raadplegen via:  
[**getbootstrap.com/docs/5.3/**](https://getbootstrap.com/docs/5.3/) *(of de nieuwste versie)*

### Wat vind je in de documentatie?

1. **Layout (Grid)**  
   Een uitgebreide uitleg over hoe het Grid-systeem werkt, inclusief alle opties voor verschillende kolombreedtes, offsets en responsieve breakpoints.

2. **Components**  
   Voorbeelden van voorgebouwde elementen zoals navbars, cards, modals, buttons, forms en nog veel meer. Je ziet direct de HTML die je kunt kopiëren en plakken in je eigen project.

3. **Utilities**  
   Een lijst met handige ‘utility-classes’ om snel spacing, uitlijning, kleuren, typografie en positionering aan te passen. Bijvoorbeeld `m-3` (margin), `p-2` (padding) of `text-center` (tekst uitlijnen in het midden).

4. **Customize**  
   Informatie over hoe je met SASS of eigen CSS de standaard Bootstrap-styling kunt overschrijven en je eigen kleurenschema kunt creëren.


<div class="note protip">
<p>Protip: Weet je even niet meer welke klasse je nodig hebt om bijvoorbeeld padding of margin aan te passen? Zoek in de utilities-sectie naar <strong>Spacing</strong> en je vindt direct de classes die je kunt gebruiken.</p>
</div>


---


<div class="header2" markdown="1">
## Oefening: Je eerste Bootstrap-pagina’s in paren
</div>


In deze oefening ga je samen met je partner in jullie bestaande GitHub-project twee aparte webpagina’s maken. Vervolgens koppel je Bootstrap aan beide pagina’s en ga je ermee experimenteren. 

### Doel van de oefening
- **Samenwerking via Git**: Je werkt in je eigen branch en voegt later jullie werk samen.  
- **Bootstrap toepassen**: Op elke pagina moeten voldoende elementen staan om verschillende Bootstrap-componenten uit te proberen.

---

## Stappenplan

### 1. Maak nieuwe branches aan
1. **Bespreek met je partner** wie de `index.html` voor zijn rekening neemt en wie een tweede pagina, bijvoorbeeld `about.html`, maakt.  
2. Ga VSCode en zorg dat je op de `main`-branch zit.
3. Maak een nieuwe branch voor jouw pagina. Een goede branch-naam is bijvoorbeeld `feature/mijn-pagina`.

### 2. Maak of bewerk je eigen HTML-bestand
- Als jij `index.html` maakt of bijwerkt, plaats het bestand in de hoofdmap van je project (of in een submap als dat logisch is in jullie structuur).  
- Als je partner `about.html` maakt, laat die in een eigen branch (`feature/about-page`) werken.  

#### Minimale inhoud
Zorg dat elk HTML-bestand minimaal het volgende bevat:
1. **Twee titels** (bijv. `<h1>` en `<h2>`).  
2. **Vier paragrafen** met enige inhoud.  
3. **Twee knoppen** (met klassen als `btn btn-primary`, `btn btn-secondary`, etc.).  
4. Een **container** (`<div class="container">`) met een of twee `<div class="row">` en `<div class="col">`-elementen om de layout te structureren.  

Voorbeeld (schematisch):
```html
<!DOCTYPE html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Mijn Bootstrap Pagina</title>
  <!-- Koppel hier de Bootstrap CDN -->
</head>
<body>
  <div class="container">
    <h1>Hoofdtitel</h1>
    <h2>Ondertitel</h2>
    <div class="row">
      <div class="col">
        <p>Hier komt paragraaf 1...</p>
        <p>Paragraaf 2...</p>
        <button class="btn btn-primary">Klik hier</button>
      </div>
      <div class="col">
        <p>Paragraaf 3...</p>
        <p>Paragraaf 4...</p>
        <button class="btn btn-secondary">Meer info</button>
      </div>
    </div>
  </div>

  <!-- Bootstrap JS (optioneel, voor interactieve componenten) -->
</body>
</html>
```

### 3. Voeg Bootstrap toe (indien nog niet gebeurd)
Als je nog geen **CDN-koppeling** hebt toegevoegd in de `<head>` van je bestand, doe dat dan nu:

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  integrity="sha384-..."
  crossorigin="anonymous"
/>
```

### 4. Commit en push
1. **Maak een commit** met een duidelijk bericht
2. **Push** je branch naar GitHub

### 5. Maak een Pull Request (PR)
- Ga naar de GitHub-pagina van je repository en maak een **Pull Request** aan van jouw branch naar `main`.  
- Vraag je partner om feedback te geven op je wijzigingen.  

### 6. Merge jullie werk
- Nadat jij en je partner elkaars Pull Requests hebben **goedgekeurd**, kun je beide branches mergen naar de `main`.  
- Haal vervolgens **lokaal** de wijzigingen binnen.

### 7. Controleer en test
- Open de `index.html` en `about.html` lokaal in de browser om te zien of alles goed werkt.  
- Pas desgewenst extra utility-classes toe (zoals `text-center`, `m-3`, `p-4` enz.) om de pagina’s verder op te maken.  

<div class="note protip">
<p>Protip: Door elk je eigen branch te gebruiken, voorkom je dat jullie in dezelfde bestanden werken en mogelijke merge-conflicten veroorzaken. Houd je commit-berichten kort en duidelijk!</p>
</div>

