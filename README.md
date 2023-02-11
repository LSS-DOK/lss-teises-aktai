# LŠS dokumentacija `markdown` (.md) formatu

Šioje repozitorijoje rasite Lietuvos šaulių sąjungos dokumentacijos kopijas [.md](https://daringfireball.net/projects/markdown/syntax) formatu, kuris gali būti lengvai pritaikomas tą pačią informaciją pateikti įvairiais būdais.

Sugeneruotą dokumentacijos svetainę rasite adresu [https://lss-dok.github.io/lss-teises-aktai/](https://lss-dok.github.io/lss-teises-aktai/).

## Kaip prisidėti?

Pastebėję klaidų, ar norint išreikšti pageidavimus, sukurkite naują GitHub issue.

Norėdami prisidėti pataisymais, ar papildomu turiniu, kurkite GitHub pull request'us.

## Svetainės pasileidimas savo kompiuteryje

Sugeneruoti ir leisti svetainę yra naudojama [MkDocs](https://www.mkdocs.org/) programinė įranga, parašyta [Python](https://www.python.org/) kalba.

### Kompiuterio paruošimas

Pirmiausia turite būti įsirašę [Python](https://www.python.org/) ir [pip](https://pypi.org/project/pip/). Tada įsirašyt pip paketus:

```
pip3 install mkdocs mkdocs-material mkdocs-material-extensions
```

Į savo Python [`site-packages`](https://stackoverflow.com/a/46071447/7823460) aplanke sukurkite `pm_attr_list` aplanką, ir į jį įkopijuokite `pm_attr_list.py` iš šios repozitorijos `plugins/` aplanko.

Norint patikrinti, ar tą pavyko sėkmingai padaryti, galima paleisti šią komandą:

```
python3 -m pm_attr_list
```

Jeigu viskas gerai, Python išsijungs iškart be papildomų žinučių. Kitu atveju išspausdins klaidą.

### Serverio paleidimas

Leiskite šią komandą:

```
mkdocs serve
```

Jeigu viskas gerai, bus išspausdintos kelios informacinės žinutės, svarbiausia jų atrodys maždaug taip:

```
INFO     -  [23:49:27] Serving on http://127.0.0.1:8000/
```

Atsidarę [http://127.0.0.1:8000/](http://127.0.0.1:8000/) savo naršyklėje matysite svetainės vaizdą iš lokalaus serverio. Keičiant `*.md` ir `mkdocs.yml` failų turinį tai automatiškai atsispindės naršyklėje.
