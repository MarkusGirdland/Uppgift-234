#AF1.3 - Läsa resultat av match

En spelare vill se resultatet av sin spelade match. Systemet har kalkylerat matchen och resultatet och matchhändelserna
går att se.

### Primär Aktör
Spelare

### Förkrav
Inloggad (F1) som Spelare och medlem tillräckligt länge att laget har spelat en match.

### Huvudscenario
1. Startar när Spelaren vill se resultatet

2. Systemet kontaktar databasen med Spelarens id och ber om Spelarens information.

3. Databasen svarar med Spelarens information och senaste uppdateringar angående ev. match som spelats.

4. Spelaren går in på "Matcher" för att hitta den senast spelade matchen samt en lista över tidigare spelade matcher.

5. Spelaren väljer den matchen som senast var spelade och ser resultat samt en matchtext med minut-för-minut händelser av matchen.


### Alternativa Scenarios
2a Databasen svarar med ett felmeddelande eller så misslyckades kontakten.
  1. Systemet meddelar Spelaren att man inte kunde få information av systemtekniska skäl och ber Spelaren vänta och försöka senare.
  Felmeddelandet, tidpunkt, Spelarensw id sparas i fel-loggen.
  Användningsfallet avslutas.
  
4a Spelaren har inga nya matcher spelade
  1. När Spelaren går in på "Matcher" så finns bara tidigare spelade matcher samt en lista på matcher som snart ska spelas.

## Datadefinitioner
### Spelarens information från databasen
Inloggningsnamn, spelarprofil & information om laget, exempelvis:

  - Namn
  - Ekonomi
  - Matcher
  - Logotyp/Tröjor
   
### Matchtext från spelad match
En text innehållande simulerade händelser som pågick under matchen, exempelvis:

  "Anton Berg (spelar Batrider) spelar agressivt och blir fångad av motståndarlagets Nyx Assassin och ger dom därmed First Blood."
  
## Frågor
- Hur simluera matcher?
- Vilka händelser ska presenteras vid matchtexten?
