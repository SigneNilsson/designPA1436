---
Title: 02_load
Description: kmom05
Template: anAnalysis
---


# 02_load

Kmom05 
=======================

Utvärdering av webbplatsers laddningstid och användbarhet.

Urval
-----------------------

Av bekvämlighet utvärderas samma webbplatser som i kmom04. För varje webbplats valdes tre sidor vars laddningstid undersöktes.
De tre sidorna som valdes var för varje webbplats: startsida, about samt en sida för antingen blogg eller webshop.

Metod
-----------------------

För varje av de tre valda sidorna för varje webbplats användes Google Pagespeed för att få mätvärden att utgå ifrån vad det gäller både LCP och FCP, både
för desktop- och mobil-enheter. Även det sammanlaga "betyget" på prestanda noteras. En av de valda webbsidorna hade ingen data som utgick från verklig 
användning av webbsidan tillgänglig. I detta fall används bara de mått på prestanda som presenteras.

Utöver detta användes Devtools för att få mäta laddningstid för DOM och LOAD samt tid tills sidan laddats klart helt. Även antalet resurser samt sidans totala storlek noteras. 
För varje sida görs mätningarna tre gånger för att få ett medelvärde för de tidigare nämnda värdena.


Resultat
-----------------------

Data från samtliga mätningar:

<iframe width="402" height="346" frameborder="0" scrolling="no" src="https://studentbth-my.sharepoint.com/personal/sinl24_student_bth_se/_layouts/15/Doc.aspx?sourcedoc={5eea5663-a5f7-495f-bb38-fc757f13d264}&action=embedview&wdAllowInteractivity=False&wdHideGridlines=True&wdHideHeaders=True&wdInConfigurator=True&wdInConfigurator=True"></iframe>

Baserat på mätvärdena ovan skulle jag rangordna mina sidor i följande ordning från bäst till sämst vad det gäller laddningstid:

1. https://www.elizabethwhibley.co.uk/
2. https://www.louisetilbrookdesigns.net/
3. https://www.katiejonesknit.co.uk/

### Webbplats 1:
https://www.elizabethwhibley.co.uk/

<figure>
<a href ="%assets_url%/img/EW.png"><img src="%assets_url%/img/EW.png" style = "width: 250px"></a>
<figcaption>Snapshot av https://www.elizabethwhibley.co.uk/ tagen 2024-12-10</figcaption>
</figure>

En möjlig förbättring enligt Google Pagespeed skulle vara att minska körtiden för JavaScript.

### Webbplats 2: 
https://www.katiejonesknit.co.uk/

<figure>
<a href ="%assets_url%/img/KJ.png"><img src="%assets_url%/img/KJ.png" style = "width: 250px"></a>
<figcaption>Snapshot av https://www.katiejonesknit.co.uk/ tagen 2024-12-10</figcaption>
</figure>

En möjlig förbättring enligt Google Pagespeed skulle vara att minska körtiden för JavaScript samt ta bort oanvänd JavaScript-kod.

### Webbplats 3: 
https://www.louisetilbrookdesigns.net/

<figure>
<a href ="%assets_url%/img/LT.png"><img src="%assets_url%/img/LT.png" style = "width: 250px"></a>
<figcaption>Snapshot av https://www.louisetilbrookdesigns.net/ tagen 2024-12-10</figcaption>
</figure>

En möjlig förbättring enligt Google Pagespeed skulle vara att minska körtiden för JavaScript.

Analys
-----------------------

Inga av sidorna fick godkänd performance enligt Google Pagespeed. 

Det är stor skillnad i datan på tiden som krävs för att ladda sidorna. Den sida som klart får bäst betyg på desktop i både Pagespeed och mått på tid att ladda i devtools är webbplats 1. Den har överlägset lägst laddningstid på samtliga sidor vilket inte är så förvånande eftersom den också har minst totala storlek.

Webbplats 2 har sämst betyg i Pagespeed för både desktop och mobil. Här finns också de sämsta resultaten för tidsmåtten Load och DOMContent från mätningarna i Devtools. 

Den största sidan från Webbplats 2 respektive 3 är ungefär i samma storlek, men skillnaden i laddningstid är stor. Den största sidan på webbplats 2 har en Load-tid på över 5 sekunder, medans motsvarande på Webbplats 3 är strax under 3 sekunder. Detta trots att sidan på Webbplats 3 har dubbelt så många requests som sidan på Webbplats 2.

En förbättringsmöjlighet som återkommer för samtliga webbplatser är _"Reduce JavaScript execution time"_. Körning av JavaScript tar t.ex. upp mycket minne och exekveras på "main-thread" vilket gör att sidan då inte kan lyssna till användares input, sidan blir alltså trög. Se [1] för ytterligare information.

En annan förbättringsmöjlighet som återkommer för samtliga webbplatser är _"Minimize main-thread work"_. Jag vet inte exakt vad det betyder, men översiktligt verkar det handla om att "main-thread" på webbläsaren används till onödiga delar vilket gör att sidan då kan bli långsam eftersom det också är "main-thread" som används vid interaktion med webbplatsen. Se [2] för ytterligare information.

Samtliga webbplatser upplevs ok utifrån laddningstid baserat på min egen upplevelse när jag går in på sidorna, men det kanske är för att jag är född på 90-talet och har upplevt värre laddningstider... En översiktlig googling visar att ca.2-3 sekunder verkar vara maxgränsen för att en webbsida inte ska anses ladda långsamt.

Samtliga sidor är ganska bildtunga och behöver också vara det för att kunna nå ut med de olika kreatörernas arbete, men ytterligare en potentiell möjlighet att minska laddningstid i stort är att t.ex. alltid optimera bildernas storlek.

Referenser 
------------------
[1] https://developer.chrome.com/docs/lighthouse/performance/bootup-time

[2] https://developer.chrome.com/docs/lighthouse/performance/mainthread-work-breakdown 


