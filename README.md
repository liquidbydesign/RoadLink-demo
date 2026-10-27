# RoadLink – interaktiv demo

**Stay connected - Save lives**

[Öppna demonstrationen](https://liquidbydesign.github.io/RoadLink-demo/)

Projektet deltar i tävlingen **Gick inte. Nu går det.** under **Eget spår**. Jag undersöker både möjligheterna och det som går fel när trafikdata och AI ska hjälpa oss att förstå varandras rörelser. Jag har länge haft en idé om ett sånt här system i bakhuvudet, men det är först nu med AI jag verkligen kan få hjälp att ta fram ett gränssnitt och testa förslag på funktioner och scenarier före skarp utveckling av app.

## Idén bakom RoadLink

Bilen har använts av oss människor i långt över hundra år. Ändå är våra möjligheter att förmedla avsikter och kommunicera med andra bilister fortfarande begränsade till tuta och blinkers. Jag vill undersöka hur vi kan ge trafikanter en bättre förståelse för vad som händer runt dem och förbättra trafiksäkerheten med en app i mobilen.

Jag vill också göra det möjligt att skicka tydliga meddelanden till andra trafikanter i närheten: uppmärksamma någon om en trasig lampa eller rök från ett hjul, eller säga ”Kör du först” när två bilar väntar vid en avsmalning. Med färdiga meddelanden och på sikt röstinmatning ska föraren kunna förmedla sin observation eller avsikt med få moment. Mottagaren ska kunna svara eller dölja meddelandet, och en tillfällig kontakt ska tillåta svar även efter att bilarna lämnat varandras närhet.

Inspirationen kommer från luft- och sjöfartens sätt att dela information om andra flygplan och fartyg i närheten samt varna vid risk för kollision. Tänk om du kunde få en förvarning när en bakomvarande bil närmar sig snabbt, eller när ett utryckningsfordon är på väg mot samma korsning men ännu inte syns. Och tänk om uppgifter om planerade färdvägar kunde hjälpa till att upptäcka möjliga konflikter innan förarna själva ser dem.

RoadLinks vision är att göra sådan information lätt att uppfatta via bilens skärm, exempelvis genom Android Auto eller Apple CarPlay. Relevanta uppgifter om rörelse och nästa manöver skulle kunna delas tillfälligt, utan att andra förare behöver se personens identitet eller exakta slutdestination.

Det här är samtidigt en idé som behöver prövas. Hur hanterar vi felaktiga positioner, fördröjningar och bilar som saknar appen? Kan AI ge användbar framförhållning utan att orsaka för många falsklarm? Därför bygger projektet både gränssnitt och lokala experiment där misslyckandena får vara en del av resultatet.

## Prova demonstrationen

En svensk prototyp om delad trafikmedvetenhet. Bilskärm och mobilskärm, simulerade fordonsmeddelanden med färdiga observationer, inkommande aviseringar och tillfälliga svar, panorerbar karta med Centrera och kantmarkeringar för trafik utanför vyn, ruttbaserade blåljusscenarier och ett körförlopp med fokusvy, ett matematiskt risklabb och ett AI-labb med en liten lokalt tränad rörelsemodell och ett ETA-labb med tränade ankomsttider och kalibrerade intervall.

## Prova meddelandefunktionen

1. Välj **Normal körning**. Klicka på en grön bil på kartan eller öppna **Meddelanden** och välj ett fordon. Listan visar fiktivt registreringsnummer, bilmodell och färg.
2. Välj ett av **tio färdiga meddelanden**, till exempel **Missljud**, **Rök från hjul** eller **Vid avsmalning → Kör du först**. Kontrollera mottagare och text och välj **Skicka i demo**.
3. Prova **Test: bilen lämnar området** och **Testa mottagarens svar** i konversationen. Svar tillåts inom den tillfälliga kontakten, medan nya observationer kräver att bilen är nära och uppgifterna färska.
4. Välj **Testa inkommande meddelande** under uppspelningen. Aviseringen under kartan kan öppnas med **Öppna & svara**, eller döljas med **Dölj**. Ett valt svar bekräftas före sändning.
5. Hitta även dolda meddelanden via **Meddelanden → Konversationer**. Kontakten gäller i 15 minuter från första meddelandet och kan avslutas eller blockeras.

All kommunikation är simulerad och stannar i webbläsarsessionens minne. Testavstånd och fordonsuppgifter är påhittade. Röstinmatning och automatisk hämtning av modell och färg via registreringsnummer är framtida funktioner. Omladdning tömmer meddelandehistoriken.

### Prova kartans nya funktioner

Dra kartan med mus eller finger, eller fokusera kartan och använd piltangenterna. **Centrera** eller Home återställer vyn till din bil. Kameran hålls inom samma simulerade täckningsgräns som kantmarkeringarna använder. Gränsen är streckad och statusen visar när den nås. Detta är ett schematiskt testområde, inte en uppmätt nätverksräckvidd.

Välj **Blåljus närmar sig**, **Blåljus från höger**, **Bil närmar sig snabbt** eller **Fordon framifrån** för att se blå respektive orange kantmarkeringar innan fordonet syns i vyn. Markeringen försvinner när fordonet visas eller underlaget är för gammalt. Panorerar du till fordonet försvinner markeringen även då.

All trafik och alla blåljuskällor är simulerade. Ingen position samlas in. Inga verkliga trafikvarningar skickas. Verklig bilintegration och trafikkommunikation är ännu inte anslutna.

Denna offentliga demokopia innehåller endast körbara HTML-filer. Huvudprojektets utvecklingsmaterial förvaltas separat.
