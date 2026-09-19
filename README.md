# veebiprojekt


## 1. Meeskonnaliikmed ja rollid

| Sofija Beljakova | GitHub Admin | Frontend & Test Lead |

---

## 2. Valitud serverivariant ja põhjendus 

* Render.com (Static site)
*  Valisin Render.com-i, kuna see on kõige tõhusam ja kiirem viis staatilise veebisaidi (HTML/CSS) juurutamiseks ilma virtuaalsete privaatserverite (VPS), SSH-võtmete või võrgutunnelite seadistamise vajaduseta. Platvorm võtab kogu hostimisega seotud rutiini enda kanda ja tagab automaatse pideva juurutamise (Continuous Deployment) iga kord, kui reporitooriumis tehakse muudatusi.

---

## 3. Serverinfo ja tehniline teave 

* **Hostimisplatvorm:** Render.com (Static Site Hosting)
* **URL:** `(https://veebiprojekt-725r.onrender.com/)`
* **Deploy branch:** `main`
* **Publish directory:** `public`

---

## 4. SSH seadistuse staatus 

* Render.com puhul ei ole klassikalisi SSH-võtmeid ega GitHub Secrets'e vaja, kuna integratsioon toimub otse Renderi teenuse autoriseerimise ja veebikonksude (webhooks) kaudu GitHubiga. Automaatne juurutamine on seadistatud „karbist välja“ kujul Pull Requesti ühendamisel (merge) main haruga.
---

## 5. Tekkinud probleemid ja lahendused

Töö käigus põrkasin kokku mitmete nüanssidega ja lahendasin need edukalt::
1. **Probleem Not Found (404) veaga esmasel juurutamisel:**
   * *Põhjus:* Render otsis faile vaikimisi repositooriumi juurkataloogist.
   * *Lahendus:* Kontrollisime projekti struktuuri ja veendusime, et failid index.html ja style.css asuvad rangelt public/ kausta sees ning Renderi seadetes on väljal Publish directory määratud väärtus public. Pärast käsitsi taaskäivitamist (Manual Deploy) hakkas veebileht edukalt tööle.


