# Bachelorproef-Houd de dief! (met een drone). Een zoektocht naar de optimale drone voor politiediensten. Hardware, software en       juridische factoren in rekening gebracht.

Deze scriptie wordt gemaakt om de graad van professionele bachelor in de toegepaste informatica te verkrijgen. 2019 - 2020

## Onderwerp van deze bachelorproef

In deze bachelorproef wordt een onderzoek gevoerd naar hoe politiediensten kunnen gebruik maken van drones of andere onbemande vliegende toestellen (voortaan wordt een UAV -Unmanned Aerial Vehicle- gebruikt als afkorting voor een onbemand vliegend toestel, als het specifiek gaat om de drone in de POC, dan wordt wel gewoon drone gebruikt) om een persoon te vatten die in overtreding is met de wet. Dit kan zowel betekenen dat deze persoon een misdrijf aan het plegen is of reeds een misdrijf heeft gepleegd in het verleden en daar nu voor wordt gezocht.


## Algemene opmerkingen in verband met deze bachelorproef

Deze bachelorproef is door de auteur geschreven om de politiediensten op een gepaste manier te helpen met het detecteren van verdachte personen en is geenszins bedoeld om overheden of politiediensten te helpen met het beperken van de vrijheden van hun burgers. Deze bachelorproef moet dat ook zo gelezen worden dat dit enkel kan gebruikt worden conform het Koninklijk Besluit van 22 februari 2006 betreffende de installatie en de werking van bewakingscamera's in de voetbalstadions en de Camerawet van 21 maart 2007 en het Europees verdrag tot bescherming van de rechten van de mens en de fundamentele vrijheden (EVRM).

## Wegwijs in deze bachelorproef

Deze bachelorproef bestaat uit een theoretisch luik en een praktisch deel, ook wel de Proof Of Concept genoemd (voortaan afgekort als POC). Voor de POC wordt gebruik gemaakt van een Tello DJI Drone. Deze drone is een klein instapmodel gemaakt door de startup Ryze Tech en wordt verkocht door DJI voor ongeveer $99. DJI heeft deze drone samen met Intel ontworpen om studenten te leren werken met drones aan een lage instapprijs. Doordat je deze drone in tegenstelling tot veel andere drones zelf (beperkt weliswaar) kan programmeren is deze drone uiterst geschikt voor de POC van deze bachelorproef. 

In deze repo vindt u ook een applicatie om een tello drone van DJI te besturen via een intranetsite op poort 5000.
De tello drone die u hier voor nodig heeft kan u kopen voor ongeveer 90 euro en dient u te verbinden via zijn
wifi op het IP-adres 192.168.10.1 UDP PORT:8889

Met deze applicatie kan u de drone aansturen en een persoon laten volgen van op afstand.
Er is OpenCV geïmplementeerd. Deze opensource software van Intel laat ons toe om gezichten te detecteren.

De beelden van drone worden doorgestuurd naar de intranetsite op jou server. Hier wordt de beelddetectie gedaan.
Aan de hand van deze beelddetectie kan de drone autonoom vliegen en jou volgen. Er is dus geen manuele besturing meer nodig.

## Benodigdheden

Deze zaken heb je nodig om deze bachelorproef te kunnen runnen:

1) [Tello DJI drone](https://store.dji.com/product/tello?from=autocomplete&position=0&vid=38421) of de [Tello DJI EDU drone](https://store.dji.com/product/tello-edu?from=autocomplete&position=1&vid=47091). De Tello DJI kost ongeveer $99 en de Tello DJI EDU kost ongeveer $149. U heeft ook een standaard Micro-USB-adapter nodig, maar dit wordt niet meegeleverd in de meeste pakketten.
2) MAC/Windows/Linux

## Software die U nodig heeft

* [PycharmIDE](https://www.jetbrains.com/pycharm/) - Dit is je werkomgeving.
* [Python](https://www.python.org/) - Om Python te kunnen gebruiken moet je eerst Python installeren. 
* [OpenCV](https://sourceforge.net/projects/opencvlibrary/files/opencv-win/) - Dit heb je nodig voor de object herkenning.
* [ffmpeg](http://ffmpeg.org/) - Dit heb je nodig om de videobeelden te streamen.
* [jQuery](https://jquerymobile.com/download/) - Web Framework om HTML5 responsive website te maken.

### Clone this repo

   ```bash
   git clone https://github.com/HoGent-Projecten3/projecten3-1920-angular-kolv02
   ```


### Installeren van PyCharm

Dit wijst zichzelf uit. [Download de laatste versie ](https://www.jetbrains.com/pycharm/) en volg de stappen.

### Installeren van Python

[Download versie 3.8 of hoger](https://www.python.org/) en kies bij het installeren voor Add Python 3.8 to PATH. Klik daarna op install now. De rest wijst zichzelf uit.

### Installeren van OpenCV

Dit is het installatieproces voor een windowssyteem.

[OpenCV](https://sourceforge.net/projects/opencvlibrary/files/opencv-win/) downloaden kan wel wat tijd in beslag nemen. Ga naar de downloadsfolder en kopier de opencv folder naar de Local Disk(C:). 

Ga vervolgens naar opencv/build/x64/vc15/bin en kopier dit path en maak er een environment variabele van.

Open vervolgens cmd en typ:

```
pip install opencv-python
```

### Installeren van ffmpeg

[ffmpeg downloaden](http://ffmpeg.org/) en installeren gaat als volgt: 

```
Voor de nieuwste Windowssytemen: 
Klik op de download knop
Kies het Windows logo 
Kies Windows build
Kies versie 4.2.2 
Kies architecture Windows 64-bit
Kies linking Static
```

Unzip de ffmpeg-4.2.2-win64-static file. Kopier het resultaat naar de Local Disk(C:).

Ga in de folder op de Local Disk(C:) naar ffmpeg/bin/ffmpeg  en kopier dit path en maak er een environment variabele van.

### Installeren van jQuery

Dit hoeft u normaal niet meer te installeren als u deze repository juist heeft gecloned.

### Download deze repository op jouw PC

Open Bachelorproef--Houd-de-dief-Met-een-drone./DroneApplicatie/ in PyCharm.

### Packages installeren

De drie onderstaande lijnen staan al in een requirements.txt file in ons pythonproject.

```
opencv-python==4.0.0.21
numpy==1.16.2
Flask==1.0.2
```

Maar je moet deze nog installeren via:

```
pip3 install -r requirements.txt
```

### Download de Tello DJI app in de Google Play Store of in App Store van Apple.

Dit is optioneel voor als je eerst wilt testen of dat je wel verbinding kan maken met de drone.
Dit is een klein bestandje en de download neemt niet veel tijd in beslag.

### Verbinden met de drone

Zet uw drone aan en connecteer uw drone met uw PC of laptop door middel van WIFI. Uw wifi netwerk zal het netwerk van de drone automatisch vinden als de drone aanstaat en zich dicht genoeg bij uw PC of laptop bevindt. 

Meer hoeft u niet de doen om uw drone te connecteren.

### Start het project in PyCharm

Indien u alles correct heeft geïnstalleerd dan kan u nu de drone besturen via jouw localhost op [http://localhost:2000/controller/](http://localhost:2000/controller/).

Nu kan u de drone besturen en ook uzelf laten volgen door de drone.

## Leren werken met de drone

[Algemene info over de drone](https://www.ryzerobotics.com/tello/downloads)

[Tello DJI SDK Documentatie](https://terra-1-g.djicdn.com/2d4dce68897a46b19fc717f3576b7c6a/Tello%20%E7%BC%96%E7%A8%8B%E7%9B%B8%E5%85%B3/For%20Tello/Tello%20SDK%20Documentation%20EN_1.3_1122.pdf)

[Tello DJI User Manual](https://dl-cdn.ryzerobotics.com/downloads/Tello/20180212/Tello+User+Manual+v1.0_EN_2.12.pdf)

## Author

* **Wout Maes** - *Initial work* - [Wout Maes](https://github.com/WoutMaes)

[![Wout](https://avatars0.githubusercontent.com/u/36442271?s=200)](https://github.com/WoutMaes)

## Promotor

* **Jens Buysse** - *Contributor* - [Jens Buysse](https://github.com/eothein)

## Co-Promotoren:

* **De Ridder Christiaan** - *Politie Westkust* 
* **Koen Henderickx** - *Easycopters*
