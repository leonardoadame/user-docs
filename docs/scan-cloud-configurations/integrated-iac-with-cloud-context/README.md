# Integrated IaC with cloud context

{% hint style="info" %}
**Feature availability**\
Integrated IaC is currently in **closed beta**. Reach out to your account team if you would like access.
{% endhint %}

## Overview of Integrated IaC

Integrated Infrastructure as Code (IaC) is a new version of Snyk IaC that has cloud context to secure cloud configurations across the entire SDLC, from code to deployed AWS, Azure, and Google Cloud environments. Integrated IaC has the Snyk cloud context interfaces, workflows, policy engine, and data model.

Snyk cloud context helps users find, prioritize, and fix cloud misconfigurations by providing for scanning and testing deployed cloud resources with a library of predefined security rules. Scanning generates a record of issues that can be filtered and triaged.

Integrated Infrastructure as Code (IaC) has additional improvements to help developers write secure infrastructure configurations, with improvements including:

* Line numbers in the CLI for better accuracy in detection issues.
* Support for HashiCorp Terraform modules and variables for SCM repositories and the CLI.
* Powerful code-to-cloud capabilities, including the ability to [fix cloud issues in Integrated IaC](fix-cloud-issues-in-integrated-iac.md) and run IaC tests in the CLI with cloud context to reduce noise.

## Features of Integrated IaC

### Developer-first security for cloud configurations

With Integrated IaC and cloud context, Snyk extends its focus on developer security to enable developers to build and deploy secure cloud configurations from IaC in the IDE, through to production. Snyk has the same interfaces across the UI and API for cloud configurations in code and in deployed environments.

### Security and compliance posture for security teams

Snyk cloud context and Integrated IaC provide visibility into an Organization’s entire cloud footprint, allowing security teams to identify and investigate issues easily. Users view reports and focus on issues that have an impact on compliance. Support is provided for more than ten compliance standards, including CIS Benchmarks, PCI-DSS, and SOC 2.

### Code to cloud with the Snyk unified policy engine and ruleset

Integrated IaC uses the same unified policy engine as cloud context rather than the current IaC policy engine. This means you can apply the same security rules to both IaC files and runtime cloud resources. The Snyk unified policy engine enables consistent security testing across IaC files and deployed cloud resources, giving your security teams assurance that misconfigurations are correctly identified. In combination with the other Snyk products, this enables you to find and fix issues throughout the entire software development lifecycle (SDLC).

### Connect cloud back to IaC for faster fixes

Integrated IaC with Snyk cloud context enables you to [fix Cloud issues directly in the IaC source code](fix-cloud-issues-in-integrated-iac.md) that was used to deploy the misconfigured Cloud resources, via an SCM source code link to the cloud issue in the underlying IaC template. With Snyk, you can view resource configurations alongside IaC-specific remediation guidance.

### New Issues UI

Integrated IaC focuses on providing visibility into an Organization's issues across all its configuration templates. As a result, traditional Projects are currently not supported in Integrated IaC. Instead, [issues](cloud-and-integrated-iac-issues/) are on the new [Cloud tab](cloud-and-integrated-iac-issues/view-cloud-and-integragted-iac-issues-in-the-snyk-web-ui.md), which provides a snapshot of the resources that are misconfigured.

Resource configuration snapshots record the configuration attributes of every resource it scans for a user's configuration file, in contrast to the current IaC Projects view. This lets users review a resource’s configuration at a given moment in time and see the attributes that have caused a specific issue.

This allows security teams to identify and investigate issues easily. Users can view all of their infrastructure as code resources in a single, centralized interface.

### Powerful filters for triaging issues

You can filter issues based on parameters, including rule severity and resource type, allowing you to target the most mission-critical resources. You can also group issues by rule or by resource to more easily view relevant misconfigurations.

