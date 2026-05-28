<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:00f2ff&height=120&section=header&text=&fontSize=0)

</div>

# ð§ Ãtude Comparative et DÃ©ploiement : Serveurs de Messagerie Open-Source

<div align="center">

![iRedMail](https://img.shields.io/badge/iRedMail-FF6600?style=for-the-badge&logo=mail.ru&logoColor=white) ![Linux](https://img.shields.io/badge/Linux_Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white) ![Postfix](https://img.shields.io/badge/Postfix-CC0000?style=for-the-badge&logo=gmail&logoColor=white) ![DKIM](https://img.shields.io/badge/DKIM_SPF_DMARC-Email_Security-00b4d8?style=for-the-badge) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

![Efrei](https://img.shields.io/badge/Efrei_Bordeaux-Mastère_Cybersécurité-purple?style=flat-square) ![Type](https://img.shields.io/badge/Type-Infrastructure_&_Déploiement-green?style=flat-square) ![Status](https://img.shields.io/badge/Status-Terminé-success?style=flat-square)

</div>

> **Sujet :** Analyse de solutions d'auto-hÃ©bergement et mise en Åuvre de la solution iRedMail.

---

## ð¯ 1. Objectifs du Projet
L'objectif principal est de rÃ©aliser une **Ã©tude comparative** des serveurs de messagerie open-source actuels afin d'identifier la solution offrant le meilleur compromis entre **sÃ©curitÃ©**, **performance** et **facilitÃ© d'administration** pour un environnement professionnel.

---

## ð 2. Ãtude Comparative des Solutions
Nous avons Ã©valuÃ© cinq solutions majeures du marchÃ© selon des critÃ¨res techniques prÃ©cis :

| Solution | Installation | Interface (UI) | SÃ©curitÃ© (DKIM, SPF, DMARC) | Public Cible |
| :--- | :--- | :--- | :--- | :--- |
| **Mailcow** | BasÃ© sur Docker, moyennement complexe | Moderne et intuitive (calendriers, contacts) | TrÃ¨s complÃ¨te avec anti-virus avancÃ© | Moyennes Ã  grandes entreprises |
| **Mail-in-a-Box** | TrÃ¨s simple (quelques commandes) | SimplifiÃ©e mais basique | Bonne (inclut DNSSEC) | Petites entreprises, particuliers |
| **iRedMail** | Moyennement complexe, multi-OS | Web pour l'administration | TrÃ¨s bonne (outils anti-spam intÃ©grÃ©s) | Entreprises de toutes tailles |
| **Mailu** | BasÃ© sur Docker, moyennement complexe | Moderne, simple et lÃ©gÃ¨re | TrÃ¨s bonne | Grandes entreprises ou particuliers avancÃ©s |
| **Lightmeter** | Configuration manuelle avancÃ©e | Aucune interface utilisateur dÃ©diÃ©e | DÃ©pend de la configuration manuelle | Administrateurs (optimisation uniquement) |

---

## ð 3. Notre Recommandation : iRedMail
AprÃ¨s analyse, notre choix s'est portÃ© sur **iRedMail**. 

**Points forts retenus :**
*   **RapiditÃ© de dÃ©ploiement** et gestion simplifiÃ©e au quotidien.
*   **SÃ©curitÃ© robuste par dÃ©faut** : intÃ©gration native de protocoles de protection essentiels.
*   **Solution "PrÃªte Ã  l'emploi"** : fournit un serveur de messagerie complet et fiable dÃ¨s l'installation.

---

## ð ï¸ 4. Mise en Åuvre Technique et Interfaces
Voici les Ã©tapes clÃ©s du dÃ©ploiement illustrÃ©es par les captures de notre environnement de test :

### 4.1 Administration du SystÃ¨me
L'accÃ¨s Ã  la gestion des domaines et des comptes se fait via une interface sÃ©curisÃ©e.
<img width="576" height="283" alt="image" src="https://github.com/user-attachments/assets/e2e11fd5-de83-48b0-84c6-11ce36f1ee74" />

*Figure 1 : Interface de connexion de l'administrateur iRedAdmin.*

### 4.2 Tableau de Bord et Gestion
L'interface d'administration permet une vue d'ensemble sur les statistiques du serveur et les options de configuration.
<img width="576" height="283" alt="image" src="https://github.com/user-attachments/assets/2f610eaa-8a97-48f6-846f-2e28275e6d06" />

*Figure 2 : Tableau de bord prÃ©sentant les options d'administration systÃ¨me.*

### 4.3 ExpÃ©rience Utilisateur (Webmail SOGo)
Les utilisateurs bÃ©nÃ©ficient d'une interface de connexion moderne et d'une boÃ®te mail complÃ¨te pour la gestion de leurs courriers.
<img width="576" height="283" alt="image" src="https://github.com/user-attachments/assets/4b68b02f-4f60-4f8e-8a10-5295eda6a2b4" />

*Figure 3 : Interface de connexion utilisateur via SOGo.*

<img width="576" height="283" alt="image" src="https://github.com/user-attachments/assets/f360ef18-059a-4bb1-b487-9a799e837168" />

*Figure 4 : Vue de l'interface de la boÃ®te mail utilisateur.*

---

## ð¡ï¸ 5. Configuration Infrastructure et SÃ©curitÃ©
Le succÃ¨s d'un serveur de messagerie repose sur une configuration DNS mÃ©ticuleuse pour garantir la dÃ©livrabilitÃ©.
*   **Enregistrements DNS** : Configuration des champs MX, SPF et des clÃ©s DKIM pour Ã©viter le bannissement par les filtres anti-spam.
*   **Protocoles supportÃ©s** : DNSSEC, SPF, DKIM et DMARC.

<img width="576" height="283" alt="image" src="https://github.com/user-attachments/assets/6ac2e32d-bffe-458f-8b54-1e6fca2cf2f5" />

*Figure 5 : Extrait de la configuration du serveur DNS (fichier de zone).*

---


**Analogie pour conclure :**
DÃ©ployer un serveur de messagerie comme iRedMail, c'est comme construire son propre **centre de tri postal privÃ©**. Au lieu de confier votre courrier Ã  un prestataire externe, vous gÃ©rez vos propres camions (protocoles), vos propres verrous (sÃ©curitÃ©) et vos propres boÃ®tes aux lettres, tout en vous assurant que votre adresse est officiellement rÃ©pertoriÃ©e dans l'annuaire mondial (DNS) pour que le courrier puisse circuler.


---

<div align="center">

### 🔗 Liens

[![Portfolio](https://img.shields.io/badge/Portfolio-00f2ff?style=for-the-badge&logo=firefox&logoColor=black)](https://kim-san04.github.io) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hakim-sawadogo) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Kim-San04)

**Cheick Abdel Hadime Hakim SAWADOGO**
*Mastère Cybersécurité, Réseaux & Cloud — Efrei Bordeaux*
📧 cheick.sawadogo@efrei.net

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00f2ff,100:0d1117&height=80&section=footer)

</div>
