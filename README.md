# LaTeX presentatiesjabloon HOGENT

In deze repo vind je een LaTeX-sjabloon voor een Beamer-presentatie in de
huisstijl van HOGENT (zoals ingevoerd in academiejaar 2018-2019).

## Voorbeeld

Bekijk het voorbeelddocument voor inspiratie, en een zicht op de mogelijkheden:

- [HOGENT-voorbeeld.tex](HOGENT-voorbeeld.tex): LaTeX broncode
- [HOGENT-voorbeeld-wit.pdf](HOGENT-voorbeeld-wit.pdf): resultaat, witte achtergrond
- [HOGENT-voorbeeld-zwart.pdf](HOGENT-voorbeeld-zwart.pdf): resultaat, zwarte achtergrond

## Kleuren

Er zijn twee kleurenschema's voorzien:

- `hgwhite`: zwarte tekst op witte achtergrond
- `hgblack`: witte tekst op zwarte achtergrond

Om één van de twee te selecteren, voeg je volgende code toe in je `.tex`-bestand:

```latex
\usetheme{hogent}
\usecolortheme{hgwhite} % witte achtergrond, zwarte tekst
```

De kleuren uit het pallet van de HOGENT huisstijl zijn ook bruikbaar in je presentatie onder volgende namen:

| Naam         | RGB         |
| :--          | :--         |
| hgdarkgreen  | 22/176/165  |
| hgpink       | 241/157/160 |
| hgochre      | 250/188/50  |
| hgorange     | 239/135/103 |
| hgpurple     | 187/144/189 |
| hgblue       | 76/162/213  |
| hglightgreen | 165/202/114 |
| hgbrown      | 216/176/131 |
| hggrey       | 195/187/175 |
| hgyellow     | 244/222/0   |

Omdat Markdown niet toelaat kleuren te tonen, bekijk je best <https://hnet.hogent.be/themas/communicatie/huisstijl-logo-s-en-sjablonen/kleurgebruik/> voor voorbeelden, of bijgevoegd voorbeeld.

## "Fotoletters"

Eén van de typische elementen van de HOGENT huisstijl zijn de grote letters (in lettertype Code Pro Black) ingevuld met een foto. Het Powerpoint-sjabloon dat door de dienst communicatie werd gepubliceerd, bevat één voorbeeld hiervan, met de letter H. Daar is echter een "workaround" gebruikt in die zin dat het effect bekomen is door de letter in een afbeelding te plakken en die daar transparant te maken. Dat betekent dat in het Powerpoint-sjabloon ook enkel de H kan gebruikt worden.

Deze stijl laat toe elke "glyph" van het lettertype te gebruiken in combinatie met elke gewenste afbeelding via een achtergrondsjabloon. Een voorbeeld met de letter H:

```latex
\setbeamertemplate{background}[imgletter]{img/example.jpg}{H}
```

De letter blijft op de achtergrond, zodat er nog tekst voor kan geplaatst worden, bv.

```latex
{
\setbeamertemplate{background}[imgletter]{img/example.jpg}{H}
\begin{frame}
  {\huge \textbf{Voorbeeld van tekst door een afbeelding}}
\end{frame}
}
```

Wanneer het `\setbeamertemplate`-commando uitgevoerd wordt, zullen in principe alle volgende slides dezelfde achtergrond krijgen. De accolades vooraan en achteraan in het vorige voorbeeld zorgen er voor dat de achtergrond enkel wordt toegepast op deze ene slide.

## Gekende Problemen

- Op dit moment wordt voor wiskundige formules het Computer Modern font gebruikt, in plaats van Montserrat, of in elk geval een schreefloos lettertype.

## Vragen, problemen, verbeteringen

Heb je vragen of problemen bij het gebruik van dit sjabloon, of heb je ideeën voor verbetering? Laat het weten via de Issues.

Concrete voorstellen tot verbetering zijn ook ten zeerste welkom en die kan je via een Pull Request indienen.
