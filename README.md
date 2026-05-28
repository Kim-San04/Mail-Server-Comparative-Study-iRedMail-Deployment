<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:00f2ff&height=120&section=header&text=&fontSize=0)

</div>

# 📧 Serveurs Mail — Étude Comparative & Déploiement iRedMail

<div align="center">

![iRedMail](https://img.shields.io/badge/iRedMail-FF6600?style=for-the-badge&logo=mail.ru&logoColor=white) ![Linux](https://img.shields.io/badge/Linux_Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white) ![Postfix](https://img.shields.io/badge/Postfix-CC0000?style=for-the-badge&logo=gmail&logoColor=white) ![DKIM](https://img.shields.io/badge/DKIM_SPF_DMARC-Email_Security-00b4d8?style=for-the-badge) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

![Efrei](https://img.shields.io/badge/Efrei_Bordeaux-Mastère_Cybersécurité-purple?style=flat-square) ![Type](https://img.shields.io/badge/Type-Infrastructure_%26_Déploiement-green?style=flat-square) ![Status](https://img.shields.io/badge/Status-Terminé-success?style=flat-square)

</div>

---

## 🎯 Objectifs du Projet

Analyser et comparer les solutions de serveurs mail open-source auto-hébergés, puis déployer et sécuriser la solution retenue (iRedMail) sur une infrastructure Linux.

---

## 📊 Étude Comparative

| Solution | Complexité | Fonctionnalités | Sécurité | Recommandé pour |
| :--- | :---: | :---: | :---: | :--- |
| **iRedMail** | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | PME / Projets académiques |
| **Mailcow** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Entreprises Docker |
| **Mailu** | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | Déploiements légers |
| **Postfix seul** | ⭐⭐⭐⭐ | ⭐⭐ | Variable | Admins expérimentés |

---

## 🏆 Notre Recommandation : iRedMail

**iRedMail** a été sélectionné pour sa facilité de déploiement sur Ubuntu, son intégration native des protocoles SMTP/IMAP/POP3, et son interface d'administration complète (SOGo).

**Stack iRedMail :**
- **MTA :** Postfix (envoi/réception SMTP)
- **MDA :** Dovecot (IMAP/POP3)
- **Webmail :** SOGo + Roundcube
- **Antispam :** Amavis + SpamAssassin
- **Antivirus :** ClamAV
- **Serveur web :** Nginx

---

## 🛠️ Déploiement Technique

### Prérequis

- Ubuntu Server 22.04 LTS
- RAM minimum : 4 Go
- DNS : enregistrements A, MX, PTR configurés

### Installation

```bash
# Téléchargement et extraction
wget https://github.com/iredmail/iRedMail/archive/refs/tags/1.6.8.tar.gz
tar -xzf 1.6.8.tar.gz && cd iRedMail-1.6.8

# Lancement de l'installeur interactif
bash iRedMail.sh
```

---

## 🛡️ Sécurisation — Anti-Spoofing Email

Configuration des enregistrements DNS anti-spoofing :

| Mécanisme | Rôle | Enregistrement |
| :--- | :--- | :--- |
| **SPF** | Autorise les IPs d'envoi | `TXT "v=spf1 mx ~all"` |
| **DKIM** | Signature cryptographique | Clé publique dans DNS |
| **DMARC** | Politique de traitement | `TXT "v=DMARC1; p=reject"` |

---

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-00f2ff?style=for-the-badge&logo=firefox&logoColor=black)](https://kim-san04.github.io) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hakim-sawadogo) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Kim-San04)

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00f2ff,100:0d1117&height=80&section=footer)

</div>
