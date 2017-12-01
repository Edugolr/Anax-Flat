Usability
===============================
Det som följer är en utvärdering av webbplatsers laddningstid och användbarhet
på 3 sidor jag själv valt ut.

Hjälpmedel som använts är som följer:
[Firefox Screenshots](https://support.mozilla.org/en-US/kb/firefox-screenshots) För skärmbilderna.
[Google Kalkylark](https://www.google.com/intl/sv/sheets/about/) För datahantering.
[Google Pagespeed Insights](https://developers.google.com/speed/pagespeed/insights/) för analys av vad som kan göras snabbare på websidorna.
[Firefox dev tool Network_Monitor](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor)
För analys av laddningstid data och förfrågningar

De 3 sidor jag valt är baserade på sidor jag själv besöker ofta samt en sida
som handlar om just webboptimering.

* [Nhl.com](https://www.nhl.com).
* [fz.se](https://www.fz.se).
* [optimizely.com](https://www.optimizely.com).


Excelark med rådata
[Rådata](https://docs.google.com/spreadsheets/d/1HumkPekYqS5ILaBvKOrBYqURDEhk59UgolW4ioKVn2I/edit?usp=sharing)


##NHL
[FIGURE src="image/NHLScreenshot.jpg?w=400&h=200" class="right"]

###Pagespeed poäng:
Mobil: 57/100.

+ Utnyttja cachelagring i webbläsare.
+ Prioritera synligt innehåll.
+ Aktivera komprimering.
+ Förminska JavaScript.
+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Optimera bilder.
+ Minska svarstiden från servern.

Dator: 64/100.

+ Utnyttja cachelagring i webbläsare.
+ Optimera bilder.
+ Aktivera komprimering.
+ Förminska JavaScript.
+ Prioritera synligt innehåll.
+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Minska svarstiden från servern.

Total: 121/200
###DevtoolNetwork:
Genomsnitt
Förfrågningar	Data	Hastighet
181	            12.01	30.32

###Diskussion förbättringsmöjligheter
NHL.com Har en mycket content tung startsida. Jag hade gärna sett att man behöll
sin slideshow med higlights från nattens matcher men resten borde skalas ned.
Länkas med en thumb till matcherna eller dylikt. Sidan är alldeles för långsam.



##FZ
[FIGURE src="image/FZScreenshot.jpg?w=400&h=200" class="right"]

###Pagespeed poäng:
Mobil: 48/100.

+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Optimera bilder.
+ Utnyttja cachelagring i webbläsare.
+ Minska svarstiden från servern.
+ Aktivera komprimering.

Dator: 65/100.

+ Optimera bilder.
+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Utnyttja cachelagring i webbläsare.
+ Aktivera komprimering.

Total: 113/200

###DevtoolNetwork:
Genomsnitt
Förfrågningar	Data	Hastighet
114	            3.87	27.17

###Diskussion förbättringsmöjligheter
fz.se Har mycket bilder på sin sida. Genom komprimering utav dessa fick jag fram
genom google Insights att de skulle *minska storleken med 350,3 kB (42 % reduktion).*
Annars spontant tycker jag även denna startsida är lite lång och packad med content.


##Optimizely
[FIGURE src="image/OptimizelyScreenshot.png?w=400&h=200" class="right"]

###Pagespeed:
Mobil: 56/100.

+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Utnyttja cachelagring i webbläsare.
+ Optimera bilder.
+ Förminska CSS.
+ Förminska HTML.

Dator: 73/100.

+ Ta bort JavaScript- och CSS-kod som blockerar renderingen från innehåll ovanför mitten.
+ Utnyttja cachelagring i webbläsare.
+ Optimera bilder.
+ Förminska CSS.
+ Förminska HTML.

Total: 129/200

###DevtoolNetwork:
Genomsnitt
Förfrågningar	Data	Hastighet
78.33	        2.92	7.35

###Diskussion förbättringsmöjligheter
optimizely.com Har den bästa sidan i testen enligt mig. Men man har ändå en del
att förbättra enligt *Insight*. Javascript som blockerar rendering cache och bildoptimering
skulle kunna göra sidan ännu bättre.


##Sammanfattning
Samtliga Webbsidor får väldigt låga betyg på Mobil testet. Alla hamnar under 60
och allra sämst är **Fz.se** som är nere på låga 48. På Datoroptmieringen går det lite bättre
Där är det istället **Nhl.com** som drar det kortaste strået på 64/100 i betyg.
Det som återkommer på samtliga *Insight* tester är Javascript som blockerar renderingen
bildoptimering samt att utnyttja cachelagringen.

##Rangordning
1. Optimizely.
2. FZ.
3. NHL.

**Optimizely** är den klara vinnaren. Med en angenäm laddningstid på 7.35s och bäst
totalpoäng på 129/200. Man har en lättöverskådlig startsida och har inte
lagt in förmycket content. Med det sagt har även dem förbättringsmöhligheter genom
bättre bildoptimering cachelagring och att ta bort Javascript som blockerar renderingen.

**FZ** Med god marginal upp men liten till sista platsen finner vi FZ. Lite förvånande
för mig då det är ett väldigt nördigt community. Man har lyckats hålla nere sidan till
3,87mb trots enligt mig alldeles förmycket bilder på startsidan. Laddninstiden ligger på
föga imponerande 27,17s och totalpoängen på 113/200. De kan absolut lägga ned mer tid
på bildoptimeringen där skulle de spara ca:10% på datan.

**NHL** På sistaplatsen i detta testet har vi NHL.com. Också en aning förvånande
då denna sida bör ha en väldigt stor budget bakom sig. Testets sämsta laddningstid
30.32s och en smockad startsida gjorde att jag tillslut valde att placera dem efter tvåan
Fz.se. De har tilltrotts att de hamnar sist i min lista aning bättre totalbetyg än Fz.
De landar på 121/200.  Man laddar in alldeles förmycket data med 12mb överlägset Testets
högsta med mer än tre gånger datan gentemot nästkommande.

##Snabbhet
Efter att ha kollat runt på lite sidor så känns ca **10s** som en bra laddningstid.
Den enda av mina testsidor som klarar det är **Optimizely**. De andra två faller utanför
med stor marginal och känns mycket riktigt, rent ut sagt, långsamma och lite irriterande.

##Grupp
Christofer Wikman
Jag skriver på distans och befinner mig just nu i Thailand. tidskillnad och
avstånd gör att jag gör denna uppgiften själv.
