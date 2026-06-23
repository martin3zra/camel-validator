# Camel VS Code Extension

`camel-vscode` is the companion Visual Studio Code extension for **Camel**, the schema migration skill designed for AI coding agents and developers. 

It automatically detects Camel migration definitions, attaches structured schema validation via `vscode-yaml`, and hooks up diagnostic linting directly inside your workspace.

## Features

* **Automated YAML Schema Mapping**: Seamlessly binds your database migration YAML files (`*.camel.yaml`) to the official structural JSON schema definition.
* **IntelliSense & Autocomplete**: Press `Ctrl + Space` to discover migration properties, allowed column definitions, index options, and specific engine syntax constraints.
* **Inline Diagnostics**: Catch syntax mistakes, typos, missing mandatory attributes, or illegal schema setups right as you type before running the database engine.

## Installation

This extension depends heavily on the **Red Hat YAML** language support plugin to power its validation layer. It will auto-install it as an extension dependency.

## Workspace Layout
Ensure your migration definitions leverage the following extension signature for auto-detection:
```text
your-project/
  └── database/
      └── migrations/
          ├── 0001_create_users_table.camel.yaml
          └── 0002_add_billing_columns.camel.yaml