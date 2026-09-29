# Acrusure — IT Infrastructure & Website Project

> Real-world business IT project covering website development, Azure deployment, Microsoft 365 migration planning, DNS, email security, and cloud infrastructure.

![Project Status](https://img.shields.io/badge/status-live-success)
![Azure](https://img.shields.io/badge/Azure-Static%20Web%20Apps-0078D4?logo=microsoftazure&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft%20365-Cloud%20Infrastructure-D83B01?logo=microsoft&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Version%20Control-181717?logo=github&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-Website-E34F26?logo=html5&logoColor=white)

## 📌 Project Overview

Acrusure is a South African insurance business for which I worked on a broader IT modernisation project.

The project started as a website build and developed into a hands-on infrastructure project involving cloud hosting, DNS, Microsoft 365, email security, migration planning, GitHub version control, and business communication tooling.

**Important:** The actual website implementation repository is intentionally kept private for client confidentiality. This repository is the public portfolio case study and contains only sanitized technical documentation.

## 🎯 Objectives

- Build and deploy a modern responsive business website.
- Move website hosting into an Azure-based environment.
- Establish GitHub as the source-control location for the website.
- Support the transition from legacy hosting infrastructure.
- Configure and validate domain/DNS requirements.
- Improve business email authentication and deliverability.
- Plan the migration of business email into Microsoft 365.
- Document the infrastructure in a maintainable and auditable way.

## 🧰 Technologies & Platforms

| Area | Technology |
|---|---|
| Website | HTML5, CSS, JavaScript |
| Source Control | GitHub |
| Hosting | Azure Static Web Apps |
| Cloud | Microsoft Azure |
| Productivity / Email | Microsoft 365 |
| DNS | MX, CNAME, TXT and related DNS records |
| Email Security | SPF, DKIM, DMARC |
| Forms | Formspree |
| Business Messaging | WhatsApp Business / Meta tools |

## 🏗️ High-Level Architecture

```text
                         ┌─────────────────────┐
                         │     End Users       │
                         │ Customers / Staff   │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │  Business Domain    │
                         │       DNS           │
                         └───────┬─────┬───────┘
                                 │     │
                    Website      │     │ Email
                                 │     │
                                 ▼     ▼
                    ┌──────────────┐  ┌─────────────────┐
                    │ Azure Static │  │ Microsoft 365   │
                    │ Web Apps     │  │ Exchange Online │
                    └──────┬───────┘  └────────┬────────┘
                           │                   │
                           ▼                   ▼
                    ┌──────────────┐  ┌─────────────────┐
                    │   GitHub     │  │ Email Security  │
                    │ Source Code  │  │ SPF / DKIM /    │
                    │ + CI/CD      │  │ DMARC           │
                    └──────────────┘  └─────────────────┘
```

## 📸 Project Screenshots

The following screenshots show selected parts of the completed implementation and deployment workflow.

### 🌐 Responsive Website

**Desktop**

![Acrusure website — desktop](screenshots/01-website-desktop.png)

**Mobile**

![Acrusure website — mobile](screenshots/02-website-mobile.png)

### ⚙️ GitHub Actions CI/CD

The deployment workflow was connected to the Azure Static Web App and used GitHub Actions for automated deployment.

![GitHub Actions deployment workflow](screenshots/03-github-actions.png)

> Screenshots are included for portfolio documentation. Production source code and sensitive infrastructure configuration remain private.

## 🌐 Website Development

The website was implemented as a self-contained static site using HTML, CSS and JavaScript.

The implementation was designed for straightforward deployment without requiring a traditional server-side application or complex build pipeline.

The production source code is maintained separately in a **private implementation repository**.

## ☁️ Azure Deployment

The project uses **Azure Static Web Apps** for website hosting.

GitHub Actions was used to automate deployment from the private source repository. This created a repeatable deployment workflow rather than relying on manually uploading website files.

Deployment credentials and tokens are stored through GitHub/Azure secret management and are not included in this public repository.

## 📧 Microsoft 365 & Email Migration

A major part of the project involved modernising the business email environment and planning the migration away from the previous hosting environment.

The work included:

- Reviewing mailbox and archive requirements.
- Planning Microsoft 365 mailbox structure.
- Working with shared and individual mailbox concepts.
- Planning migration of historical Outlook/PST data.
- Reviewing backup and archive requirements.
- Configuring domain authentication records.
- Testing email delivery and spam placement.
- Enabling appropriate Microsoft account security controls and MFA.

No mailbox contents, PST files, passwords, tokens or private business data are stored in this repository.

## 🔐 Email Security

The domain configuration included the main email-authentication controls used to improve sender validation and reduce spoofing.

### SPF

SPF identifies authorised mail-sending infrastructure for a domain.

### DKIM

DKIM provides cryptographic authentication for supported outbound email.

### DMARC

DMARC provides policy and reporting capabilities built around SPF and DKIM authentication.

The project also included practical deliverability testing, including checking whether messages reached Gmail inboxes or spam folders and troubleshooting the configuration.

## 🔄 Legacy Infrastructure → Cloud Infrastructure

A major project theme was reducing dependence on the previous hosting environment and moving toward a Microsoft/Azure-based setup.

The resulting architecture separates major responsibilities:

- **GitHub** — source control and deployment workflow.
- **Azure** — website hosting.
- **Microsoft 365** — business email and productivity.
- **DNS** — domain routing and service discovery.
- **SPF/DKIM/DMARC** — email authentication.

## 🛡️ Security & Privacy Approach

Because this is based on a real business environment, this public repository intentionally follows a sanitisation approach.

### Never publish

- Passwords
- API keys
- Azure deployment tokens
- Microsoft 365 credentials
- MFA recovery codes
- Private mailbox contents
- PST/archive files
- Private client/customer information
- Sensitive internal infrastructure details

### Public documentation focuses on

- Architecture
- Technologies
- Implementation approach
- Security concepts
- Lessons learned
- Sanitized diagrams and screenshots where appropriate

## 🧠 Key Skills Demonstrated

### Cloud & Infrastructure
- Azure Static Web Apps
- DNS configuration
- Cloud migration concepts
- Microsoft 365 administration

### Security
- SPF
- DKIM
- DMARC
- MFA/security controls
- Email deliverability troubleshooting
- Secure credential handling
- Client-data protection

### Development
- HTML5
- CSS
- JavaScript
- Responsive web design
- Git/GitHub
- GitHub Actions

### IT Operations
- Requirements gathering
- Troubleshooting
- Migration planning
- Backup/archive considerations
- Technical documentation
- Client-facing technical work

## 📈 Project Outcome

The project resulted in a working business website hosted through Azure, a GitHub-based source-control and deployment workflow, a modernised Microsoft 365 email environment, and improved domain/email security configuration.

More importantly, the project provided hands-on experience connecting **web development, cloud infrastructure, IT administration and cybersecurity** in one real-world environment.

## 📚 Related Learning

This project forms part of my broader transition into cybersecurity and cloud security.

I am currently working toward the **Microsoft SC-200: Security Operations Analyst** certification and building hands-on experience with Microsoft security tooling, including Microsoft Sentinel and KQL.

## 🔗 Repository Structure

This public repository contains portfolio documentation only.

The production implementation is maintained separately in a private repository to protect the client's business information and the website's source code.

```text
Acrusure-IT-Infrastructure-Project/
├── README.md
├── docs/
│   ├── architecture.md
│   └── security.md
└── PUBLIC-RELEASE-CHECKLIST.md
```

## 👤 Author

**Tristan Mellet**

BSc Network & Security student | Aspiring Cybersecurity Professional

GitHub: [@TristanMellet](https://github.com/TristanMellet)

---

## ⚠️ Disclaimer

This repository documents a real-world project in a sanitized form for portfolio and educational purposes. Certain implementation details, business information and infrastructure configuration have intentionally been omitted to protect the client and the security of the environment.
