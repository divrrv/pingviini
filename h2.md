# pingviini
Repositorio tehtävälle h2


# h2 Komentaja Pingviini

## Linux komentorivin perusteet (tiivistelmä) 27.1 14:25

Komentorivillä voit esimerkiksi asentaa ohjelmia ja tarkastella tiedostojen sisältöä sekä liikkua tiedostojen välillä.
Tällä komennolla näet missä kohdassa tiedostoja olet:

        pwd


## Tehtävä

Tehtävässä asennan micro-editorin, listaan koneen raudan, asennan 3 komentoriviohjelmaa, näytän kansioiden sisältöjä sekä muutaman kuvaavan esimerkin grep-komennon käytöstä.

Avaan virtaalikoneen ja terminaalin.

Aloitan lataamalla micro-editorin komennoilla:

    sudo apt-get update

    sudo apt-get install micro

![11](https://user-images.githubusercontent.com/112497215/213946557-36ebcab7-c5ad-4557-bc6a-5eb25e15cacb.PNG)

Tämän jälkeen lataan lshw:n komennolla:

    sudo apt-get install lshw
 
ja listaan koneen raudan komennolla: 
 
    sudo lshw -short -sanitize
  
  Tulostuksesta näemme tarkemmat tiedot koneestani mm. muistien määrät, processorin mallin sekä systeemin.
  
![22](https://user-images.githubusercontent.com/112497215/213946562-30c91b22-77ad-48b7-a806-579d4ea7990b.PNG)

Seuraavaksi asennan 3 komentoriviohjelmaa, asensin tree, python3 ja figlet ohjelmat komennolla:

    sudo apt-get install tree python3-py figlet
 
 
![333](https://user-images.githubusercontent.com/112497215/213946568-0f0137a2-c779-44c6-93ec-b202c8051f4f.PNG)

figlet muotoilee haluamasi tekstin suureksi kokonaisuudeksi.

![44](https://user-images.githubusercontent.com/112497215/213946579-5694734f-9455-401c-b31e-3c503795e2a0.PNG)

tree listaa kansiot ja niiden sisältämät tiedostot nimien kanssa.

![444](https://user-images.githubusercontent.com/112497215/213946582-fc5620cc-cfaf-4261-a01c-8905df48840a.PNG)

python3:ssa voit suorittaa python koodia.

![4444](https://user-images.githubusercontent.com/112497215/213946588-a0f3820f-e801-4339-8774-b0141db93cc1.PNG)

Tässä osiossa esittelen eri kansiot, jotka olivat listattuna  "Command Line Basics Revisited" kappaleessa "Important directories" osoitteessa: https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited

home/

![5](https://user-images.githubusercontent.com/112497215/213946598-a0c0263c-b3d1-49d0-a2b5-8ca547133f5d.PNG)

home/user/

![55](https://user-images.githubusercontent.com/112497215/213946600-b8394311-86a0-42ed-90b3-15a710752586.PNG)

etc/

![555](https://user-images.githubusercontent.com/112497215/213946603-96bed7c4-d910-4ed8-a3c1-469b9eb91eac.PNG)


![5555](https://user-images.githubusercontent.com/112497215/213946605-b448b7e6-6864-45aa-be0c-570a34f4f2eb.PNG)

media/

![55555](https://user-images.githubusercontent.com/112497215/213946612-a110165e-d6f6-40f3-a5fd-f277526162e1.PNG)

var/log/

![555555](https://user-images.githubusercontent.com/112497215/213946616-71453c2d-c5ee-4ea9-8bca-9b02c2707d12.PNG)

Viimeiseksi näytän muutaman esimerkin grep-komennon käytöstä.

![5555555](https://user-images.githubusercontent.com/112497215/213946619-73772446-a56c-4e36-a74d-4d90a03767e3.PNG)



# h3 Vapaus

## x) 27.1 14:41

Vapaassa ohjelmassa saat oikeuden ajaa, kopioda, levittää, opiskella ja kehittää ohjelmistoa.

Avoimen lähdekoodin ohjelmistot ovat melkein kuin vapaat ohjelmistot, mutta hieman eroavalla lisenssillä.



## a)
Koitin etsiä kaikkiin kolmeen github sivut, mutta python ja tree osoittautuivat haasteeksi löysin kuitenkin wikipediasta treen lisenssin ja pythonin omilta sivuilta pythonin lisenssin.

### Tree
GNU General Public License, version 2

Vapaa lisenssi

Lisenssi antaa vapaat muokkaus ja käyttö oikeudet

![image](https://user-images.githubusercontent.com/112497215/214563718-974e4d38-44e4-4860-9076-f15835736efe.png)

### Figlet

![image](https://user-images.githubusercontent.com/112497215/214563868-267e930b-5c9f-421c-95ff-3f35d0eef7e8.png)
![image](https://user-images.githubusercontent.com/112497215/214669725-a37c99bf-d979-4006-91e6-82583cd183b3.png)


### Python3

Python Software Foundation License Version 2

Vapaa lisenssi

Lisenssi antaa vapaat muokkaus, kopiointi, jako ja käyttö oikeudet


## b)

komento tulostaa sanat jotka sisältävät e kirjaimen.

        cat testitesti.md |grep -P -o '\S+e\S+'
![image](https://user-images.githubusercontent.com/112497215/214665282-6d45f5df-89a4-420c-a7a3-c0fae1e51a16.png)




## c)

tulostaa tiedoston tiedoston

        cat testi.md
        
![image](https://user-images.githubusercontent.com/112497215/214666591-70d5f5be-a860-48bb-9b60-e6c68c59610f.png)

jäejestää sisäsällön aakkosjärjestykseen

        cat testi.md | sort
        
![image](https://user-images.githubusercontent.com/112497215/214666656-8d27858f-1684-46cf-a125-7319b171ee14.png)

toistaa yllä mainitun komennon, mutta lisänä poistaa toistuvat sanat

        cat testi.md | sort | uniq
        
![image](https://user-images.githubusercontent.com/112497215/214666719-79489a3a-aa10-4faf-b957-ee6e6ff0e040.png)

tulostaa 4 viimeistä riviä

        cat testi.md |head -4
        
![image](https://user-images.githubusercontent.com/112497215/214666763-8d178164-82cf-4ee0-aa3a-930a813946d0.png)




## Lähteet:
https://terokarvinen.com/

https://linuxhint.com/linux-pipe-command-examples/

https://docs.python.org/3/license.html


## The End
