# Projektna naloga

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

</br>
</br>

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

</br>
</br>

## Predstavitev žanrov

<img src="zupancicSlike\general_genres.png" alt="" width="769"/>

**Levi graf** prikazuje histogram žanrov iger nefiltriranih podatkov.</br>
Prvi 3 najboljši žanri iger so: "*Indie*", "*Action*", "*Casual*"</br>



**Desni graf** prikazuje histogram žanrov iger, katerih lastništvo je bilo večje od razpona 0-20000.</br>
Prvi 3 najboljši žanri iger so: "*Indie*", "*Action*", "*Adventure*"</br>
Glede na levi graf pa je razvidno manjša razlika med prvima dvema žanroma, kar pove, da je dober delež "*Indie*" iger nepopularen vsaj iz lastnosti števila nakupov igre.

</br>

<img src="zupancicSlike\best50_byOwner.png" alt="" width="769"/>

Graf prikazuje porazdelitev 50 najboljših iger (iz vidika največjega števila nakupov igre)
</br>
Prvi 3 najboljši žanri izbranih so: "*Action*", "*Free to play*", "*Indie*"

</br>
</br>

## Povezava med ceno igre in razmerjem dobrih in slabih ocen

<img src="grzinicSlike\white_notblack.png" alt="" width="769"/>

Na grafu lahko na x osi vidimo ceno iger in na y osi razmerje ocen izračunano po formuli positive / (positive + negative). Že iz grafa lahko odčitamo, da dražja kot je igra bolj verjetno je, da bodo igralci imeli pozitivno mnenje. Na grafu je dodana tudi premica, ki prikazuje kako so podatki razdeljeni. 

</br>
</br>

## Najbolj popularni razvijalci


Najbolj popularni razvijalci so tisti, ki imajo največje število privržencev (število prodanih kopij vseh njihovih iger). Tukaj ne potrebujemo pregledovati popularnosti vsake igre, saj se v igričarski industriji velikokrat zgodi, da razvijalci izdajo dobro ali slabo igro. Važno je, da jih ljudje poznajo oz., da posedujejo njihovo igro. 
</br></br>

<img src="popovicSlike\plt2.png" alt="" width="769"/>
</br>
</br>
<img src="popovicSlike\plt3.png" alt="" width="769"/>

Iz zgornjih grafov lahko presodimo, da popularnost razvijalca ni odvisna od števila izdanih iger in ali je igra brezplačna, ali plačljiva. Npr.: "*PUBG Corporation*" in "*Smartly Dressed Games*" imata izdano samo po eno igro, pri tem da je prva plačljiva, druga pa ne, a sta oba razvijalca še vedno v zgornjih 10 po lestvici. </br>

"*Feral Interactive*" pa v številu iger zelo odstopa od drugih razvijalcev zato, ker sodeluje z drugimi razvijalci na različnih platformah npr.:("*Linux*", "*MacOs*", "*iOS*", "*Android*"). Posledično je v podatkih zato tako veliko število izdanih iger.


Glede na popularnost je razvijalec "*Valve*" v ogromni prednosti pred drugimi. Podatkovna baza pripada "*Steam*" spletni trgovini, ki pa pripada razvijalcu "*Valve*". Obstajajo tudi druge spletne trgovine, ki so (do sedaj) vse manjše, zato popularnost razvijalca kljub morebitni pristranskosti podatkov ni zgrešena.