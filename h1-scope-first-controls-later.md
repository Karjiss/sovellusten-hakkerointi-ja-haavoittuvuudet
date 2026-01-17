# h1 - Scope first, Controls later

Tämä tehtäväraportti on tehty Tero Karvisen ja Lari Iso-Anttilan "Sovellusten Hakkerointi ja Haavoittuvuudet" -kurssille.

## a) Perustaso

Tässä tehtävässä laadin ISMS-soveltamisalan omalle kotiverkolleni/opiskelulabille, jota käytän kyseisellä kurssilla.

### 1. Mitä soveltamisalaan kuuluu? (Scope)

**In Scope:**

| Kotiverkon infra     | Laitteet kurssiharjoituksia varten | Tiedot/Data |
| -----------------    | ----------------------             | -------    |  
|  ASUS-kotireititin   | Custom pöytäkone                   | Github     |
|  Wi-Fi               | Kannettava tietokone               | Microsoft Authenticator |
|  RJ-45-verkkokaapeli | Puhelin                            | Onedrive   |

Soveltamisalaani, tässä tapauksessa kotiverkkooni kuuluu:

Kotiverkossa käytössä oma Asuksen kotireititin, johon on kytketty paikallisesti, sekä Wi-Fin välityksellä laitteita, kuten puhelimeni, pöytäkoneeni (Windows 10) ja HP läppäri (Windows 11).
Kurssiharjoituksiin käytän enimmäkseen pöytäkonetta ja kannettavaa vain, kun teemme harjoituksia luokassa. Puhelinta, sekä Microsoft Authenticatoria tarvitsen kurssin Moodle-sivuille pääsyyn MFA-kirjautumisen avulla.
Virtuaalikoneet ajetaan VMWaren Workstation Pro:lla. Käytössä tällä hetkellä on Debian 13 ja Kali Linux.
Muistiinpanoja, harjoitusaineistoja, sekä kurssimateriaaleja säilytetään paikallisesti, sekä OneDrivessä minun hallinnoimana. Raportit tallennetaan pilveen repositorioihini, joista ne linkataan Laksuun arvioitavaksi.


### 2. Out-of-scope

Rajasin soveltamisalalta ulos Äly-TV:n ja Chromecastin, sillä ne ovat merkityksettömiä kurssille. Tyttöystävän tietokoneen ja puhelimen rajasin ulos yksityisyyden takia, mutta myös, koska laitteet eivät kuulu minulle, eikä niille ole mitään tarvetta kurssin suorittamista varten. Mobiililaajakaista, sekä laajakaista on myös rajattu pois, sillä hallittavuus laajakaistoissa on palveluntarjoajan päässä. Wi-Fin mahdollisuus kotiverkossa myös tekee mobiiliverkosta tässä tapauksessa (kotona tai koululla) merkityksettömän. Myös Moodle on rajattu pois, sillä en ole vastuussa, tai hallinnassa sen sisällöstä. 

**Out-of-scope:**
| Laite/Palvelu | Ulosrajauksen syy|
| ----- | ------ |
| Chromecast | Merkityksetön |
| Tyttöystävän PC | Omistajuus |
| Tyttöystävän puhelin | Omistajuus |
| Äly-tv | Merkityksetön |
| Elisa mobiililaajakaista | Hallittavuus |
| Elisa laajakaista | Hallittavuus |
| Moodle | Hallittavuus |

### 3. Rajapinnat

Kotiverkossa käytössä Elisa Internet-palveluntarjoajana. Yhteys liikkuu Elisalta reitittimeeni, josta se kulkeutuu Wi-Fin ja langallisen yhteyden kautta harjoituksille tarkoitettuihin laitteisiin.
Verkkoyhteys kulkee sisään, sekä ulos. Reitittimen sisäänrakennettu palomuuri suojaa kotiverkkoani uhkilta, sillä tehdasasetuksillakin reitittimessä on palomuuri päällä, sekä se ei vastaa automaattisiin skannauksiin Internetistä.

Github, Moodle sekä Onedrive ovat kaikki keskeisiä rajapintoja kurssia varten, sillä näissä palveluissa on kaikki tiedot ja materiaali kurssin suorittamista varten.

Pilvipalveluita minun kotiverkkooni tarjoaa:

| Toimittaja | Palvelu |
| -----|----- |
| Microsoft Onedrive | Tiedostojen säilytykseen |
| Github | Kurssiraportteja varten tehtävien raporttien säilytys |
| Moodle | Kurssin materiaalit |

Muita toimittajia ovat:
|Toimittaja | Palvelu |
|-----|-----|
| Apple | Puhelimen valmistaja |
| Hewlett Packard | Kannettavan tietokoneen valmistaja |
| Asus | Kotireitittimen valmistaja |
| Elisa | Internet-palveluntarjoaja |

**Verkko- ja rajapintakaavio:**

<img width="768" height="626" alt="image" src="https://github.com/user-attachments/assets/86db0623-798b-4e98-9e99-aa8160587ddf" />

### Mitä näyttöä voisin esittää?


Reitittimen palomuuriasetukset todistavat, että reitittimellä on palomuuri käytössä, sekä ICMP echo pois käytöstä. (Kuva 1.)

<img width="1007" height="865" alt="image" src="https://github.com/user-attachments/assets/62755d5a-5c7e-4876-b118-27ab37443f9f" />

MFA-pyyntö kirjautuessa Moodleen. (Kuva 2.) 

<img width="950" height="626" alt="image" src="https://github.com/user-attachments/assets/2ef31fd0-47ce-4e4e-a23d-fe79e4a326f5" />

Kotiverkon clientit, MAC-osoitteet piilotettu. (Poislukien chromecast, joka on harvoin päällä). (Kuva 3.)

<img width="522" height="601" alt="image" src="https://github.com/user-attachments/assets/2b9fea7c-c62a-4873-9c00-7a1722113b0c" />

VMWaren virtuaalikoneet. (Kuva 4.)

<img width="426" height="97" alt="image" src="https://github.com/user-attachments/assets/20e8d0e7-aef1-4d5a-ba83-dcd28f27ba38" />

## b) Sidotaan Standardiin

Tässä tehtävässä loin taulukon, joka sitoo opiskelulabrani/kotiverkkoni sidosryhmät ISO 27001 -standardiin:

| Sidosryhmä | Tarve/Vaatimus | ISO27001 -viite | Näyttö |
| ---------- | -------------- | --------------- | ------ |
| Oppilaitos |  Lain ja sääntöjen mukaan toimiminen harjoitustyökalujen kanssa. | 4.2 (Sidosryhmien tarpeiden ja odotusten ymmärtäminen) | Hyväksytty kurssin säännöt |
| Oppilaitos |  Harjoitukset on tehtynä ajallaan ja oikein. | 9.1 (Seuranta, mittaaminen, analysointi ja arviointi) | Tämä tehtävä, sekä tulevat tehtävät palautettuna |
| Minä itse | Pyrin parantamaan labrani turvallisuutta kurssin edetessä. | 9.3 (Johdon katselmus) ja 10.2 (Jatkuva parantaminen) | Reitittimen lokitiedot ja kurssin dokumentaatio |

## Lähteet

Iso-Anttila, L & Karvinen, T. 2026. Sovellusten Hakkerointi ja Haavoittuvuudet - Kurssi. Luettavissa: https://terokarvinen.com/application-hacking/

Iso-Anttila, L. & Karvinen, T. 2026. Standardit. Sovellusten hakkerointi ja haavoittuvuudet - Moodlen materiaalit. Haaga-Helia ammattikorkeakoulu. Luettu 15.1.2026.

