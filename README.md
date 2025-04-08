# certificate
Totally Legit Certificate - homework


x) 

## OWASP 2021: OWASP Top 10:2021

A01:2021 – Broken Access Control

- Oli noussut viidennelle sijalle web application haavoittuvuuksista. 
- Rikkinäinen pääsynhallinta kuvaa tilannetta, jossa käyttäjällä on pääsy tietoihin tai toimintoihin ilman oikeuksia. 
- Pääsee käsiksi API:in, kun puuttuu pääsynhallinta komennoille POST, PUT ja DELETE
- Voi estää mm. eri oikeuksien rajoittamisella eli least privileged tai rajoittaa API/ ohjaimeen pääsyä. 


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
- Voidaan estää 



## Yhteenveto


# references

OWASP 2021: OWASP Top 10:2021, A01:2021 – Broken Access Controlhttps://owasp.org/Top10/A01_2021-Broken_Access_Control/
OWASP 2021: OWASP Top 10:2021, A10:2021 – Server-Side Request Forgery (SSRF) https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29/


