# h1 - Scope first, Controls later

Tämä tehtäväraportti on tehty Tero Karvisen ja Lari Iso-Anttilan "Sovellusten Hakkerointi ja Haavoittuvuudet" -kurssille.

## a) Perustaso

Tässä tehtävässä laadin ISMS-soveltamisalan omalle kotiverkolleni/opiskelulabille, jota käytän kyseisellä kurssilla.

### 1. Mitä soveltamisalaan kuuluu? (Scope)

*Kotiverkko:*

| Perusinfra           | Laitteet kurssiharjoituksia varten | Tiedot     |
| -----------------    | ----------------------             | -------    |  
| ASUS-kotireititin    | Custom pöytäkone                   | Github     |
|  Puhelin             | Kannettava tietokone               | Moodle     |
|  Wi-Fi               |                                    | Onedrive   |
|                      |                                    | Authenthicator |

Soveltamisalaani, tässä tapauksessa kotiverkkooni kuuluu:

Asuksen kotireititin, johon on kytketty paikallisesti, sekä Wi-Fin välityksellä laitteita, kuten puhelimeni, pöytäkoneeni (Windows 10) ja HP läppäri (Windows 11).

Kurssiharjoituksiin käytetään enimmäkseen pöytäkonetta, sillä siinä on eniten tehoa. Puhelinta tarvitsen koulun sivuille kirjautumiseen (Moodle).

Virtuaalikoneet ajetaan VMWaren Workstation Pro:lla. Käytössä tällä hetkellä on Debian 13 ja Kali Linux.

Muistiinpanoja, harjoitusaineistoja, sekä kurssimateriaaleja säilytetään paikallisesti, sekä OneDrivessä. Raportit tallennetaan pilveen repositorioihini.

### 2. Out-of-scope

Rajasin soveltamisalalta ulos Äly-TV:n ja Chromecastin, sillä ne ovat merkityksettömiä kurssille. Tyttöystävän tietokoneen ja puhelimen rajasin ulos, koska laitteet eivät kuulu minulle.

| Laite | Ulosrajauksen syyt |
| ----- | ------|
| Chromecast | Merkityksetön |
| Tyttöystävän PC | Omistajuus, hallittavuus |
| Tyttöystävän puhelin | Omistajuus, hallittavuus |
| Äly-tv | Merkityksetön |
