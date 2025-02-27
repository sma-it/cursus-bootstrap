---
title: Navigatie en Basiscomponenten
---

<div class="header1" id="nav-base-components" markdown="1">
# Navigatie en Basiscomponenten
</div>

In dit hoofdstuk leer je hoe je een **navigatiebalk** (navbar) toevoegt aan je Bootstrap-project en hoe je verschillende **basiscomponenten** (zoals buttons en badges) gebruikt om je website interactiever te maken. De **navbar** is een van de meestgebruikte onderdelen van Bootstrap en biedt je een kant-en-klare, responsieve structuur. Daarnaast ontdek je hoe je eenvoudig knoppen en opvallende labels (badges) kunt stylen.

---

<div class="header2" markdown="1">
## De Navbar-component: opbouw en styling
</div>

### 1. Basiselementen van de navbar
Een typische **Bootstrap Navbar** bestaat uit de volgende onderdelen:

- **`<nav class="navbar ...">`**: de container voor je hele navigatiebalk. Vaak gebruik je `navbar-expand-*` en `navbar-light` of `navbar-dark` om de stijl en uitklapbaarheid in te stellen.
- **`.navbar-brand`**: het logo of de titel van je website.
- **`.navbar-toggler`**: de knop die verschijnt op kleine schermen om het menu in- of uit te klappen.
- **`.navbar-collapse`**: de container waarin je navigatielinks staan. Deze collapse is verbergbaar op kleinere schermen.
- **`.nav-item`** en **`.nav-link`**: representeren de afzonderlijke menu-items en hun links.

### 2. Voorbeeld van een eenvoudige navbar
Hieronder zie je een voorbeeld van een **responsive** navbar. De navbar klapt uit boven de `md`-breakpoint (medium, 768px). Daaronder wordt hij ingeklapt en kan de gebruiker het menu openen via de `navbar-toggler`-knop.

```html
<nav class="navbar navbar-expand-md navbar-light bg-light">
  <div class="container">
    <a class="navbar-brand" href="#">
      MijnSite
    </a>
    <!-- Toggler (hamburgerknop) -->
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>

    <!-- Inklapbaar menu -->
    <div class="collapse navbar-collapse" id="mainNavbar">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Over Ons</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Diensten</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

**Toelichting**:

1. **`navbar-expand-md`**: de navbar breidt zich uit (is volledig zichtbaar) vanaf een schermbreedte van 768px en groter. Op kleinere schermen wordt hij ingeklapt.  
2. **`bg-light`** en **`navbar-light`**: de achtergrond is licht, en de tekst- en icoonkleur is donker.  
3. **`ms-auto`** (margin start auto) op de `<ul>` zorgt ervoor dat de navigatielinks naar de rechterkant worden geduwd.  
4. **`data-bs-toggle="collapse"`** en **`data-bs-target="#mainNavbar"`** zorgen ervoor dat de `navbar-toggler` de `<div>` met `id="mainNavbar"` kan in- en uitklappen.  

### 3. Kleur en styling aanpassen
- Met **`bg-light`**, **`bg-dark`**, **`navbar-light`** of **`navbar-dark`** kun je de kleuren snel wisselen.  
- Wil je een eigen kleur gebruiken? Dan kun je die toewijzen via custom CSS of via Bootstrap’s [theming opties](https://getbootstrap.com/docs/5.0/customize/color/).

<div class="note protip">
<p>Protip: Voor extra variatie kun je <code>bg-primary</code>, <code>bg-secondary</code> of een eigen klasse gebruiken in plaats van <code>bg-light</code>.</p>
</div>

---

<div class="header2" markdown="1">
## Buttons, badges en andere basiscomponenten
</div>

Naast navigatiebalken biedt Bootstrap tal van andere **basiscomponenten** die direct klaar zijn voor gebruik. Hier zoomen we in op **knoppen** (buttons) en **badges** (labels).

### 1. Buttons
Met Bootstrap maak je eenvoudig knoppen met verschillende stijlen en groottes. De basisklasse is `btn`, met daarnaast een **variatiereeks** zoals `btn-primary`, `btn-secondary`, `btn-success`, enz. 

**Voorbeeld**:
```html
<button class="btn btn-primary">Knop Primary</button>
<button class="btn btn-secondary">Knop Secondary</button>
<button class="btn btn-success">Knop Succes</button>
<button class="btn btn-danger">Knop Danger</button>
```

**Extra klassen**:
- **`btn-lg`** of **`btn-sm`** om de grootte van de knop aan te passen.  
- **`btn-outline-...`** (bijv. `btn-outline-primary`) voor een transparante achtergrond met een gekleurde rand.  

### 2. Badges
Een **badge** is een klein element waarmee je informatie kunt benadrukken, zoals het aantal meldingen of een nieuwe status. Plaats de klasse `badge` en een variatieklasse als `bg-primary` of `bg-success` om de kleur te bepalen.

**Voorbeeld**:
```html
<h1>Berichten <span class="badge bg-primary">3</span></h1>
<p>
  Nieuwe verzoeken: <span class="badge bg-success">2</span><br>
  Ongelezen berichten: <span class="badge bg-danger">5</span>
</p>
```

**Toepassingen**:
- Weergave van aantallen (bijv. aantal items in een winkelmandje).  
- Extra markering, zoals “Nieuw!” of “Populair!” bij producten of blogartikelen.  

```html
<div class="note protip">
<p>Protip: Combineer badges met knoppen of links om bijv. een <code>Notifications (3)</code> knop te maken. Je kunt ook de hulppagina van de Bootstrap-documentatie raadplegen voor meer <em>utility-classes</em>.</p>
</div>
```

### 3. Andere basiscomponenten
Bootstrap heeft veel meer te bieden dan alleen knoppen en badges. Denk aan:

- **Alerts** (`.alert .alert-danger`, `.alert-success`) om feedback of waarschuwingen te tonen.  
- **List groups** (lijsten met een speciale opmaak).  
- **Progress bars**.  

Je vindt deze allemaal in de [Components-sectie](https://getbootstrap.com/docs/5.0/components) van de Bootstrap-documentatie.  


<div class="header2" markdown="1">
## Praktische tips over uitlijning, marges en spacing (Utility Classes)
</div>

Naast de grotere **components** (zoals navbars en buttons) biedt Bootstrap een zeer uitgebreide set **utility classes** waarmee je snel de **uitlijning**, **marges** (margin) en **ruimte** (padding) van elementen kunt regelen. Zo hoef je niet elke keer in je eigen CSS te duiken.

### 1. Marges en padding
- **`m-<size>`**: voor margin (buitenste ruimte).  
- **`p-<size>`**: voor padding (binnenste ruimte).  

<small><em>Voorbeeld: `m-3` geeft een marge van “3” aan alle kanten van het element, `mt-2` geeft marge-top van “2” en `ms-4` geeft marge-links van “4”. (De s staat voor “start” – handig in RTL-contexten.)</em></small>

**Standaard-sizes** in Bootstrap: `0`, `1`, `2`, `3`, `4`, `5` (en soms `auto`). Hoe hoger het getal, hoe groter de marge/padding.

<div class="note protip">
<p>Protip: In plaats van <code>ml-3</code> (margin-left) gebruik je in Bootstrap 5 <code>ms-3</code>, omdat “start” rekening kan houden met rechts-naar-links talen.</p>
</div>

### 2. Tekst en uitlijning
- **`.text-start`**, **`.text-center`**, **`.text-end`**: lijnt tekst links, gecentreerd of rechts uit.  
- **`.fw-bold`** (font-weight bold), **`.fw-light`** (font-weight light) voor snelle typografieaanpassingen.  
- **`.text-uppercase`**, **`.text-lowercase`**, **`.text-capitalize`** om de teksttransformatie te regelen.

### 3. Weergave en positionering
- **`.d-none`**, **`.d-block`**, **`.d-inline-block`**: toggle de zichtbaarheid en weergavemodus van elementen.  
- **`.float-start`**, **`.float-end`** of **`.float-none`**: laat elementen links of rechts ‘floaten’.  
- **`.position-relative`**, **`.position-absolute`**: om elementen relatief of absoluut te positioneren.  

### 4. Snel een kleur geven
- **`.bg-primary`**, **`.bg-success`**, **`.bg-danger`**, etc. voor achtergrondkleuren.  
- **`.text-primary`**, **`.text-success`** voor tekstkleuren.  

In de [Bootstrap Utility Docs](https://getbootstrap.com/docs/5.0/utilities) vind je een **volledige lijst** met alle beschikbare klassen. Experimenteer gerust met de verschillende combinaties en ontdek hoe je layouts snel kunt verfijnen.

---

<div class="header2" markdown="1">
## Oefening: bouw een homepage met navbar en lay-out met card-elementen
</div>

In deze oefening ga je jouw website verder professionaliseren door een **navbar** te implementeren en de hoofdpagina in te delen met **cards** voor je content. 

### Doel van de oefening
- Een **navigatiebalk** toevoegen aan de homepage.  
- Gebruikmaken van het **Bootstrap Grid** en **card-componenten** om content gestructureerd te presenteren.  
- Verder oefenen met **utility classes** om uitlijning, marges en kleuren in te stellen.  
- Wederom samenwerken via GitHub (ieder in een eigen branch).

#### Stappenplan

1. **Maak een nieuwe branch**  
   - Bespreek met je partner wie welke pagina bijwerkt.  
   - Maak een nieuwe branch.
   - Je partner kan een eigen branch maken als die aan een andere pagina werkt, of jullie kunnen samen in dezelfde feature branch werken—maar overleg goed om merge-conflicten te voorkomen.

2. **Voeg de Navbar toe**  
   - Kopieer het basisvoorbeeld van de **navbar** uit de Bootstrap-documentatie of uit de voorbeelden in deze cursus.
   - Pas de klassen naar wens aan (`navbar-light bg-light`, `navbar-dark bg-primary`, enz.).
   - Voeg menu-items toe (bijv. links naar je homepage, about-pagina, contact-pagina).

3. **Maak een ‘cards’-sectie** in je homepage  
   - In je `index.html` (of welke hoofdpagina je gebruikt) maak je een `<section class="container my-4">`.  
   - Binnen deze container zet je een `<div class="row">`.  
   - Voeg 2 of 3 `col-12 col-md-4` kolommen toe. In elke kolom komt een Bootstrap-card:
     ```html
     <div class="card">
       <img src="https://via.placeholder.com/300" class="card-img-top" alt="...">
       <div class="card-body">
         <h5 class="card-title">Card titel</h5>
         <p class="card-text">Korte beschrijving van deze card.</p>
         <a href="#" class="btn btn-primary">Meer Info</a>
       </div>
     </div>
     ```

4. **Styling en spacing**  
   - Voeg `mt-3`, `mb-4`, `p-3`, etc. toe om de elementen netjes te plaatsen.  
   - Experimenteer met `.bg-light`, `.text-center` of `.fw-bold` om titels en paragrafen duidelijker te maken.

5. **Commit en push**  
   - Maak een commit en sync je changes.
   - Maak een Pull Request aan op GitHub en laat je partner feedback geven.

6. **Merge en test**  
   - Na goedkeuring merge je de branch in `main`.  
   - Haal de laatste wijzigingen binnen met `git pull origin main`.  
   - Open de pagina in je browser en kijk of de navbar en cards naar verwachting werken.  


<div class="note protip">
<p>Protip: Je kunt de <code>.row</code> en <code>.col</code>-klassen ook binnen je <em>.card-body</em> gebruiken voor een <em>extra</em> verdeling van content. Bezoek de <strong>Bootstrap Cards</strong>-documentatie om meer varianten te ontdekken (verticale kaarten, kaarten met een header of footer, enz.).</p>
</div>
