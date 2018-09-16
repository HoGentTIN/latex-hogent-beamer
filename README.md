# HOGENT LaTeX sjabloon voor een presentatie

In deze repo vind je een LaTeX-sjabloon voor een Beamer-presentatie in de huisstijl van HOGENT (zoals ingevoerd in academiejaar 2018-2019).

## Vereisten

- Voor het gebruik van dit sjabloon heb je de volgende lettertypes nodig:
    - [Montserrat](https://fonts.google.com/specimen/Montserrat). Dit is het standaard-lettertype van de HOGENT huisstijl (i.h.b. de gewichten Regular, Semibold en Extrabold)
    - [Fira Code](https://github.com/tonsky/FiraCode). De HOGENT huisstijl heeft geen lettertype voor monogespatieerde tekst gespecifieerd, zoals gebruikt bij `\texttt` of in de `verbatim`-omgeving. Fira Code is een lettertype met ligaturen voor programmacode.
- Omdat het sjabloon werkt met TrueType-lettertypes, moet je de presentatie compileren met **XeTeX** of LuaTex.
    - In TexStudio: Options > Configure Texstudio > Build
        - Default compiler: _txs:///xelatex_
        - PDF Chain: _txs:///xelatex | txs:///view-pdf_

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

Omdat Markdown niet toelaat kleuren te tonen, bekijk je best <https://hnet.hogent.be/themas/communicatie/huisstijl-logo-s-en-sjablonen/kleurgebruik/> voor voorbeelden.
