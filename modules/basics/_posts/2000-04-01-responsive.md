---
title: Bootstrap Grid en Responsive Layout
---

<div class="header1" id="grid" markdown="1">
# Bootstrap Grid en Responsive Layout
</div>

Het **Grid-systeem** vormt de kern van Bootstrap. Hiermee kun je je webpagina’s overzichtelijk indelen in rijen en kolommen, die automatisch **responsief** zijn voor verschillende schermgroottes. In dit hoofdstuk ontdek je hoe je de classes `container`, `row` en `col` gebruikt en hoe breakpoints (zoals `sm`, `md`, `lg`, etc.) werken om je layout flexibel te houden.

---

<div class="header2" markdown="1">
## Container, Row en Col classes
</div>

### De `container`
In Bootstrap start je layout vaak met een `<div class="container">`. Deze container zorgt ervoor dat je inhoud mooi uitgelijnd is en in het midden van het scherm komt te staan bij grotere schermen. Er zijn twee varianten:

1. **`.container`**  
   - Heeft vaste breedtes bij specifieke schermformaten.  
   - Maakt de inhoud gecentreerd op grotere schermen.  

2. **`.container-fluid`**  
   - Gebruikt altijd de **volledige breedte** van het scherm, ongeacht de viewport-grootte.  

Gebruik `.container` wanneer je wat meer witruimte links en rechts wilt hebben, en `.container-fluid` als je graag de volle breedte benut.

### De `row`
Binnen een container gebruik je meestal een `<div class="row">` om een rij te definiëren. Deze rij verdeelt de beschikbare ruimte vervolgens in **kolommen**. Stel je de ‘row’ voor als een horizontale band waarin je meerdere kolommen naast elkaar kunt plaatsen.

### De `col`
Binnen elke `row` maak je een of meerdere kolommen met `<div class="col">`. In zijn meest eenvoudige vorm verdeelt Bootstrap de ruimte van de rij gelijkmatig over de aanwezige kolommen.

**Voorbeeld:**

```html
<div class="container">
  <div class="row">
    <div class="col bg-light border">Kolom 1</div>
    <div class="col bg-light border">Kolom 2</div>
    <div class="col bg-light border">Kolom 3</div>
  </div>
</div>
```

In dit voorbeeld worden **drie kolommen** gemaakt die elk evenveel ruimte innemen. Met behulp van verschillende **breakpoints** (zoals `col-md-4`) kun je aangeven dat de kolommen er anders uitzien op verschillende schermformaten. Dat bespreken we in het volgende onderdeel.


<div class="note protip">
<p>Protip: Je kunt het aantal kolommen in een row onbeperkt uitbreiden. Gebruik <code>bg-light</code>, <code>border</code> en <code>p-3</code> in het begin om de kolommen visueel duidelijk af te bakenen tijdens het testen.</p>
</div>


---

<div class="header2" markdown="1">
## Breakpoints en responsive design
</div>

Bootstrap werkt met een **mobile-first** benadering en hanteert standaard vijf belangrijke breakpoints:

| Breakpoint | Class prefix | Schermbreedte (min)  |
|------------|------------- |----------------------|
| Extra small | *(geen prefix, bijv. `col-`)* | < 576px  |
| Small       | `-sm-`       | ≥ 576px             |
| Medium      | `-md-`       | ≥ 768px             |
| Large       | `-lg-`       | ≥ 992px             |
| Extra large | `-xl-`       | ≥ 1200px            |
| XXL         | `-xxl-`      | ≥ 1400px            |

Met deze breakpoints kun je bepalen **vanaf** welke schermgrootte een bepaalde kolomverdeling moet gelden. Voorbeeld:

```html
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6 col-lg-4 bg-light border">Kolom A</div>
    <div class="col-12 col-md-6 col-lg-4 bg-light border">Kolom B</div>
    <div class="col-12 col-lg-4 bg-light border">Kolom C</div>
  </div>
</div>
```

- **`col-12`**: Op kleine schermen (extra small) nemen de kolommen de volle breedte in en komen ze dus **onder elkaar**.  
- **`col-md-6`**: Vanaf medium (≥768px) delen Kolom A en B de rij elk voor de helft, terwijl Kolom C op een nieuwe regel zou komen omdat die alleen `col-12` heeft voor md.  
- **`col-lg-4`**: Vanaf large (≥992px) heeft elke kolom 4 kolombreedtes, en passen er dus precies **drie kolommen** naast elkaar.  

Zo kun je stap voor stap je layout verfijnen voor verschillende resoluties. In de tweede helft van dit hoofdstuk kijken we nog dieper naar het Grid-systeem en leer je hoe je rijen en kolommen kunt combineren voor meer complexe layouts.

<div class="header2" markdown="1">
## Responsieve opbouw van de homepage
</div>

Nu je de basis van het Grid-systeem kent, kun je een homepage (of welke hoofdpagina dan ook) bouwen die zich aanpast aan verschillende schermgroottes. Een klassieke structuur is:

1. **Header** – bovenaan de pagina, vaak met een navigatiebalk (navbar) en titel.  
2. **Main** – het hoofdgedeelte van de pagina, met de belangrijkste content.  
3. **Footer** – een voettekst met contactinfo, copyright, of andere links.  

Met Bootstrap kun je deze onderdelen verdelen in rijen (`row`) en kolommen (`col`). Je kunt zelfs sections binnen de “Main” maken om content logisch op te splitsen.

#### Voorbeeld van een basisstructuur

```html
<div class="container">
  <!-- Header -->
  <header class="row mb-4">
    <div class="col bg-primary text-white py-3">
      <h1 class="text-center">Mijn Website</h1>
    </div>
  </header>

  <!-- Main content -->
  <main class="row">
    <!-- Linkerkolom / hoofdkolom -->
    <div class="col-12 col-md-8 bg-light p-3">
      <h2>Belangrijkste content</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p>
    </div>
    <!-- Rechterkolom / sidebar -->
    <aside class="col-12 col-md-4 bg-secondary text-white p-3">
      <h3>Sidebar</h3>
      <p>In deze kolom kun je extra info of links kwijt.</p>
    </aside>
  </main>

  <!-- Footer -->
  <footer class="row mt-4">
    <div class="col bg-dark text-white text-center py-2">
      <p>&copy; 2025 - Jouw Naam</p>
    </div>
  </footer>
</div>
```

- **Header**: Een enkele kolom die zich over de volle breedte uitstrekt (aangegeven door `col` in de `row`).  
- **Main**: Op kleine schermen (door `col-12`) neemt elk blok de volledige breedte in. Vanaf medium schermen (`col-md-8` / `col-md-4`) wordt het verdeeld in een 2/3 en 1/3-opzet.  
- **Footer**: Net als de header, één kolom over de volle breedte.  

Deze structuur maakt je pagina meteen responsief. Probeer vooral de breakpoints (`col-sm-`, `col-md-`, `col-lg-`) uit om te zien welke layout het beste past bij jouw inhoud.

<div class="note protip">
<p>Protip: Wil je nog meer ruimte tussen je elementen? Voeg <code>my-4</code> (margin-top en margin-bottom) of <code>py-3</code> (padding-top en padding-bottom) toe aan de rijen/kolommen.</p>
</div>

---

<div class="header2" markdown="1">
## Oefening: eenvoudige indeling met het grid (header, main, footer)
</div>

In deze oefening ga je, samen met je partner, een eenvoudige responsive indeling maken voor jullie bestaande GitHub-project. We werken dus voort op de pagina’s die jullie eerder al hebben aangemaakt (bijvoorbeeld `index.html` en `about.html`).

### Doel van de oefening
- Een homepage (bijv. `index.html`) opbouwen met **header**, **main** en **footer** die responsief zijn.  
- Werken met het **Bootstrap Grid** en breakpoints, zodat onderdelen anders worden ingedeeld op mobiel vs. desktop.  
- Opnieuw samen oefenen met **branches** en het “pull request”-proces via GitHub.

### Stappenplan

1. **Branch voor je layout**  
   - Bespreek met je partner wie welke pagina bijwerkt.  
   - Maak een nieuwe branch, bijvoorbeeld `feature/responsive-index`, waar je de layout van `index.html` aanpast.  
   - Je partner kan eventueel een eigen branch maken voor `about.html`, of meewerken aan dezelfde branch.

2. **Voeg een header en footer toe**  
   - Zorg in de `<body>` van je `index.html` voor een `header` en een `footer`, elk in een eigen `row`.  
   - Maak hierbinnen een `col` die de volledige breedte inneemt (bijv. `<div class="col">`).  
   - Geef je header- en footer-rijen eventueel een **achtergrondkleur** (met `bg-primary`, `bg-dark`, etc.) en pas de tekstkleur aan (met `text-white`).

3. **Voeg een main-gedeelte toe**  
   - Creëer een `<main class="row">`-sectie.  
   - Voor de hoofdcontent kun je één kolom gebruiken (`<div class="col-12 col-md-8">`) en voor de sidebar (optioneel) `<div class="col-12 col-md-4">`.  
   - Vul beide kolommen met content (Je kan chatGPT gebruiken om die te genereren) en geef ze een lichte achtergrond (`bg-light`, `bg-secondary`, etc.) om het verschil te zien.

4. **Experimenteer met breakpoints**  
   - Speel met `col-sm-`, `col-md-` en `col-lg-` om te zien hoe de indeling verandert.  
   - Voeg wat marge of padding toe via **utility classes** (`mt-3`, `p-3`, etc.) om de layout te verfijnen.

5. **Commit en push**  
   - Commit de wijzigingen met een duidelijke boodschap, zoals "Maak responsive layout met header, main, en footer"
   - Maak een **Pull Request** aan op GitHub en laat je partner de code reviewen.

6. **Samenvoegen en testen**  
   - Merge de branch naar `main` zodra de review is goedgekeurd.  
   - Iedereen in het team haalt de laatste versie binnen.
   - Test de pagina op verschillende schermformaten of door je browser te verkleinen.


<div class="note protip">
<p>Protip: Mocht je later een echte navigatiebalk willen, kijk dan in de Bootstrap-documentatie bij <em>Components &gt; Navbar</em>. Dit kan je header nog professioneler maken.</p>
</div>

