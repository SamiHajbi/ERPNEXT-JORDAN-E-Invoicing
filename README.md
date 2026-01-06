# JoFotara

## ERPNEXT Integration with Jordanian Tax Authority

JoFotara is an ERPNext application that integrates with the Jordanian Tax Authority's electronic invoicing system. This app adds the necessary fields and functionality to ERPNext to support compliance with Jordanian tax regulations.

## Features

- **Company Configuration**: Adds a dedicated JoFotara tab in the Company DocType with fields for configuring the integration with the Jordanian Tax Authority.
- **Integration Settings**: Provides fields for Client ID, Secret Key, Device ID, API Endpoint, and Sandbox Mode configuration.
- **Easy Setup**: All customizations are contained within the app and applied automatically during installation.

## Customizations

This app adds the following customizations to ERPNext:

1. **Company DocType**:
   - Adds a new tab labeled "JoFotara" after the "Stock and Manufacturing" tab
   - Adds a section titled "JoFotara Settings" with the following fields:
     - Enable JoFotara Integration (Check)
     - Client ID (Data)
     - Secret Key (Password)
     - Device ID (Data)
     - API Endpoint (Data)
     - Is Sandbox Mode? (Check)

## Installation

You can install this app using the [bench](https://github.com/frappe/bench) CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app https://github.com/YOUR_USERNAME/jofotara
bench install-app jofotara
```

After installation, the JoFotara tab will be available in the Company form.

### Contributing

This app uses `pre-commit` for code formatting and linting. Please [install pre-commit](https://pre-commit.com/#installation) and enable it for this repository:

```bash
cd apps/jofotara
pre-commit install
```

Pre-commit is configured to use the following tools for checking and formatting your code:

- ruff
- eslint
- prettier
- pyupgrade

### CI

This app can use GitHub Actions for CI. The following workflows are configured:

- CI: Installs this app and runs unit tests on every push to `develop` branch.
- Linters: Runs [Frappe Semgrep Rules](https://github.com/frappe/semgrep-rules) and [pip-audit](https://pypi.org/project/pip-audit/) on every pull request.


### License

mit
