# Cost Management and Resource Usage

> Cost and usage governance on AWS.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000064-cost-usage-governance/

## Overview

In this lab, we will use IAM (Identity and Access Management) service to implement some best practices about cost management and resource usage on AWS environment.

## Workshop contents

1. Preparation
   - Create IAM Group
   - Create IAM user
2. Limit by Region
   - Create restriction policy
   - Assign policy to group
   - testpolicy
3. Limit by EC2 family
   - Create restriction policy
   - Assign policy to group
   - Validate policy effectiveness
4. Limit by instance size
   - Update restriction policy
   - Validate policy effectiveness
5. Limited by EBS volume
   - Create restriction policy
   - Assign policy to group
   - Validate policy effectiveness
6. Clean up resources

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone --recurse-submodules https://github.com/vanhoangkha/000064-cost-usage-governance.git
cd 000064-cost-usage-governance
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Complete the **Clean up** chapter when you finish to remove them.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
