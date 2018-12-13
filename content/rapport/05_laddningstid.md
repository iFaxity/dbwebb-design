Titel på rapporten
=======================

I denna rapport ska jag undersöka olika laddningstider på webbplatser och ge förslag på som kan göras för att förbättra laddningstiderna på sidorna.

Urval
-----------------------

Jag har valt webbplaserna [Mozilla Development Network](https://developer.mozilla.org), [Material Design](https://material.io) och [Stackoverflow](https://stackoverflow.com).

Jag valde dessa webbplatser eftersom det är sidor jag använder, har olika laddningstider och är olika stora.
Webbplatserna används även en del av webbutvecklare så tyckte det var passande.

En hemsida tycker jag inte ska ha en laddningstid på längre än 3 sekunder.
För jag läste i en rapport att enligt Google så efter sidan har laddat i mer än 3 sekunder så lämnar mer än hälften av användarna sidan.
Vilket är förståeligt för man vill inte kolla på en blank skärm för länge.
Vilket är skräckinjagande för hemsidor eftersom den mesta av trafiken på internet kommer från mobila enheter.
Så det blir alltmer viktigare att ha en snabb sida.

Metod
-----------------------

Vektygen jag använder i denna rapporten är Google PageSpeed och utvecklar verktygen som finns i Google Chrome.

Google PageSpeed ska användas till att ta reda på hur bra en sida är jämfört med andra hemsidor, och ger även lite tips på hur sidan kan bli snabbare att ladda. Medans utvecklar verktygen i Chrome ska användas till att mäta sidans laddningstid, storleken på sidan och antal resurser på sidan.
Och används för att få en bättre bild om hur sidan laddas på en riktig webbläsare.

För att rättvist mäta en sidas laddningstid så hämtade jag sidan 5 gånger innan jag gjorde mina 3 tester, såklart med cachen avstängd, eftersom de första gångerna man hämtar sidan så måste t.ex. routern uppdatera sin DNS och annat i nätverket.
Det gör på så sätt testet mer rättvist.

Resultat
-----------------------

<!--Dokumentera dina resultat från din studie. Berätta vad du kom fram till, vilka resultat du hittade och observerade.-->

All samlad data bifogat nedan i ett iframe element:
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRkfrPKjQLvOSFXsAPxFeHeJ_TOovhr1aQz8ONfegdvH8aSDUn9vWxPX8ZEzDHneFxmqODwGpEtHxeb/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false" width="100%" height="500"></iframe>



### Mozilla Development Network

[FIGURE src="image/screenshots/developer_mozilla.jpg?width=800" caption="Bild på MDN's webbplats"]

Mozilla Development Network (MDN) är en webbplats som är skapad av Mozilla, skaparna av Firefox webbläsaren.
Eftersom webbplatsen har dokumentation så har sidorna ofta en hel del text och mycket styles.

Dem sidorna jag valde var:

1. [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
2. [https://developer.mozilla.org/en-US/docs/Learn](https://developer.mozilla.org/en-US/docs/Learn)
3. [https://developer.mozilla.org/en-US/docs/Web/CSS/Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)


Alla sidor hade ungefär samma antal resurser, runt 15-18st per sida.
Varav mer än hälften är javascript & css filer, resten av filerna är fonter & bilder.
Fast själva materialet på sidorna ändrades så storleken på sidorna var olika.
Den totala storleken för sidorna överskred aldrig 220 KB med en snitt storlek på 214 KB.
Eftersom all javascript, css & html var gzip komprimerade. Utan komprimeringen hade sidan minst varit 30% större.

Eftersom resurserna och storleken inte skiljde sig så mycket var laddningstiderna även ganska lika.
Laddningstiderna landade då med en medel laddningstid på 353ms, med den största laddningstiden på 501ms.

Rankerna på alla sidorna från PageSpeed var faktisk bra på alla sidor.
Alla sidorna på desktop hade en rank på 100, medans på mobiler var det ett snitt på 93 med den minsta på 92.
Vilket betyder att sidorna är bra optimiserad, enligt PageSpeed i alla fall.

Det finns faktisk inte så mycket att bättra på denna webbplatsen utifrån dem sidor jag hade valt. Det enda man kan göra är att att ladda CSS som inte är viktig sist på sidan, och splitta upp CSS filerna så man undviker onödig kod.
Men ju fler filer man har så får man fler förfrågningar och detta kan göra sidan långsamare, speciellt på mobila enheter.

Så risken är inte riktigt värt att ta för att vinna några extra millisekunder.
Speciellt om man har en sida med mycket mobila användare, vilket blir vanligare på webben.


### Material Design

[FIGURE src="image/screenshots/material.jpg?width=800" caption="Bild på Material Designs webbplats"]

Material Design är en webbplats med specifikationer & guider från Googles Material Design. Denna webbplatsen blir allt mer populär på internet bland utvecklare som är intresserade i Google's design på t.ex. deras appar, hemsidor, etc.
Detta är en webbplats jag bekantat mig med det senaste året och hittar inspiration för när jag designar ibland.

Dem sidorna jag valde var:

1. [https://material.io/design](https://material.io/design)
2. [https://material.io/design/introduction](https://material.io/design/introduction)
3. [https://material.io/design/guidelines-overview](https://material.io/design/guidelines-overview)

Eftersom dessa sidorna är ordentligt utsmyckade med både design och skript så är sidorna ganska tunga och tar en hel del tid att ladda.
Antalet resurser är minst 28 och maximalt 38, med ett snitt på 34 stycken filer.
Av dessa filer är lite mer än hälften javascript och bilder.
Den största javascript filen är nästan 400 KB, filen är inte komprimerad men är minifierad.
Där är även en hel del PNG bilder som kunde varit JPEG och hade fått bättre komprimering.

Totalt så är den största sidan 2 MB, men snittet ligger på 1381 KB.
Detta tar en hel del på laddningstiden med många filer och stora filer.
Så den minsta laddningstiden är på 1340ms medans snittet ligger på 1779ms.
Så det tar en lång tid för sidan att ladda.

Rankerna på alla sidorna från PageSpeed är ok på desktop med ett snitt på 96. Medans på mobil blir det mycket sämre, med ett snitt på 32. Vilket är mycket dåligt, vilket betyder att sidan är till för desktops och inte mobiler. Sidan är dock responsiv och ser bra ut på mobiler vilket är konstigt.

Denna sidan går att förbättra med en hel dels jobb. Det största problemet sidan har är den gigantiska javascript filen som inte är komprimerad. Där finns dock andra filer som också behövs komprimeras. Sedan måste bilderna uppdateras till JPEG där det passar och kanske behöver dem skalas om eftersom dem skalas ner från en stor bild som blir liten på sidan. Sedan hade det behövts att ladda oviktig CSS sist så att rendereringen inte blockeras som den gör nu.

### Stackoverflow

[FIGURE src="image/screenshots/stackoverflow.jpg?width=800" caption="Bild på Stackoverflows webbplats"]

Stackoverflow är en webbplats för att fråga och svara på frågor man har för specifikt programmering. Eftersom det är ett arkiv för frågor om specifika saker i programmering så är det en väsentlig webbplats för programmerare. Man kommer ofta besöka webbplatsen för att hitta svar till problem man stött på.

Dem sidorna jag valde var:

1. [https://stackoverflow.com/questions](https://stackoverflow.com/questions)
2. [https://stackoverflow.com/tags](https://stackoverflow.com/questions)
3. [https://stackoverflow.com/questions/tagged/javascript](https://stackoverflow.com/questions)

Antalet resurser var ganska förvånande många på de flesta sidorna. Snittet på hur många filer som hämtades var 39 st. Men det minimala var 17 st. På de flesta sidorna så ändrades antalet filer, detta på grund av att sidan använder sig av reklam. Eftersom reklamen ändrades varje gång sidan hämtades så hämtades olika mängd filer.

Trots att hemsidan hämtade en hel del filer så var den största sidan totalt 564 KB. Vilket är lite om man tänker på att din sidan hämtade 56 resursfiler. Dock landade medelvärdet för sidstorlek på 460 KB vilket är inte så mycket för en hemsida. Detta är på grund av att varje fil som kan komprimeras var komprimerade. Så det sänkte drastiskt storleken på varje förfrågan webbläsaren gjorde. Bilderna som användes på sidan var också nerskalade så att man inte hämtade onödigt stora bilder.

Den minsta laddningstiden låg på 398ms vilket inte är alltför farligt. Medans snittet låg på 546ms. Vilket är på grund av den mängden förfrågningar webbläsaren behöver göra. Vissa av filerna är även render blockerande, så webbläsaren måste vänta tills filen är hämtad tills att få fortsätta renderera sidan för användaren.

Rankerna på sidorna från PageSpeed är faktiskt bra, förutom en specifik sida. Alla sidor hade samma ranker på både mobil och desktop. Den mobila ranken låg på 95, medans desktop ranken låg på 100. Vilket är i princip perfekt.

Dock finns där rum för att sidan bättre. Vissa filer har en chachelagrings policy på 1 dag eller 7 dagar, vilket hade kanske kunnat bli bättre eftersom då behöver inte sidan hämta resurserna på nytt igen lika ofta. Kanske en månad istället hade varit bättre. Har man ETaggar på sin server så kan man öka värdet till flera månader då det hjälper att se när en fil har ändrats och behövs hämtas på nytt. På så sätt kan man ha det bästa av båda världarna så att säga.


Analys
-----------------------

<!--Diskutera och analysera de resultaten du fann.-->
Utifrån mitt resultat så är min slutsats att bland dem sider jag valt så är laddningstiderna förvånansvärt bra.
Eftersom laddningstiderna total snittar under 1 sekund, vilket är 2 sekunder snabbare än vad jag tyckte var den maximala tiden en sida borde få ladda.
Den sidan som tog längst tid att ladda var lite över 2 sekunder, så även den var snabbare än 3 sekunder.

Dock fick sidorna som tog längre att ladda mindre poäng på PageSpeed, i alla fall på den mobila sektorn.
Detta är på grund av att PageSpeed tar hänsyn till filstorlek och är lite mer strikt genom att simulera en telefon så laddningstiden blir sämre för simulatern eftersom man vet inte riktigt hur det fungerar.

Men eftersom PageSpeed är en webb version av Lighthouse (moderna testverkyt inbyggt i Chrome) så kan man anta att dem segar ner en dator processor en hel del, vilket inte heller är ett rättvist test mot mobiler eftersom moderna mobiler är en hel del snabbare nu.
Eftersom jag provade den sidan som hade sämst laddningstid och provade på min Pixel 2 telefon. Enligt PageSpeed laddade sidan på mobilen på 14 sekunder.
Medans på min telefon tog det 3-4 sekunder att ladda.

Där finns dock områden där sidorna kan bli snabbare.
Speciellt inom komprimering av statiska resursfiler och bildstorlek.
Sedan finns det mindre områden man kan göra bättre som att städra undan CSS som inte behövs för alla sidor så slipper man skicka med en generell CSS styles resurs.

Dock gjordes dessa mätningar när man hade laddat sidan 3 gånger så att det blir en så kallad "warm run", för att sidan är alltid lite sölig första gången man laddar pga hur internet fungerar.
Så vill man ha ett mer "riktigt" resultat kan man prova att rensa sin DNS och lite andra nätverksinställningar.
Dock blir det inte rättvist då man "jämför äpplen med apelsiner" eftersom det kan bli fler DNS hopp för olika sidor beroende på vart dem ligger i världen.


Referenser
-----------------------
[https://www.marketingdive.com/news/google-53-of-mobile-users-abandon-sites-that-take-over-3-seconds-to-load/426070/]

Övrigt
-----------------------

Rapport utförd av Christian Norrman (chnc16).
