# Security & Privacy Notes

## Public Repository Rules

This project is based on a real business environment. The public portfolio repository is intentionally sanitized.

Do not publish:

- Passwords or authentication secrets
- Azure Static Web Apps deployment tokens
- Microsoft 365 credentials
- MFA recovery information
- Private mailbox contents
- PST or archive files
- Customer information
- Private backup files
- Sensitive internal infrastructure details
- Production website source code

## Email Authentication

The project uses the three main domain-level email authentication mechanisms:

- **SPF** — sender authorization
- **DKIM** — message signing
- **DMARC** — policy and authentication alignment

These controls were configured and tested as part of the wider email migration and deliverability work.

## Security Mindset

The project reinforced several practical security principles:

1. Credentials belong in secret stores, not Git.
2. Real client information should not be used in public documentation.
3. DNS changes should be planned before changing nameservers.
4. Email migrations require both data integrity and authentication planning.
5. Infrastructure changes should be tested after implementation.
6. Production source code can remain private while the technical approach is documented publicly.
