# guitare-parleur

Le but de ce projet est de concevoir une guitare en jouet avec des boutons qui jouent des enregistrements personnalises.

## Specification

- Leger, simple, pas trop cher
- Sur batteries (AA ou rechargeables), donc faible consomattion
- Autour de 20 boutons
- Enregistrements assez bonne qualite, environ 15 secondes chacun

## Electronique

- DFPlayer Mini MP3 Player
  - Usages: (a) lire carte memoire SD (b) decoder fichier MP3 (c) amplifieur pour haut-parleur
  - Achete: https://www.ebay.co.uk/itm/122780734012
  - Wiki: https://www.dfrobot.com/wiki/index.php/DFPlayer_Mini_SKU:DFR0299
  - Example: http://stonez56.blogspot.tw/2015/03/arduino-dfplayer-mini-mp3-module.html
  - Datasheet: https://github.com/Arduinolibrary/DFPlayer_Mini_mp3/raw/master/DFPlayer%20Mini%20Manual.pdf
- 6x AA battery holder
  - Usage: pour les piles
  - Achete: https://www.amazon.co.uk/dp/B00X3LMP0G/ref=pe_3187911_185740111_TE_item
- Diode 1N4001
  - Usage: reduire tension de ~1V (5V fournis par Arduino vers 4.2V pour DFPLayer)
  - Achete: https://www.amazon.co.uk/dp/B00QLTV9HW/ref=pe_3187911_185740111_TE_item
- Speaker 3" diameter 8 ohm 1 watt
  - Achete: https://www.amazon.co.uk/gp/product/B00XW2NPTG
  - Datasheet: https://www.adafruit.com/product/1313
- 3" diameter black speaker cover
  - Usage: protection haut-parleur
  - Achete: https://www.ebay.co.uk/itm/172285549238
- MPR121 Breakout Capacitive Touch Sensor Controller
  - Usage: boutons tactiles, 12 boutons max par controlleur donc 2 cartes necessaires
  - Achete: https://www.ebay.co.uk/itm/162189499405 (x2)
  - Datasheet: https://www.sparkfun.com/products/retired/9695

- Il manquent:
  - La carte memoire (de recoupe)
  - Des fils/cables pour relier le tout
  - Des resistences entre TX/RX arduino et le module MP3 (puisque difference de tension logique 5v vs 4.2v)
  - Une capacitance pour proteger l'arduino de pics de consomation de l'haut parleur
  - Optionnel:
    - Un transisteur pour etteindre le module MP3 quand on ne s'en sert pas (pour reduire la consomation)
    - Pas facile de le choisir par contre (trop de choix)
    - https://www.reddit.com/r/AskElectronics/comments/7trtjw/help_pick_a_transistor/
