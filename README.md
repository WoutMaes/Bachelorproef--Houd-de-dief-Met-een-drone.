# Bachelorproef-Houd de dief! (met een drone). Een zoektocht naar de optimale drone voor politiediensten. Hardware, software en       juridische factoren in rekening gebracht.

Deze scriptie wordt gemaakt om de graad van professionele bachelor in de toegepaste informatica te verkrijgen.

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

## Author

* **Wout Maes** - *Initial work* - [PurpleBooth](https://github.com/WoutMaes)

## Promotor

* **Jens Buysse** - *Contributor* - [PurpleBooth](https://github.com/eothein)

## Co-Promotoren:

* **De Ridder Christiaan** - *Politie Westkust* 
* **Koen Henderickx** - *Easycopters*


