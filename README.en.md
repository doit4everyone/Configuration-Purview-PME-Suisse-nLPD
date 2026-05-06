🇫🇷 [Lire ce README en français](README.md)

# Microsoft Purview MVC Guide (2026)

## Minimum Viable Compliance for nLPD — Swiss SMEs 🇨🇭

This repository contains two complementary documents for deploying and maintaining defensible nLPD compliance at Swiss SMEs with 5 to 25 employees:

- **A deployment guide** for the consultant, enabling full setup in 4 to 6 hours.
- **A client operations guide** handed over to the client's IT administrator for day-to-day autonomy.

> **Key message**
> The Minimum Viable Compliance (MVC) does not aim for technical perfection.
> It is the **ability to demonstrate a proportionate approach** before the FDPIC.

---

## 🎯 MVC Scope

✅ **Included**

- Microsoft 365 Business Premium
- Microsoft Purview Suite (add-on)
- MFA (all accounts)
- Purview Audit (1-year retention)
- 2 sensitivity labels: **1 - Internal** + **2 - Confidential** (AES-256 / Azure RMS)
- Custom SITs: AVS-Suisse-PME + Medical-RH-Suisse (4 national languages + English)
- Service-side auto-labelling (existing SharePoint files)
- Exchange DLP: sensitive data warning + mandatory IBAN justification
- Automatic 10-year retention (HR + Finance, CO art. 958f)
- SharePoint external sharing blocked at tenant level
- Break-glass RMS (documented emergency procedure)

❌ **Out of MVC scope**

- IRM (Insider Risk Management)
- Endpoint DLP
- eDiscovery Premium
- Communication Compliance
- DSPM for AI
- Power Platform Managed Environments
- Copilot governance

*(These features are covered in the [Microsoft Purview 2026 Full Guide](https://github.com/doit4everyone/microsoft-purview-configuration-2026-nLPD).)*

---

## 🧩 Repository contents

### 1️⃣ MVC Deployment Guide — for the consultant

**`Purview_MVC_PME_Suisse_v1.docx`** / **`Purview_MVC_PME_Suisse_v1.pdf`**

Full procedure covering:

- prerequisites and role assignment
- MFA activation and SharePoint tenant-level blocking
- custom SIT creation (AVS, medical, 4 national languages)
- sensitivity label creation and publication
- service-side auto-labelling (existing SharePoint files)
- Break-glass RMS (full PowerShell procedure)
- Exchange DLP (2 rules, simulation mode)
- automatic 10-year retention (HR + Finance)
- validation tests and client handover checklist
- pre-filled data processing register (nLPD art. 12)
- **Annex F — Sector-specific adaptations**: fiduciary, architects, lawyers, agencies, medical practices

---

### 2️⃣ Client Operations Guide — to hand over to the client

**`Purview_MVC_Guide_Exploitation_Client_v1.docx`** / **`Purview_MVC_Guide_Exploitation_Client_v1.pdf`**

Operational guide for the IT administrator, no prior Purview training required:

- understanding and using the 2 labels
- responding to DLP alerts in Outlook
- sending documents to external recipients (OTP, traceability)
- revoking access to an encrypted file (Revoke-AipServiceDocumentAccess)
- using the Break-glass account in case of serious issues
- monthly control routine (15 minutes)
- nLPD incident response procedure (art. 24)
- producing evidence for the FDPIC
- annual review
- **sector-specific guidance**: daily usage and adapted routine for fiduciary, architects, lawyers, communication agencies and medical practices

---

## 🔐 MVC Architecture

| Component | Configuration |
| --- | --- |
| Label 1 | 1 - Internal — no encryption, default |
| Label 2 | 2 - Confidential — AES-256, auto-labelling AVS + IBAN + medical |
| External recipients | All authenticated users (OTP for non-Microsoft accounts) |
| Exchange DLP | Rule 1: sensitive data warning + justified override |
| Exchange DLP | Rule 2: IBAN warning + mandatory recorded justification |
| SharePoint | External sharing blocked at tenant level |
| Retention | 10 years SharePoint HR + Finance (CO art. 958f) |
| Audit | 1 year (Purview Suite) |
| Break-glass | Super User RMS configured before go-live |

---

## 🇨🇭 nLPD Compliance

| Article | Requirement | MVC Measure |
| --- | --- | --- |
| Art. 12 | Data processing register | Pre-filled template in Annex I |
| Art. 8 | Technical and organizational measures | Encryption + DLP + audit + retention + SharePoint blocking |
| Art. 24 | Traceability and breach notification | Exportable logs, timestamped DLP incidents, RMS revocation |

---

## 🏷️ License model

| Component | License |
| --- | --- |
| Microsoft 365 Business Premium | Required |
| Microsoft Purview Suite | Required (~CHF 15.70 / user / month) |

---

## 📖 Going further

For advanced deployments including IRM, Endpoint DLP, eDiscovery, Communication Compliance, DSPM for AI and Copilot governance, refer to the **[Microsoft Purview 2026 Full Guide](https://github.com/doit4everyone/microsoft-purview-configuration-2026-nLPD)**.

---

## ⚠️ Disclaimer

This repository is provided for educational and architectural purposes. Adapt configurations to your legal context and involve legal and compliance teams before any production deployment. This document does not constitute legal advice.

Read the [full DISCLAIMER](DISCLAIMER.md).

---

## 🧭 Quick access

🌐 Presentation page: <https://doit4everyone.github.io/purview-mvc-pme-suisse/>

🏠 All guides: <https://doit4everyone.github.io/>

---

## ☕ Support this project (optional)

This guide is provided free of charge.

It is the result of several weeks of real-environment testing, methodological validation, and alignment with Swiss nLPD requirements.

Strictly optional:

👉 **[Support the project on Ko-fi](https://ko-fi.com/doit4everyone)**

No obligation, no associated service, and no difference in access to content is linked to this support.

---

ℹ️ *References, structure and drafting assistance by AI, with final human validation.*
