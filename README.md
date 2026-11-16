# Matopeli

Selaimessa toimiva klassinen matopeli (Snake) suomeksi. Yksi tiedosto, ei
build-vaihetta eikä riippuvuuksia – avaa vain `index.html`.

**Pelaa täältä:** https://saarajara-stack.github.io/matopeli1-demo/

## Mitä peli sisältää

- Aloitusnäkymässä annat madolle nimen (enintään 12 merkkiä) ja valitset sen
  värin kymmenestä vaihtoehdosta.
- Pelikenttä on 21 × 21 ruutua ja piirretään canvasille näkyvällä ruudukolla.
- Madon pää on vartaloa vaaleampi, ja madon nimi seuraa päätä pienenä lappuna.
- Jokaisesta ruoasta saa **+10 pistettä** ja peli nopeutuu hieman.
- Pisteet ja ennätys näkyvät ruudulla; ennätys tallentuu selaimen
  localStorageen.
- Aloitusnäkymässä on QR-koodi sivun omaan osoitteeseen, joten pelin saa auki
  puhelimella suoraan skannaamalla.

## Ohjaus

| Toiminto | Näppäimistö | Kosketusnäyttö |
|---|---|---|
| Liikkuminen | nuolinäppäimet tai WASD | pyyhkäisy tai ruudun nuolinäppäimistö |
| Tauko | välilyönti | napautus pelikentällä |

Mato ei voi kääntyä suoraan takaisin itseensä. Törmäys seinään tai omaan
vartaloon päättää pelin – hännän viimeinen pala ei kuitenkaan ole törmäys,
koska se siirtyy pois samalla askeleella.

## Tekninen huomio

Canvas skaalataan näytön pikselitiheyden (`devicePixelRatio`) mukaan, joten
grafiikka on terävä myös puhelimen näytöllä. QR-koodi piirretään cdnjs:stä
ladatulla qrcodejs-kirjastolla; jos kirjasto ei lataudu, sivun osoite näytetään
tekstinä, joten peli toimii aina.

## Tekijä

Tämä peli on tehty **tekoälyavusteisesti yhdellä promptilla** Claude Code
-työkalulla: pelin koodi, README, GitHub-repo ja GitHub Pages -julkaisu
syntyivät samasta yhdestä toimeksiannosta.
