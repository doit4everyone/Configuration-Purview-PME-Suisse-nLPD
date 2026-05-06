---
canonical: https://doit4everyone.github.io/Configuration-Purview-PME-Suisse-nLPD/
meta-description: Guide MVC Microsoft Purview pour PME suisses — Minimum Viable de Conformité nLPD, déploiement en 4 à 6 heures, adaptations sectorielles incluses.
title: Guide MVC Microsoft Purview (2026) | DoIt4Everyone
---

# Guide MVC Microsoft Purview (2026)

## Minimum Viable de Conformité nLPD pour PME suisses 🇨🇭

Ce guide propose une procédure de déploiement allégée, conçue pour installer une conformité nLPD défendable chez une PME suisse de 5 à 25 personnes en une session de 4 à 6 heures.

Il s'accompagne d'un guide d'exploitation remis directement au responsable IT du client, sans formation Purview préalable, incluant les spécificités par secteur d'activité.

---

## 🎯 Objectifs

- Déployer une protection nLPD **défendable devant le PFPDT** en 4 à 6 heures
- Remettre au client un **guide opérationnel autonome** adapté à son secteur
- Couvrir les secteurs PME les plus courants avec des **adaptations documentées**

---

## 📥 Téléchargement

👉 [Télécharger la documentation complète (v1.0)](https://github.com/doit4everyone/Configuration-Purview-PME-Suisse-nLPD/releases/latest)

---

## 🧩 Ce que couvre le MVC

- **MFA** sur tous les comptes — première barrière
- **Blocage SharePoint** — partage externe bloqué au niveau tenant
- **2 étiquettes** — 1 - Interne + 2 - Confidentiel (chiffrement AES-256)
- **Auto-labelling service** — détection AVS, IBAN, médical en 4 langues nationales
- **DLP Exchange** — avertissement + justification obligatoire IBAN
- **Rétention automatique** — 10 ans RH et Finances (CO art. 958f)
- **Break-glass RMS** — accès de secours, révocation d'urgence (Revoke-AipServiceDocumentAccess)
- **Audit 1 an** — traçabilité complète exportable pour le PFPDT

---

## 🗂️ Adaptations sectorielles

Le guide de déploiement (Annexe F) et le guide d'exploitation (Partie 8) documentent les adaptations pour chaque secteur :

| Secteur | Guide déploiement (Annexe F) | Guide exploitation (Partie 8) |
| --- | --- | --- |
| PME générique | MVC tel quel | Standard |
| Fiduciaire / comptabilité | Étiquette 3 - Externe-Fiduciaire + SIT IDE/UID + rétention couplée | Quelle étiquette envoyer à l'AFC, banques, caisses AVS |
| Architectes / ingénieurs | Partage contrôlé SharePoint + expiration 30 jours | Partager un dossier projet, renouveler les liens |
| Avocats / notaires | Étiquette 3 - Juridique-Externe + note Justitia.swiss | Quelle étiquette pour tribunaux et parties adverses |
| Agences communication | Exclusion sites créatifs auto-labelling + DLP ciblée | Comptes surveillés vs exclus, charte informatique |
| Cabinets médicaux | Étiquette 3 - Patient-Externe + note HIN | Quelle étiquette pour les patients, flux HIN séparé |

---

## 🇨🇭 Défendable devant le PFPDT

| Article nLPD | Exigence | Mesure MVC |
| --- | --- | --- |
| Art. 12 | Registre des activités de traitement | Modèle pré-rempli fourni |
| Art. 8 | Mesures techniques et organisationnelles | Chiffrement, DLP, rétention, audit |
| Art. 24 | Traçabilité et notification des violations | Journaux exportables, révocation RMS |

---

## 📖 Aller plus loin

Pour les déploiements avancés incluant IRM, Endpoint DLP, eDiscovery, Communication Compliance, DSPM for AI et gouvernance Copilot :

👉 **[Guide complet Microsoft Purview 2026](https://doit4everyone.github.io/microsoft-purview-configuration-2026-nLPD/)**

---

## ☕ Soutenir le projet *(optionnel)*

Ce guide est mis à disposition gratuitement.

👉 [Ko-fi — doit4everyone](https://ko-fi.com/doit4everyone)

---

[🏠 Retrouvez tous les guides sur doit4everyone.github.io](https://doit4everyone.github.io/)

---

ℹ️ *Références, structuration et aide à la rédaction assistées par IA, avec validation humaine finale.*

[Improve this page](https://github.com/doit4everyone/purview-mvc-pme-suisse/edit/main/docs/index.md)
