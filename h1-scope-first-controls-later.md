# h1 - Scope first, Controls later

Tämä tehtäväraportti on tehty Tero Karvisen ja Lari Iso-Anttilan "Sovellusten Hakkerointi ja Haavoittuvuudet" -kurssille.

## a) Perustaso

Tässä tehtävässä laadin ISMS-soveltamisalan omalle kotiverkolleni/opiskelulabille, jota käytän kyseisellä kurssilla.

### 1. Mitä soveltamisalaan kuuluu? (Scope)

*Kotiverkko:*

| Perusinfra           | Laitteet kurssiharjoituksia varten | Tiedot     |
| -----------------    | ----------------------             | -------    |  
|  ASUS-kotireititin   | Custom pöytäkone                   | Github     |
|  Wi-Fi               | Kannettava tietokone               | Microsoft Authenticator |
|                      | Puhelin                            | Onedrive   |

Soveltamisalaani, tässä tapauksessa kotiverkkooni kuuluu:

Kotiverkossa käytössä oma Asuksen kotireititin, johon on kytketty paikallisesti, sekä Wi-Fin välityksellä laitteita, kuten puhelimeni, pöytäkoneeni (Windows 10) ja HP läppäri (Windows 11).
Kurssiharjoituksiin käytän enimmäkseen pöytäkonetta ja kannettavaa vain, kun teemme harjoituksia luokassa. Puhelinta, sekä Microsoft Authenticatoria tarvitsen kurssin Moodle-sivuille pääsyyn MFA-kirjautumisen avulla.
Virtuaalikoneet ajetaan VMWaren Workstation Pro:lla. Käytössä tällä hetkellä on Debian 13 ja Kali Linux.
Muistiinpanoja, harjoitusaineistoja, sekä kurssimateriaaleja säilytetään paikallisesti, sekä OneDrivessä minun hallinoimana. Raportit tallennetaan pilveen repositorioihini, joista ne linkataan Laksuun arvioitavaksi.


### 2. Out-of-scope

Rajasin soveltamisalalta ulos Äly-TV:n ja Chromecastin, sillä ne ovat merkityksettömiä kurssille. Tyttöystävän tietokoneen ja puhelimen rajasin ulos yksityisyyden takia, mutta myös, koska laitteet eivät kuulu minulle, eikä niille ole mitään tarvetta kurssin suorittamista varten. Mobiililaajakaista on myös rajattu pois, sillä hallittavuus Internetissä on palveluntarjoajan päässä. Wi-Fin mahdollisuus kotiverkossa myös tekee mobiiliverkosta tässä tapauksessa (kotona tai koululla) merkityksettömän. Myös Moodle on rajattu pois, sillä en ole vastuussa, tai hallinnassa sen sisällöstä.

| Laite/Palvelu | Ulosrajauksen syy|
| ----- | ------ |
| Chromecast | Merkityksetön |
| Tyttöystävän PC | Omistajuus |
| Tyttöystävän puhelin | Omistajuus |
| Äly-tv | Merkityksetön |
| Elisa mobiililaajakaista | Hallittavuus |
| Moodle | Hallittavuus |

### 3. Rajapinnat

Kotiverkossa käytössä Elisa Internet-palveluntarjoajana. Yhteys liikkuu Elisalta reitittimeeni, josta se kulkeutuu Wi-Fin ja Langallisen yhteyden kautta harjoituksille tarkoitettuihin laitteisiin.
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


