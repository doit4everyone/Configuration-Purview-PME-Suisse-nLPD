🇬🇧 [Read this README in English](README.en.md)

# Guide MVC Microsoft Purview (2026)

## Minimum Viable de Conformité nLPD pour PME suisses 🇨🇭

Ce dépôt contient deux documents complémentaires pour déployer et maintenir une conformité nLPD défendable chez une PME suisse de 5 à 25 personnes :

- **Un guide de déploiement** pour le consultant, permettant une mise en place complète en 4 à 6 heures.
- **Un guide d'exploitation** remis au responsable IT du client, pour l'autonomie opérationnelle au quotidien.

> **Message clé**
> Le Minimum Viable de Conformité (MVC) ne vise pas la perfection technique.
> C'est la **capacité de démontrer une démarche proportionnée** devant le PFPDT.

---

## 🎯 Périmètre du MVC

✅ **Inclus**

- Microsoft 365 Business Premium
- Microsoft Purview Suite (add-on)
- MFA (tous les comptes)
- Audit Purview (traçabilité 1 an)
- 2 étiquettes de sensibilité : **1 - Interne** + **2 - Confidentiel** (chiffrement AES-256 / Azure RMS)
- SITs personnalisés : AVS-Suisse-PME + Medical-RH-Suisse (4 langues nationales + anglais)
- Auto-labelling service (fichiers SharePoint existants)
- DLP Exchange : avertissement données sensibles + justification obligatoire IBAN
- Rétention automatique 10 ans (RH + Finances, CO art. 958f)
- Blocage du partage externe SharePoint au niveau tenant
- Break-glass RMS (procédure de secours documentée)

❌ **Hors périmètre MVC**

- IRM (Insider Risk Management)
- Endpoint DLP
- eDiscovery Premium
- Communication Compliance
- DSPM for AI
- Power Platform Managed Environments
- Gouvernance Copilot

*(Ces fonctionnalités sont couvertes dans le [Guide complet Microsoft Purview 2026](https://github.com/doit4everyone/microsoft-purview-configuration-2026-nLPD).)*

---

## 🧩 Contenu du dépôt

### 1️⃣ Guide de déploiement MVC — pour le consultant

**`Purview_MVC_PME_Suisse_v1.docx`** / **`Purview_MVC_PME_Suisse_v1.pdf`**

Procédure complète couvrant :

- prérequis et attribution des rôles
- activation MFA et blocage SharePoint tenant
- création des SITs personnalisés (AVS, médical, 4 langues nationales)
- création et publication des 2 étiquettes de sensibilité
- auto-labelling côté service (fichiers SharePoint existants)
- Break-glass RMS (procédure PowerShell complète)
- DLP Exchange (2 règles, mode simulation)
- rétention automatique 10 ans (RH + Finances)
- tests de validation et checklist de remise
- registre des activités de traitement pré-rempli (art. 12 nLPD)
- **Annexe F — Adaptations sectorielles** : fiduciaire, architectes, avocats, agences, cabinets médicaux

---

### 2️⃣ Guide d'exploitation client — à remettre au client

**`Purview_MVC_Guide_Exploitation_Client_v1.docx`** / **`Purview_MVC_Guide_Exploitation_Client_v1.pdf`**

Guide opérationnel pour le responsable IT, sans formation Purview préalable :

- comprendre et utiliser les 2 étiquettes
- réagir aux alertes DLP dans Outlook
- envoyer des documents à des destinataires externes (OTP, traçabilité)
- révoquer l'accès à un fichier chiffré (Revoke-AipServiceDocumentAccess)
- utiliser le compte Break-glass en cas de problème grave
- routine mensuelle de contrôle (15 minutes)
- conduite à tenir en cas d'incident nLPD (art. 24)
- produire les preuves pour le PFPDT
- révision annuelle
- **spécificités sectorielles** : usage quotidien et routine adaptés pour fiduciaire, architectes, avocats, agences de communication et cabinets médicaux

---

## 🔐 Architecture MVC

| Composant | Configuration |
| --- | --- |
| Étiquette 1 | 1 - Interne — sans chiffrement, par défaut |
| Étiquette 2 | 2 - Confidentiel — AES-256, auto-labelling AVS + IBAN + médical |
| Destinataires externes | Tous les utilisateurs authentifiés (OTP pour non-Microsoft) |
| DLP Exchange | Règle 1 : avertissement données sensibles + override justifié |
| DLP Exchange | Règle 2 : avertissement IBAN + justification obligatoire |
| SharePoint | Partage externe bloqué au niveau tenant |
| Rétention | 10 ans SharePoint RH + Finances (CO art. 958f) |
| Audit | 1 an (Purview Suite) |
| Break-glass | Super User RMS configuré avant mise en production |

---

## 🇨🇭 Conformité nLPD

| Article | Exigence | Mesure MVC |
| --- | --- | --- |
| Art. 12 | Registre des activités de traitement | Modèle pré-rempli en Annexe I |
| Art. 8 | Mesures techniques et organisationnelles | Chiffrement + DLP + audit + rétention + blocage SharePoint |
| Art. 24 | Traçabilité et notification des violations | Journaux exportables, incidents DLP horodatés, révocation RMS |

---

## 🏷️ Modèle de licence utilisé

| Composant | Licence |
| --- | --- |
| Microsoft 365 Business Premium | Requis |
| Microsoft Purview Suite | Requis (~CHF 15.70 / utilisateur / mois) |

---

## 📖 Aller plus loin

Pour les déploiements avancés incluant IRM, Endpoint DLP, eDiscovery, Communication Compliance, DSPM for AI et gouvernance Copilot, consultez le **[Guide complet Microsoft Purview 2026](https://github.com/doit4everyone/microsoft-purview-configuration-2026-nLPD)**.

---

## ⚠️ Avertissement

Ce dépôt est fourni à des fins pédagogiques et architecturales. Adaptez les configurations à votre contexte légal et impliquez les parties juridiques et conformité avant tout déploiement en production. Ce document ne constitue pas un avis juridique.

Lire le [DISCLAIMER complet](DISCLAIMER.md).

---

## 🧭 Accès rapide

🌐 Page de présentation : <https://doit4everyone.github.io/Configuration-Purview-PME-Suisse-nLPD/>

🏠 Retrouvez tous les guides sur : <https://doit4everyone.github.io/>

---

## ☕ Soutenir ce projet (optionnel)

Ce guide est mis à disposition gratuitement.

Il est le fruit de plusieurs semaines de travail, incluant des tests techniques terrain sur Microsoft 365 / Purview, une validation méthodologique orientée PME et une prise en compte des exigences de la nLPD (Suisse).

À titre strictement optionnel :

👉 **[Soutenir le projet sur Ko-fi](https://ko-fi.com/doit4everyone)**

Aucune contrepartie, aucun service associé et aucune différence de traitement n'est liée à ce soutien.

---

ℹ️ *Références, structuration et aide à la rédaction assistées par IA, avec validation humaine finale.*
