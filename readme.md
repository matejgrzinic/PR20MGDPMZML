# Igre spletne trgovine Steam

## Avtorji
* Matej Gržinič
* Matej Lavrenčič
* Metod Zupančič
* Denis Popović

## Podatki
* steam.csv - Glavni podatki igre
* steam_description_data.csv - Opis igre
* steam_media_data.csv - slike igre
* steam_requirements_data.csv - minimalne in priporočljive strojne zahteve naprave glede na operacijski sistem
* steam_support_info.csv - povezave za pomoč uporabnikom igre
* steamspy_tag_data.csv - Lastnostne oznake igre


## Uvod 

Zanima nas katere igre so najboljše ali najpopularnejše in kateri razvijalci, žanri in tipi iger prevladujejo v (trenutno) najbolj popularni spletni trgovini "*Steam*". Kaj se je obdržalo skozi čas in kaj ne, kakšni so trendi in kako je s cenami iger. Poiskati želimo najbolj pomembne lastnosti uspešnosti iger.
   
Podatke smo dobili na spletni strani kaggle (https://www.kaggle.com/nikdavis/steam-store-games).

<br>
<br>

## Predstavitev vseh iger glede na kategorijo, razvijalce, uspešnost in trenutno igranost

### Kategorije

<img src="laurencicSlike\categories.png" alt="gameByCategory" width="769"/>

Graf prikazuje vse kategorije in koliko iger jim pripada. 

### Izdajalci
<img src="laurencicSlike\developer.png" alt="gameByDeveloper" width="769"/>

Graf prikazuje izdajalce (10), ki imajo največ iger.

### Uspešnost
1) "*Dota 2*"
2) "*PLAYERUNKNOWN'S BATTLEGROUNDS*"
3) "*Counter-Strike: Global Offensive*"
4) "*Unturned*"
5) "*Warframe*"
6) "*Team Fortress 2*"
7) "*Z1 Battle Royale*"
8) "*Heroes & Generals*"
9) "*Warface*"
10) "*Grand Theft Auto V*"

 Prikazane igre (10), so tiste, ki imajo največjo uspešnost. Za izračunat uspešnost ene igre sem najprej pridobil vrednost pozitivnih ocen v odstodkih (glede na skupne ocene) in nato delil z lastniki igre. Manjša je izračunana vrednost, večja je uspešnost igre.

### Trenutno igranost  
<img src="laurencicSlike\playtime.png" alt="gameByPlaytime" width="769"/>

Graf prikazuje igre (10), ki imajo največji "median_playtime" podatek, s katerim preverimo, katere igre imajo najvišjo igranost.

<br>
<br>

## Predstavitev žanrov

<img src="zupancicSlike\general_genres.png" alt="" width="769"/>

**Levi graf** prikazuje histogram žanrov iger nefiltriranih podatkov.<br>
Prvi 3 najboljši žanri iger so: "*Indie*", "*Action*", "*Casual*"<br>



**Desni graf** prikazuje histogram žanrov iger, katerih lastništvo je bilo večje od razpona 0-20000.<br>
Prvi 3 najboljši žanri iger so: "*Indie*", "*Action*", "*Adventure*"<br>
Glede na levi graf pa je razvidno manjša razlika med prvima dvema žanroma, kar pove, da je dober delež "*Indie*" iger nepopularen vsaj iz lastnosti števila nakupov igre.

<br>

<img src="zupancicSlike\best50_byOwner.png" alt="" width="769"/>

Graf prikazuje porazdelitev 50 najboljših iger (iz vidika največjega števila nakupov igre)
<br>
Prvi 3 najboljši žanri izbranih so: "*Action*", "*Free to play*", "*Indie*"

<br>
<br>

## Povezava med ceno igre in razmerjem dobrih in slabih ocen

<img src="grzinicSlike\white_notblack.png" alt="" width="769"/>

Na grafu lahko na x osi vidimo ceno iger in na y osi razmerje ocen izračunano po formuli positive / (positive + negative). Že iz grafa lahko odčitamo, da dražja kot je igra bolj verjetno je, da bodo igralci imeli pozitivno mnenje. Na grafu je dodana tudi premica, ki prikazuje kako so podatki razdeljeni. 

<br>
<br>

## Najbolj popularni razvijalci


Najbolj popularni razvijalci so tisti, ki imajo največje število privržencev (število prodanih kopij vseh njihovih iger). Tukaj ne potrebujemo pregledovati popularnosti vsake igre, saj se v igričarski industriji velikokrat zgodi, da razvijalci izdajo dobro ali slabo igro. Važno je, da jih ljudje poznajo oz., da posedujejo njihovo igro. 
<br><br>

<img src="popovicSlike\plt2.png" alt="" width="769"/>
<br>
<br>
<img src="popovicSlike\plt3.png" alt="" width="769"/>

Iz zgornjih grafov lahko presodimo, da popularnost razvijalca ni odvisna od števila izdanih iger in ali je igra brezplačna, ali plačljiva. Npr.: "*PUBG Corporation*" in "*Smartly Dressed Games*" imata izdano samo po eno igro, pri tem da je prva plačljiva, druga pa ne, a sta oba razvijalca še vedno v zgornjih 10 po lestvici. <br>

"*Feral Interactive*" pa v številu iger zelo odstopa od drugih razvijalcev zato, ker sodeluje z drugimi razvijalci na različnih platformah npr.:("*Linux*", "*MacOs*", "*iOS*", "*Android*"). Posledično je v podatkih zato tako veliko število izdanih iger.


Glede na popularnost je razvijalec "*Valve*" v ogromni prednosti pred drugimi. Podatkovna baza pripada "*Steam*" spletni trgovini, ki pa pripada razvijalcu "*Valve*". Obstajajo tudi druge spletne trgovine, ki so (do sedaj) vse manjše, zato popularnost razvijalca kljub morebitni pristranskosti podatkov ni zgrešena.


## Korelacija

<img src="popovicSlike\plt4_corr.png" alt="" width="769"/>

Kot vidimo iz slike je korelacija med atributi zelo slaba. Večje korelacije so med avg_playtime - median_playtime in developer - publisher, kar je smisleno. Atributa Owners (št. prodanih kopij) in reviews (št. kritik) sta tudi v močni korelaciji, saj z večjim številom ljudi, ki je kupilo igrico raste tudi število kritik.

## Napovedovanje števila igralcev

Za X množico smo pustili le atribute ["average_playtime", "median_playtime", "price", "achievements", "positive_ratings", "negative_ratings", "required_age", "english"]

| Razpon števila igralcev  | količina |
|-------------|:-------------|
|0-20000| 18596|
 |20000-50000| 3059|
 |50000-100000| 1695|
 |100000-200000| 1386|
 |200000-500000| 1272|
 |500000-1000000| 513|
 |1000000-2000000| 288|
 |2000000-5000000| 193|
 |5000000-10000000| 46|
 |10000000-20000000| 21|
 |20000000-50000000| 3|
 |50000000-100000000| 2|
 |100000000-200000000| 1

**Celotna podatkovna baza** 

| Model  | točnost | povprečna absolutna napaka |
|-------------| :-------------: | :-------------: |
| večinski  | 0.688  | 117628  |
| GaussianNB  | 0.683  | 190052 |
| DecisionTreeClassifier | 0.699 | 136991 |
| KNeighborsClassifier (k = 3) | 0.688 | 109479 |
| KNeighborsClassifier (k = 5) | 0.698 | 105057 | 
| KNeighborsClassifier (k = 7) | 0.708 | 98506 |
| svm |0.707 | 109438 | 

<br>

**Brez upoštevanja iger z manj kot 20000 igralci**

<br>

| Model  | točnost | povprečna absolutna napaka |
|-------------| :-------------: | :-------------: |
| večinski  | 0.337  | 463691  |
| GaussianNB  | 0.314  | 482595 |
| DecisionTreeClassifier | 0.369 | 388465 |
| KNeighborsClassifier (k = 3) | 0.372 | 326908 |
| KNeighborsClassifier (k = 5) | 0.386 | 319793 | 
| KNeighborsClassifier (k = 7) | 0.391 | 296162 |
| svm |0.384 | 407363 |

Glede na dobljene rezultate sklepamo, da je napovedovanje že zaradi slabih korelacij prejšnje analize med atributi ni efektivno s povprečno točnostjo napovedovanja različnih modelov okoli 70%. Ob filtriranju le bolj relevantnih podatkov točnost upade na povprečno 30% natančnost, ker ima največji delež iger manj kot 20000 igralcev.


## Podatki skozi čas

<img src="popovicSlike\plt5_earlyAccesThroughTime.png" alt="" width="769"/><br>
<img src="popovicSlike\plt6_indieThroughTime.png" alt="" width="769"/><br>
<img src="popovicSlike\plt7_freeThroughTime.png" alt="" width="769"/><br>

Za izris grafov skozi čas smo vzeli najbolj značilne vplivne žanre ali lastnosti.<br>
Indie in Early Access sta dosegla najvišje rasti. 


## Povprečna cena

<img src="zupancicSlike\pricePerCategory.png" alt="" width="769"/><br>

<img src="zupancicSlike\pricePerGenre.png" alt="" width="769"/><br>


