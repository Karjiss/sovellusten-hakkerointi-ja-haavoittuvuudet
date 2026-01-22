# h2 - Break & Unbreak

## Käyttöympäristö

- Käyttöjärjestelmä: Microsoft Windows 10 Home
- Emolevy: Gigabyte Z170-Gaming K3
- Prosessori: Intel i5-6600K
- Näytönohjain: NVIDIA GeForce RTX 2060
- RAM: 16 GB DDR4
- Virtualisointiohjelmisto: VMWare Workstation Pro
- Virtuaalikone: Kali Linux

## x) Tiivistä

### OWASP Top 10 - Broken Access Control (OWASP)

- Huono pääsynvalvonta antaa käyttäjille liikaa oikeuksia, joka voi johtaa vakaviin vahinkoihin.
- Deny by default on oletusarvoinen kielto, jolla automaattisesti estetään pääsy kaikkiin resursseihin oikeudettomilta käyttäjiltä.

### Find Hidden Web Directories - Fuzz URLs with ffuf (Karvinen 2023)

- Ffuf käyttää sanalistoja löytääkseen esimerkiksi piilotettuja sivuja palvelimelta.
- Voit myös tarkentaa hakua suodattamalla ei haluttuja vastauksia pois.

### Portswigger - Access Control (Portswigger Ltd)

- Pääsynhallinnan (Access Control) suunnittelun päätökset on aina ihmisten tekemiä, joten virheiden mahdollisuus on suuri.
- Pääsynhallintaa tehtäessä pitäisi aina auditoida ja testata toimivuus kunnolla.

### Raportin kirjoittaminen (Karvinen 2006)

 - Raportin tulee olla täsmällinen, toistettava sekä helppolukuinen.


## a) Break into 010-staff-only

Tässä tehtävässä murtaudutaan sovellukseen, sekä korjataan haavoittuvuus.

Käytin apuna Karvisen artikkelia ["Hack'n Fix"](https://terokarvinen.com/hack-n-fix/) vuodelta 2014.
