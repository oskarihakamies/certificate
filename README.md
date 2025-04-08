# certificate
Totally Legit Certificate - homework


x) 

## OWASP 2021: OWASP Top 10:2021

A01:2021 – Broken Access Control

- Oli noussut viidennelle sijalle web application haavoittuvuuksista. 
- Rikkinäinen pääsynhallinta kuvaa tilannetta, jossa käyttäjällä on pääsy tietoihin tai toimintoihin ilman oikeuksia. 
- Pääsee käsiksi API:in, kun puuttuu pääsynhallinta komennoille POST, PUT ja DELETE
- Voi estää mm. eri oikeuksien rajoittamisella eli least privileged tai rajoittaa API/ ohjaimeen pääsyä.
- Käytännössä pienen virheen takia hyökkääjä voi päästä koko järjestelmään käsiksi huonoimmissa tapauksissa.


A10:2021 – Server-Side Request Forgery (SSRF)

- Kyseessä on hyökkäys, joka tapahtuu kun web application hakee etäresurssia tarkistamatta URL-osoitetta
- Voidaan estää mm. kerroksittain OSI mallia katsoen. Päällimmäisenä tietysti network ja application layer. 
- Omasta mielestä hieman kiinnostavampi aihe lukea verrattuna näihin kahteen OWASP aiheeseen.

  

## PortSwigget Academy: 

Insecure direct object references (IDOR)

- Termi IDOR popularisoitui vuonna 2007 sen noustessa OWASP top teniin.
- Eli IDOR on pääsynhallinnan haavoittuvuus, joka ilmenee, kun sovellus käyttää käyttäjän antamaa syötettä päästäkseen suoraan käsiksi objekteihin.
- Ongelma ilmenee, kun sovellus luottaa liikaa siihen mihin käyttäjä voi päästä käsiksi.
- Tunnilla mainittu hyökkäys, jota oli mielenkiintoista kuunnella.


Path traversal

- Toiselta nimeltä tunnettu myös directory traversal, missä haavoittuvaisuus tapahtuu, kun sovellus ei tarkista käyttäjän antamaa syötettä kunnolla.
- PortSwiggerillä hyvin kuvattu miten hyökkäys mahdollistettaisiin mm. ../ lisäyksellä, joka lisäisi yhden path filen (tässä tapauksessa salasanoihin)
- Helpoin tapa estää hyökkäys aluksi on välttää kokonaan käyttäjän antaman syötteen välittäminen tiedostojärjestelmän API:in.
- Sen jälkeen (jos tätä ei voi välttää) on tuplatarkistaa se. Ensin validoi käyttäjän syöttämän tiedon ennen prosessoimista ja sitten liittää se perushakemistoon.
  

Server-side request forgery (SSRF)

- Menestynyt SSRF hyökkäys antaa hyökkääjälle pääsyn organisaation sisäiseen dataan.
- Hyödyntää usein luottamussuhteita laajentaakseen hyökkäystä haavoittuvasta sovelluksesta ja tehdäkseen luvattomia toimintoja. Luottamussuhteilla tarkoitetaan asiakkaan ja palvelimen välistä suhdettä usein.
- Sokeaa SSRF:ää on hankalampi hyödyntää, mutta joskus se voi johtaa täyteen etäkoodin suorittamiseen palvelimella tai muissa taustajärjestelmissä.
- PortSwiggerillä oli hyvää visualisointia, miten hyökkääjä voi käyttää SSRF hyökkäyksiä serveriä vastaan.


Cross-site scripting (XSS)

- Toimii, kun haavoittuvaa sivua manipuloidaan siten, että se palauttaa haitallista JavaScriptiä takaisin käyttäjälle.
- Kolme "pää" XSS hyökkäystä, jossa reflected XSS hyökkäyksessä haitallinen skripti tulee tämänhetkisestä HTTP-pyynnöstä.
- Kaksi muuta ovat Stored XSS ja DOM-based XSS. Stored XSS hyökkäyksessä skripti on peräisin tietokannasta ja dom-based XSS taas haavoittuvaisuus on asiakas eli client-side puolelta.
- XSS on yksi hyökkäys, josta itse olin kuullut/tiennyt eniten. Tietenkin lisäystä tietoon aina tarvitaan.


a)

Totally Legit Certificate:

Asensin ZAP:in komennolla sudo apt-get install zaproxy kaliin ihan alkuun

<img width="315" alt="image" src="https://github.com/user-attachments/assets/45890f7c-98f1-447b-9111-7bc480c99e7c" />

Ja käynnistin sen zaproxy & komennolla. 

<img width="423" alt="image" src="https://github.com/user-attachments/assets/ac29e51f-0bb0-406a-81bf-8204510e50fc" />

Tunnilta muistin sertifikaattien ollen network kohdassa. 

<img width="122" alt="image" src="https://github.com/user-attachments/assets/f06ded93-76cb-422a-8c7d-783eccbaf31e" />

Tallensin generoimani sertifikaatin koneelleni:

<img width="271" alt="image" src="https://github.com/user-attachments/assets/ca5ebae9-1718-4c1b-9c64-f506f8976616" />










## Yhteenveto


# references

OWASP 2021: OWASP Top 10:2021, A01:2021 – Broken Access Controlhttps://owasp.org/Top10/A01_2021-Broken_Access_Control/
OWASP 2021: OWASP Top 10:2021, A10:2021 – Server-Side Request Forgery (SSRF) https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29/
PortSwigger: Insecure direct object references (IDOR), https://portswigger.net/web-security/access-control/idor



