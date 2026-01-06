# JoFotara – ERPNext Jordan E-Invoicing Integration

JoFotara is a production-ready ERPNext application that integrates ERPNext with the **Jordanian Tax Authority (JoFotara)** electronic invoicing system.  
The app adds all required fields, validations, and integration logic needed to comply with Jordanian e-invoicing regulations while remaining fully upgrade-safe.

---

## Project Naming & Identity

- **ERPNext App Name:** `jofotara`
- **Repository Name:** ERPNext Jordan E-Invoicing
- **Tax Authority System:** JoFotara (Jordanian Tax Authority)

> The internal app name **remains `jofotara`** by design.  
> This ensures upgrade safety, backward compatibility, and prevents breaking existing ERPNext installations.

Changing the repository URL **does NOT** change:
- App name inside ERPNext
- Database tables
- Installed sites
- Existing configurations

---

## Key Features

- Jordanian E-Invoicing (JoFotara) compliance
- UBL 2.1 XML generation & validation
- Secure API authentication
- Multi-company support
- Sandbox & Production modes
- Upgrade-safe (no core overrides)
- ERPNext-native validations and workflows

---

## Customizations Added

### Company DocType

Adds a dedicated **JoFotara** tab containing:

- Enable JoFotara Integration
- Client ID
- Secret Key (encrypted)
- Device ID
- API Endpoint
- Sandbox Mode

All settings are **company-specific**.

---

## Installation

Install using the official **bench** CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app https://github.com/SamiHajbi/ERPNEXT-JORDAN-E-Invoicing
bench install-app jofotara
---
## Upgrade

To update the application safely:

```bash
cd apps/jofotara
git pull
bench migrate
bench build
bench restart
---

## Development & Contribution

This project uses pre-commit for code quality and formatting.

```bash
cd apps/jofotara
pre-commit install
---

Tools Used

ruff

eslint

prettier

pyupgrade

CI / Automation

GitHub Actions workflows included:

Continuous Integration (installation + tests)

Security & quality checks using:

Frappe Semgrep Rules

pip-audit

## Support & Contact

For technical support, implementation assistance, or enterprise deployment:

📧 Email: Info@Decart.net

📞 Phone / WhatsApp: +962 7 9200 0160

Support provided by Decart International.

## License

MIT License

Disclaimer

This application is an integration tool only.
It does not replace official compliance responsibility with the Jordanian Tax Authority.
Users must ensure adherence to all JoFotara laws, regulations, and updates.
