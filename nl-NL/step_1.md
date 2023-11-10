De **micro:bit** is een kleine computer die je kunt gebruiken om te communiceren met de wereld om je heen.

Dit project helpt je te **ontdekken** wat de **micro:bit** kan doen.

### Wat ga je maken

Verveel je je wel eens en weet je niet wat je wil gaan doen? Je kunt de micro:bit gebruiken om je te helpen bij het beslissen!

In dit project ga je een **hobby kiezer** maken.

Je gaat:
+ De micro:bit laten oplichten en afbeeldingen weergeven
+ Willekeurige getallen gebruiken om keuzes te maken
+ Use `if`{:class='microbitlogic'} blocks to control which images are displayed
+ Het logo of een knop gebruiken om het scherm te wissen

--- no-print ---

### Afspelen ▶️

--- task ---

Wat gebeurt er als je de micro:bit **schudt**? Wat gebeurt er als je op het **logo** klikt?

<div style="position:relative;height:100%;padding-bottom:125%;padding-top:0;overflow:hidden;">
<iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---run?id=S47133-08356-20146-01355" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe>
</div>

--- /task ---

--- /no-print ---

### MakeCode openen

Om je micro:bit-project te maken, moet je eerst de MakeCode-editor openen.

--- task ---

Open de MakeCode editor op [makecode.microbit.org](https://makecode.microbit.org)

--- collapse ---

---
title: Offline versie van de editor
---

Er is ook een [downloadbare versie van de MakeCode editor](https://makecode.microbit.org/offline-app).

--- /collapse ---

--- /task ---

Zodra de editor is geopend, moet je een nieuw project aanmaken en je project een naam geven.

--- task ---

Klik op de knop **Nieuw Project**.

<img src="images/new-project-button.png" alt="De knop Nieuw project in MakeCode." width="250" />

--- /task ---

--- task ---

Geef je nieuwe project de naam `Kies een hobby` en klik op **Aanmaken**.

<img src="images/new-project.png" alt="De naam 'Kies een hobby' geschreven in het dialoogvenster een project maken." width="300" />

**Tip:** Om het makkelijker te maken om je project later terug te vinden, geef het een logische naam die gerelateerd is aan de activiteit die je aan doen bent.

--- /task ---

### De MakeCode editor

De **MakeCode editor** - gemaakt door de micro:bit Foundation- bevat alles wat je nodig hebt om te beginnen met coderen op de micro:bit.

![De MakeCode editor venster](images/makecode-tour.png)

Aan de linkerkant is er een **simulator**. Dit bevat een virtuele micro:bit die je kunt gebruiken om je code te testen!

Het heeft alle functies en knoppen die je op een V2 micro:bit vindt, inclusief:
+ LED display
+ Luidspreker
+ Microfoon
+ Invoerknoppen
    + A
    + B
    + Logo

In het midden staat het **blokken paneel**, dat ingedeeld is per kleur en je toegang geeft tot de verschillende codeblokken.

Aan de rechterkant is er het **code editor paneel**, waar je blokken naar toe sleept om je programma te maken.

The MakeCode editor panel already contains two blocks: `on start`{:class='microbitbasic'} and `forever`{:class='microbitbasic'}.

### Toon pictogram

You will use the `forever`{:class='microbitbasic'} block to see how the LEDs on the simulator work.

--- task ---

Click on the `Basic`{:class='microbitbasic'} block menu in the blocks panel. Dit zal uitklappen om de beschikbare blokken te laten zien.

<img src="images/basic-blocks.png" alt="Het basisblokmenu met het 'toon pictogram' blok geaccentueerd." width="300" />

Drag the `show icon`{:class='microbitbasic'} block and drop it **inside** the `forever`{:class='microbitbasic'} block. Het moet als een puzzelstuk op zijn plaats passen.

```microbit
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})
```

--- /task ---

--- task ---

Klik op de pijl omlaag op het Toon pictogram blok en kies een pictogram.

<img src="images/show-icons.png" alt="Het Toon pictogram menu uitgeklapt met alle beschikbare iconen." width="300" />

![]()

--- /task ---

--- task ---

**Test:** Klik op de afspeelknop van de simulator. Het LED-scherm moet oplichten, met het pictogram dat je gekozen hebt.

In dit voorbeeld hebben we het `X` pictogram gekozen.

![De microbitsimulator geeft een 'X'-pictogram weer op de LED's, terwijl de codeblokken aan de rechterkant worden weergegeven.](images/led-display.png)

Goed gedaan! Je hebt de micro:bit iets laten doen!

--- /task ---

### Kies je hobby's

--- task ---

Kies drie hobby's of activiteiten die je graag doet in je vrije tijd.

Hier zijn een paar ideeën om je op weg te helpen:
+ 🎮 Gamen
+ 📚 Lezen
+ 🧁 Bakken
+ 📺 Tv kijken
+ 🚶‍♀️ Wandelen
+ 🏐 Een sport beoefenen
+ 🎨 Tekenen

--- /task ---

--- task ---

Verander je pictogram in een die je eerste hobby vertegenwoordigt.

We hebben een Pac-Man spook gekozen voor gamen! 👻

--- /task ---

### Maak een variabele

Je gebruikt drie verschillende pictogrammen om drie verschillende hobby's weer te geven.

Elke hobby wordt aan een getal gekoppeld en je maakt een variabele zodat je kunt veranderen welke hobby wordt weergegeven.

--- task ---

Open the `Variables`{:class='microbitvariables'} menu, and click **Make a variable**.

<img src="images/variable-menu.png" alt="Het variabelenblokmenu wordt geopend met de knop 'Maak een variabele' gemarkeerd." width="350" />

--- /task ---

--- task ---

Noem de nieuwe variabele `activiteit` en klik vervolgens op de knop **OK**.

<img src="images/variable-name.png" alt="Het dialoogvenster 'Voer een nieuwe variabelenaam in', met de naam 'activiteit' in het vak." width="350" />

--- /task ---

Je zult nu zien dat er nieuwe blokken beschikbaar zijn. These blocks let you set, change, or use the value stored in the `activity`{:class='microbitvariables'} variable.

<img src="images/variable-blocks.png" alt="Het variabelen blokmenu - met nieuwe blokken om de waarde in te stellen, te wijzigen en de waarde van de 'activiteit' variabele te gebruiken in je code." width="350" />

--- task ---

Drag the `set`{:class='microbitvariables'} block inside the `on start`{:class='microbitbasic'} block.

```microbit
let activity = 0
```

--- /task ---

### Welke hobby wordt weergegeven?

When `activity`{:class='microbitvariables'} is set to `1`, the icon for your first hobby should display. When `activity`{:class='microbitvariables'} is set to `2`, the icon for the next hobby should display.

Je gebruikt hiervoor `als... dan` blokken.

--- task ---

Open the `Logic`{:class='microbitlogic'} menu and choose the `if`{:class='microbitlogic'} block.

<img src="images/if-block.png" alt="Het Logisch blokmenu geopend met het 'als' blok gemarkeerd." width="350" />

Drag the `if`{:class='microbitlogic'} block inside the `forever`{:class='microbitbasic'} loop block. Place it **above** your `show icon`{:class='microbitbasic'} block.

```microbit
basic.forever(function () {
    if (true) {

    }
    basic.showIcon(IconNames.Ghost)
})
```

--- /task ---

--- task ---

From the `Logic`{:class='microbitlogic'} menu, drag out the comparison block `0 = 0`{:class='microbitlogic'}.

<img src="images/condition-block.png" alt="Het Logisch blokmenu met het vergelijkingsblok '0=0' gemarkeerd." width="350" />

Place it inside the `true` space within the `if`{:class='microbitlogic'} block.

```microbit
basic.forever(function () {
    if (0 == 0) {

    }
    basic.showIcon(IconNames.Ghost)
})
```

--- /task ---

--- task ---

Go back to the `Variables`{:class='microbitvariables'} menu and pick the small block that says `activity`{:class='microbitvariables'}.

Sleep dit blok naar de **eerste** `0` in je nieuwe vergelijkingsblok.

Verander de tweede `0` in `1`.

```microbit
basic.forever(function () {
    let activity = 0
    if (activity == 1) {

    }
    basic.showIcon(IconNames.Ghost)
})
```

--- /task ---

--- task ---

Drag your `show icon`{:class='microbitbasic'} block **inside** the `if`{:class='microbitlogic'} block.

```microbit
basic.forever(function () {
    let activity = 0
    if (activity == 1) {
        basic.showIcon(IconNames.Ghost)
    }
})
```

--- /task ---

--- task ---

**Test:** Voer je programma uit:

Als je een wijziging in een codeblok aanbrengt, wordt de simulator opnieuw opgestart.

Het is je misschien opgevallen dat er na je laatste wijziging niets op de LED's verscheen.

Find your `set`{:class='microbitvariables'} block again. Hint: it's inside the `on start`{:class='microbitbasic'} block.

**Verander** de `0` naar `1`.

**Test opnieuw**:

Wanneer de simulator na de laatste wijziging opnieuw opstart, zou het pictogram moeten verschijnen.

Zorg ervoor dat je **de waarde van de activiteitsvariabele weer op `0` zet**, zodat deze juist is ingesteld voor de volgende stap.

--- /task ---

### Voeg meer hobby's toe

To add more hobby options to your program, you will need to add more conditions to your `if`{:class='microbitlogic'} block.

--- task ---

Klik op het `+` -symbool onderaan het `als` -blok. Hierdoor wordt een `anders` blok gemaakt.

<img src="images/if-plus-icon.png" alt="Het + symbool in de linker onderhoek van het 'als blok' in de 'de hele tijd' lus." width="250" />

--- /task ---

--- task ---

Click on the `+` symbol below the `else`{:class='microbitlogic'}. This will create an `else if`{:class='microbitlogic'}. Do this one more time so you have two `else if`{:class='microbitlogic'} blocks.

--- /task ---

--- task ---

Now click on the `-` symbol next to the `else`{:class='microbitlogic'} to remove it.

![Met het + symbool worden een "anders" en twee " anders als" aan een voorwaarde toegevoegd. Vervolgens wordt de als verwijderd door op het - symbool ernaast te klikken.](images/adding-ifs.gif)

--- /task ---

--- task ---

Right click on the whole `=`{:class='microbitlogic'} block in the first `if`{:class='microbitlogic'} block.

Klik net links van de activiteitsvariabele, of net rechts van de waarde `0`, om er zeker van te zijn dat je het hele blok selecteert.

Klik op **Dupliceren** om een kopie te maken.

Drag the duplicated `=`{:class='microbitlogic'} block into the first `else if`{:class='microbitlogic'} block. Verander vervolgens het getal `1` in een `2`.

![Als je met de rechtermuisknop op het vergelijkingsblok in het eerste blok klikt, verschijnt er een menu. Er wordt op de eerste optie, 'Dupliceren', geklikt. Een nieuwe versie van het vergelijkingsblok wordt gemaakt en naar de eerste anders als blok gesleept.](images/duplicate-comparison.gif)

--- /task ---

--- task ---

Duplicate the `=`{:class='microbitlogic'} block one more time and drag it into the second `else if`{:class='microbitlogic'} block. Verander vervolgens het nummer naar `3`.

```microbit
basic.forever(function () {
    let activity = 0
    if (activity == 1) {
        basic.showIcon(IconNames.Ghost)
    } else if (activity == 2) {

    } else if (activity == 3) {

    }
})
```

--- /task ---

### Geef je hobby's vorm

--- task ---

**Kies** nog twee afbeeldingen om je hobby's weer te geven.

You can use the `show icon`{:class='microbitbasic'} block or create your own icon using the `show leds`{:class='microbitbasic'} block.

--- collapse ---

---
title: Gebruik het toon lichtjes blok
---

From the `Basic`{:class='microbitbasic'} menu, drag the `show leds`{:class='microbitbasic'} block inside an `else if`{:class='microbitlogic'} block.

<img src="images/show-leds.png" alt="Het basismenu met het 'toon lichtjes'-blok gemarkeerd." width="350" />

Je kunt op elk van de vierkanten klikken om te kiezen welke je wilt laten oplichten. Witte vierkantjes worden verlicht op de micro:bit.

<img src="images/draw-icon.png" alt="Het 'toon lichtjes' blok met een smiley gemaakt van witte vierkanten." width="350" />

--- /collapse ---

--- /task ---

### Kies een willekeurige hobby

**Stel** de micro:bit in om een willekeurige hobby te kiezen wanneer je hem schudt.

--- task ---

Drag the `on shake`{:class='microbitinput'} block from the `Input`{:class='microbitinput'} menu.

<img src="images/on-shake.png" alt="Het invoermenu met het 'bij schudden' blok gemarkeerd." width="350" />

--- /task ---

--- task ---

From the `Variables`{:class='microbitvariables'} menu, drag the `set`{:class='microbitvariables'} block inside the `on shake`{:class='microbitinput'} block.

--- /task ---

--- task ---

From the `Math`{:class='microbitmath'} menu, drag the `pick random`{:class='microbitmath'} block to the `0` of the `set`{:class='microbitvariables'} block.

<img src="images/pick-random.png" alt="Het Rekenen menu met het blok 'kies willekeurig 0 tot 10' gemarkeerd." width="350" />

Verander de getallen `0 tot 10` in `1 tot 3`.

```microbit
let activity = 0
input.onGesture(Gesture.Shake, function () {
    activity = randint(1, 3)
})
```

--- /task ---

### Het scherm wissen

Gebruik het logo (V2) of een knop (V1) om de LED's uit te schakelen.

--- task ---

Drag the `on logo pressed`{:class='microbitinput'} block from the `Input`{:class='microbitinput'} menu.

<img src="images/onlogo-pressed.png" alt="Het invoermenu met het 'bij logo ingedrukt' blok gemarkeerd." width="350" />

--- collapse ---

---
title: V1 micro:bit-gebruikers
---

De logo-invoer is alleen beschikbaar op de V2 micro:bit.

For the V1 micro:bit, use the `on button`{:class='microbitinput'} block from the `Input`{:class='microbitinput'} menu.

<img src="images/button-a.png" alt="Het invoermenu met het 'wanneer knop A wordt ingedrukt' blok gemarkeerd." width="350" />

--- /collapse ---

--- /task ---

--- task ---

Drag the `clear screen`{:class='microbitbasic'} block from the `Basic`{:class='microbitbasic'} menu and place it inside the `on logo pressed`{:class='microbitinput'} block (or the `on button`{:class='microbitinput'} block for V1).

```microbit
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    basic.clearScreen()
})
```

--- /task ---

--- task ---

Now drag the `set`{:class='microbitvariables'} block from the `Variables`{:class='microbitvariables'} menu and place it below the `clear screen`{:class='microbitbasic'} block.

```microbit
let activity = 0
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    basic.clearScreen()
    activity = 0
})
```

--- /task ---

--- task ---

**Test:** Voer je programma uit:

**Klik** op de schudknop op de simulator om een willekeurige hobby te kiezen.

**Gebruik** het logo (of Knop A op de V1 micro:bit) om ervoor te zorgen dat het scherm wordt gewist.

--- /task ---

--- task ---

Download je code en test hem op een echte micro:bit!

[[[download-to-microbit]]]

Wanneer je jouw programma hebt gedownload naar jouw micro:bit, zal het onmiddellijk worden uitgevoerd.

**Test**: Je zou telkens een willekeurig pictogram moeten zien als je de micro:bit schudt.

--- /task ---

[[[microbit-share]]]

### Completed project

If you want to check your code you can can find [the completed project here](https://makecode.microbit.org/S47133-08356-20146-01355).

### Verbeter je project

Je kunt je project verbeteren om het nog aantrekkelijker te maken:

+ Voeg meer hobby's toe, zodat je uit een groter assortiment kunt kiezen.

Vergeet niet om:
  + Een ander symbool toe te voegen om elke nieuwe activiteit
  + Verhoog het aantal `anders als` blokken zodat je meer iconen kunt toevoegen
  + Verhoog het willekeurige bereik tot meer dan drie zodat het overeen komt met het aantal toegevoegde hobby's
