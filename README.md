# SjabloonGIPWebsite

## Responsive Menu

```html
        <li class="icon">
            <a href="javascript:void(0);" onclick="myFunction()">&#9776;</a>
        </li>
```

Verwijst naar het icoon dat je gebruikt om navigatie knoppen uit te schuiven.

css class ```ul.topnav``` verwijderd de margin en padding. Het geeft het menu een background-color

```ul.topnav li {float: left;}``` zorgt ervoor dat de list items mooi naast elkaar staan.

```ul.topnav li a:hover {backgorund-color: #555;}``` zet de achtergrond kleur op een andere kleur wanneer je met je muis over de knop hovert. (hover-animatie)

```ul.topnav li.icon {display: none;}``` verstopt het list item dat de navigatie knoppen opent en sluit bij een klein scherm.

#### Media Queries

Wanneer je dingen wil laten veranderen aan bepaalde voorwaarden van een apparaat kan je Media Queries gebruiken.

Bijvoorbeeld de hoogte en breedte van een apparaat, of het in landscape of portrait mode staat, de resolutie, ...

Een voorbeeld is de achtergrond kleur van een website veranderen wanneer de minimum breedte lager dan 480px.

Wanneer je dan je browser kleiner maakt dan 480px zal de achtergrond kleur veranderen in de opgegeven kleur.

Je hebt meerdere value's zoals all, print, screen en speech.

Degene die ik heb gebruikt is screen. Dit wordt gebruikt voor de schermen van computers, tablets, ...

Meer info over Media Queries: http://www.w3schools.com/css/css3_mediaqueries.asp

```css
@media screen and (max-width:680px) {
  ul.topnav li:not(:first-child) {display: none;}
  ul.topnav li.icon {
    float: right;
    display: inline-block;
  }
}
```

Deze media querie hide alle list items die kleiner zijn dan 680px breed, behalve het eerste list item: home.

```css
@media screen and (max-width:680px) {
  ul.topnav.responsive {position: relative;}
  ul.topnav.responsive li.icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  ul.topnav.responsive li {
    float: none;
    display: inline;
  }
  ul.topnav.responsive li a {
    display: block;
    text-align: left;
  }
}
```

Deze media querie zorgt ervoor dat de "responsive" class wordt toegevoegd wanneer er op het icoontje wordt geklikt. (als de maximum breedte lager is dan 680px)

de functie toggleMenu veranderd de klasnaam met responsive erbij of niet, zodat het menu uitgeschoven kan worden op kleine schermen.

## Welkomsbericht met flexbox

De class column-layout is een div waarin 2 andere divs zitten, main-column en sidebar-two.

Bij de opmaak kan je de breedte van de div kiezen, de kleur, margin, ... de ```display: flex``` typ je als e flexbox wilt gebruiken.

Daarna kan je in de andere div's bij opmaak ```flex: 1``` typen. De 1 is dan plaats gebruiken voor het object, als je 2 neemt neemt bv de tekst dubbel zo veel plaats in beslag. De ```order: 1``` is in welke volgorde de divs horizontaal komen.