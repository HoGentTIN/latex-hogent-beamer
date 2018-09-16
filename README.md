# LaTeX presentatiesjabloon HOGENT

In deze repo vind je een LaTeX-sjabloon voor een Beamer-presentatie in de huisstijl van HOGENT (zoals ingevoerd in academiejaar 2018-2019).

## Vereisten

- Voor het gebruik van dit sjabloon heb je de volgende lettertypes nodig:
    - [Montserrat](https://fonts.google.com/specimen/Montserrat). Dit is het standaard-lettertype van de HOGENT huisstijl (i.h.b. de gewichten Regular, Semibold en Extrabold)
    - [Code Pro Black](https://www.dafontfree.net/freefonts-code-pro-black-f62435.htm). Dit lettertype wordt gebruikt voor de "fotoletters" (zie verder).
    - [Fira Code](https://github.com/tonsky/FiraCode). De HOGENT huisstijl specifieert geen lettertype voor monogespatieerde tekst, zoals gebruikt bij `\texttt` of in de `verbatim`-omgeving. Dit sjabloon gebruikt Fira Code, een lettertype met ligaturen voor programmacode.
- Omdat het sjabloon werkt met TrueType-lettertypes, moet je de presentatie compileren met **XeTeX** of LuaTex.
    - In TexStudio: Options > Configure Texstudio > Build
        - Default compiler: _txs:///xelatex_
        - PDF Chain: _txs:///xelatex | txs:///view-pdf_

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

Deze stijl laat toe elke "glyph" van het lettertype te gebruiken in combinatie met elke gewenste afbeelding via het commando `\imgletter`. Een voorbeeld met de letter M:

```latex
\imgletter{img/afbeelding.png}{M}
```

De letter blijft op de achtergrond, zodat er nog tekst voor kan geplaatst worden, bv.


```latex
\begin{frame}
  \imgletter{img/blurred-background-cellphone-coffee-842554.jpg}{H}
  {\huge \textbf{Voorbeeld van tekst door een afbeelding}}
\end{frame}
```

## Gekende Problemen

- Op dit moment wordt voor wiskundige formules het Computer Modern font gebruikt, in plaats van Montserrat, of in elk geval een schreefloos lettertype.
- De positionering van de "fotoletters" is nog niet optimaal.
- De stijl heeft geen paginanummering.

## Vragen, problemen, verbeteringen

Heb je vragen of problemen bij het gebruik van dit sjabloon, of heb je ideeën voor verbetering? Laat het weten via de Issues.

Concrete voorstellen tot verbetering zijn ook ten zeerste welkom en die kan je via een Pull Request indienen.
