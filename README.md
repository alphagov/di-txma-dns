# di-txma-dns

Infrastructure required for TxMA DNS, such as Route 53 Hosted Zones, Records, and any resources required for Custom Domains.

## Pre-requisites

To run this project you will need the following:
- [Pre-commit](https://pre-commit.com/) - Pre-commit hooks
- [Checkov](https://www.checkov.io/) - Scans cloud infrastructure configurations to find misconfigurations before they're deployed.Used in the pre-commit hooks.

## Getting started

Since the dev environment does not allow custom domains, unfortunately it is not possible to deploy the stacks to test before merging. Therefore, it is important to make sure that the template is at least valid. The SAM validate command can be used to achieve this:

```bash
sam validate --lint
```

There are also pre-commit hooks that can be installed to help achieve this automatically. After installing pre-commit (see pre-requisites), simply run:

```bash
pre-commit install
```

Every time a commit is made the hook should run and validate the templates automatically.

**Note:** It my be necessary to install some of the software used by the pre-commit hooks e.g. Checkov.

## Licence

[MIT License](LICENCE)
