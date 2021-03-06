#AF1.3 Läsa resultat av match

En spelare vill se resultatet av sin spelade match. Systemet har kalkylerat matchen och resultatet och matchhändelserna
går att se.

##UC1 Läsa resultat av match
###Huvudscenario
- Starar när en spelaren vill atuentisiera sig som en användare. (1d)
- Systemet ber om spelarens användarnamn och lösenord.
- Spelaren anger "Kalle" som användarnamn och "password" som lösenord. (1a)
- Systemet autentisierar spelaren som en användare och presenterar att autentisieringen lyckades.
- Systemet presenterar startsidan för spelarens lag.
- Spelaren går in på "Matcher" för att hitta den senast spelade matchen samt en lista över tidigare spelade matcher. (1b)
- Spelaren väljer den senast spelade matchen och läser resultatet. (1c)

###Alternativa scenarios
1a. Spelaren kunde inte autentisieras

- Systemet presenterar felmeddelande.
- Systemet erbjudern en "Återställ Lösenord"-funktion (1e)
- Gå till steg 2 i huvudscenario.

1b. Spelaren har inga matcher spelade

- Systemet presenterar meddelande om att inga matcher är spelade.
- Gå till steg 5 i huvudscenario.

1c. Systemet kan inte läsa matchens resultat

- Systemet presenterar meddelande om att systemtekniska fel uppstått angående matchens resultat
- Gå till steg 5 i huvudscenario.

1d. Servern för spelet är inte online

- Systemet presenterar meddelande om att servrarna inte är tillgängliga och ber användaren försöka igen senare
- Gå till steg 1 i huvudscenario.

1e.

- Spelaren trycker på "Återställ Lösenord".
- Spelaren skriver in "Kalle@email.com" som sin e-mail.
- Spelaren får ett nytt lösenord i sin e-mail.
- Spelaren skriver in "Kalle" som användarnamn och "1kd43e" som nytt lösenord slumpat av systemet.
- Gå till steg 4 i huvudscenario.
