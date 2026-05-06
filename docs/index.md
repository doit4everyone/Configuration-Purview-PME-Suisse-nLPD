---
title: "Procédure déploiement Purview MVC (nLPD Suisse) | DoIt4Everyone"
description: "Procédure technique de déploiement Microsoft Purview pour PME suisses. Configuration MVC (Minimum Viable de Conformité) nLPD en 4 à 6 heures."
---

<style>
  header, footer { display: none !important; }

  .wrapper {
    max-width: 900px !important;
    margin: 0 auto !important;
    float: none !important; 
    position: relative !important;
    padding: 40px 20px !important;
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif !important;
    font-size: 1.1em !important;
  }

  section {
    width: 100% !important;
    float: none !important;
    margin: 0 !important;
  }

  h1, h2 { text-align: center; }
  table { width: 100%; display: table; margin: 20px 0; }
</style>

<h1 style="text-align: center;">Guide Minimum Viable de Conformité Microsoft Purview (2026)</h1>
<h2 style="text-align: center;"><strong>Procédure de déploiement nLPD pour PME suisses 🇨🇭</h2>

Ce guide propose une **procédure technique complète**, conçue pour installer une conformité nLPD défendable chez une PME suisse de 5 à 25 personnes en une session de **4 à 6 heures**.

---

### 🎯 Objectifs du déploiement

*   Appliquer une **procédure de configuration** simplifiée et efficace.
*   Garantir une protection des données **défendable devant le PFPDT**.
*   Remettre un **guide d'exploitation** autonome adapté au secteur d'activité.

---

### 🧩 Périmètre technique du MVC

*   **MFA & Sécurité** : Durcissement des accès prioritaires.
*   **Gouvernance SharePoint** : Blocage des partages externes non maîtrisés.
*   **Classification** : Déploiement de 2 étiquettes (Interne / Confidentiel).
*   **Auto-labelling** : Détection automatisée (AVS, IBAN, Médical) en 4 langues.
*   **Prévention (DLP)** : Blocage et justification des flux de données sensibles.
*   **Conservation** : Rétention légale 10 ans (CO art. 958f).
*   **Audit** : Activation de la traçabilité complète pour les rapports nLPD.

---

### 🗂️ Adaptations par secteurs d'activité

| Secteur | Configuration technique | Guide d'exploitation |
| :--- | :--- | :--- |
| **Fiduciaire** | SIT IDE/UID + Rétention couplée | Envois AFC et Caisses AVS |
| **Architectes** | Expiration auto des partages projets | Gestion des liens externes |
| **Avocats** | Étiquette Juridique + Justitia.swiss | Échanges tribunaux et parties |
| **Médical** | Étiquette Patient + Flux HIN | Confidentialité des données de soins |

---

### 🇨🇭 Conformité nLPD

| Article | Exigence | Mesure MVC incluse |
| :--- | :--- | :--- |
| **Art. 12** | Registre des activités | Modèle RAT pré-rempli |
| **Art. 8** | Mesures techniques | Chiffrement, DLP, Rétention |
| **Art. 24** | Traçabilité | Journaux d'audit exportables |

---

### 📥 Téléchargement

👉 **[Télécharger la procédure complète (v1.0)](https://github.com/doit4everyone/purview-mvc-pme-suisse/releases/latest)**

---

### 📖 Aller plus loin

Pour les besoins avancés (Gouvernance Copilot, eDiscovery, Endpoint DLP) :

👉 **[Consulter le Guide complet Microsoft Purview 2026](https://doit4everyone.github.io/microsoft-purview-configuration-2026-nLPD/)**

---

[🏠 Retour au portail principal](https://doit4everyone.github.io/)

---

ℹ️ *Références, structuration et aide à la rédaction assistées par IA, avec validation humaine finale.*
