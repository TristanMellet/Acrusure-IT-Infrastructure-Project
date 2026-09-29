# Acrusure Infrastructure Architecture

## Overview

The Acrusure project combines a public business website, cloud hosting, domain services, Microsoft 365 and email-authentication controls.

## Logical Flow

```text
Internet
   │
   ▼
Domain / DNS
   │
   ├──────────────► Azure Static Web Apps
   │                      │
   │                      ▼
   │                 Business Website
   │
   └──────────────► Microsoft 365
                          │
                          ▼
                   Exchange Online
                          │
                          ▼
                  SPF / DKIM / DMARC
```

## Source Control & Deployment

GitHub stores the website source code in a separate private implementation repository and contains the GitHub Actions deployment workflow there.

The public repository intentionally contains no production source code or deployment secrets.

## Design Principles

- Keep credentials outside source control.
- Separate public portfolio documentation from private business information.
- Keep production implementation code private.
- Use version control for website and infrastructure-related changes.
- Use DNS records deliberately for each service.
- Document changes so the environment can be maintained after implementation.
- Test infrastructure changes rather than assuming configuration is correct.
