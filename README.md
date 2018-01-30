# guitare-parleur

Le but de ce projet est de concevoir une guitare en jouet avec des boutons qui jouent des enregistrements personnalises.

## Spécification

- Léger, simple, pas trop cher
- Sur batteries (AA ou rechargeables), donc faible consommation
- Autour de 20 boutons
- Enregistrements assez bonne qualité, environ 15 secondes chacun

## Électronique

- Arduino Pro Micro
  - Usage: logiciel de contrôle
  - Acheté: https://www.amazon.co.uk/dp/B072BMYZ18/ref=pe_3187911_185740111_TE_item
- DFPlayer Mini MP3 Player
  - Usages: (a) lire carte mémoire SD (b) décoder fichier MP3 (c) amplificateur pour haut-parleur
  - Acheté: https://www.ebay.co.uk/itm/122780734012
  - Wiki: https://www.dfrobot.com/wiki/index.php/DFPlayer_Mini_SKU:DFR0299
  - Exemple: http://stonez56.blogspot.tw/2015/03/arduino-dfplayer-mini-mp3-module.html
  - Datasheet: https://github.com/Arduinolibrary/DFPlayer_Mini_mp3/raw/master/DFPlayer%20Mini%20Manual.pdf
- 6x AA battery holder
  - Usage: pour les piles
  - Acheté: https://www.amazon.co.uk/dp/B00X3LMP0G/
- Diode 1N4001
  - Usage: réduire tension de ~1V (5V fournis par Arduino vers 4.2V pour DFPlayer)
  - Acheté: https://www.amazon.co.uk/dp/B00QLTV9HW/
- Speaker 3" diameter 8 ohm 1 watt
  - Acheté: https://www.amazon.co.uk/gp/product/B00XW2NPTG
  - Datasheet: https://www.adafruit.com/product/1313
- 3" diameter black speaker cover
  - Usage: protection haut-parleur
  - Acheté: https://www.ebay.co.uk/itm/172285549238
- MPR121 Breakout Capacitive Touch Sensor Controller
  - Usage: boutons tactiles, 12 boutons max par contrôleur donc 2 cartes nécessaires
  - Acheté: https://www.ebay.co.uk/itm/162189499405 (x2)
  - Datasheet: https://www.sparkfun.com/products/retired/9695

- Il manque:
  - La carte mémoire (de récup’)
  - Des fils/câbles pour relier le tout
  - Des résistances entre TX/RX arduino et le module MP3 (puisque différence de tension logique 5v vs 4.2v)
  - Une capacitance pour protéger l'arduino de pics de consommation du haut-parleur
  - Optionnel:
    - Un transistor pour éteindre le module MP3 quand on ne s'en sert pas (pour réduire la consommation)
    - Pas facile de le choisir par contre (trop de choix)
    - https://www.reddit.com/r/AskElectronics/comments/7trtjw/help_pick_a_transistor/
