# novi-front-end-eindopdracht
Eindopdracht voor Front End vak gestart mei 2021


# Elkweekend-ElkeStad.nl
Een stedentrip is geweldig. Even kort eruit, geen bagage nodig en ook qua voorbereiding hoef je niet veel te doen.
Helaas is het uitzoeken van een geschikte stad, met vluchten en prijzen die telkens weer veranderen een heftige opgave. Ik wil een applicatie ontwikkelen die mij aangeeft naar welke stad ik op stedentrip moet gaan.

1.	Als gebruiker kun je je registreren en inloggen.
2.	Als ingelogde gebruiker kun je aangeven naar wat voor stedentrip je opzoek bent. Als input is nodig:
  * Vertrekdatum
  * Keuze aantal nachten (1, 2 of 3)
  * Keuze vertrek-vliegveld (Maastricht-Airport, Eindhoven-Airport, Liege-Airport)
  * Budget voor vliegtickets
  * 
De applicatie zoekt de beste bestemming uit en geeft de gebruiker een top 7 op basis van de zoekcriteria.

Om een scoring systeem te maken combineer ik verschillende data-bronnen:
1.	Prijs enkel ticket retourvlucht
2.	Kosten Levensonderhoud
3.	Ranking op stedenlijst

De prijs van de vlucht haal ik binnen via de SkyScanner API.
(Bron: https://skyscanner.github.io/slate/#api-documentation)

De gemiddelde kosten van levensonderhoud in een bepaalde stad komt van het Amerikaans Department of Defense.
(Bron: https://www.defensetravel.dod.mil/site/perdiemCalc.cfm)

De stedenlijst is een vooraf opgestelde lijst. Ik heb hierbij de keuze tussen:
1.	Lijst met steden gerangschikt op aantal internationale bezoekers
(Bron: https://en.wikipedia.org/wiki/List_of_cities_by_international_visitors)
2.	De lijst van een MasterCard onderzoek uit 2016.
(Bron: https://newsroom.mastercard.com/wp-content/uploads/2016/09/FINAL-Global-Destination-Cities-Index-Report.pdf)
3.	Een lijst van een EuroMonitor Onderzoek uit 2019.
(Bron: https://go.euromonitor.com/white-paper-travel-2019-100-cities.html#download-link)
4.	Een zelf samengestelde combinatie van bovenstaande lijsten.

Vanwege het karakter van een stedentrip van maximaal 3 dagen is bij een vlucht naar een stad buiten Europa de vluchttijd zo lang, dat het niet meer interessant is. Om die reden zijn steden buiten Europa uitgesloten.

Ik heb verder weinig informatie nodig van de gebruikers, dus ik maak gebruik van de NOVI-backend om standaard gebruikersgegevens op te slaan voor het registreren en inloggen.
