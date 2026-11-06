---
title: ServiceNow Vault release notes
description: The ServiceNow Vault application provides a set of data security tools that protect sensitive information from unauthorized access, corruption, or theft throughout its entire life cycle. See the following sections for release notes by version.For the November 2026 release of ServiceNow Vault, Vault Suite version 1.1.1 no longer includes Code Signing.For the October 2026 release of ServiceNow Otto for Vault version 3.1, use an agentic workflow to classify sensitive data across a large table estate without labeling each column by hand, and stay informed about data protection coverage with a monthly Vault coverage report email.ServiceNow Vault reduces the effort of monitoring and protecting sensitive data, adding AI-generated Insights, code signing metrics, and log export monitoring to Vault Console, generating module access policies as part of field encryption, and applying Zero Trust Access default policies on install.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/servicenow-vault-rn.html
release: australia
topic_type: topic
last_updated: "2026-07-13"
reading_time_minutes: 5
keywords: [ServiceNow Vault, Vault Suite, code signing, ServiceNow Vault, Vault Console, ServiceNow Otto for Vault, Vault by Default, data discovery, data classification, anonymization, Workflow Data Fabric, ServiceNow Vault, Vault Console, ServiceNow Otto for Vault, Vault by Default, data classification, anonymization, Zero Trust Access, code signing, Log Export Service]
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Vault release notes

The ServiceNow Vault application provides a set of data security tools that protect sensitive information from unauthorized access, corruption, or theft throughout its entire life cycle. See the following sections for release notes by version.

## About ServiceNow Vault

-   Protect sensitive data across its entire life cycle by implementing encryption, data discovery, classification, anonymization, zero trust access, code signing, and log export from a unified console.
-   Accelerate deployment by installing the Vault Suite application to activate all data security capabilities within ServiceNow Vault automatically in a single step, eliminating manual plugin configuration.
-   Automate security administration tasks using AI capabilities provided by the ServiceNow Otto for Vault application to generate custom data patterns, recommend data classifications for applications, monitor data access, and secure custom applications
-   Gain visibility into your security posture with a centralized dashboard that track metrics across all Vault tools.
-   ServiceNow Vault is a bundle of the following products:
    -   
    -   
    -   
    -   
    -   
    -   
    -   

See  for more information.

**Important:** For Now LLM Service model updates for each release, see .

## Activation and other requirements

**Note:** ServiceNow Vault is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install Vault Console, Vault Suite and ServiceNow Otto for Vault by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html). Vault console is available for free installation, but a ServiceNow Vault subscription is required to access its full features.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-security-rn-landing.md)

## Brazil Patch 1

For the November 2026 release of ServiceNow Vault, Vault Suite version 1.1.1 no longer includes Code Signing.

### What's deprecated or removed

-   **Code Signing in Vault Suite**

    Code Signing is no longer included in Vault Suite. Installing Vault Suite doesn't install Code Signing. On instances that already have Code Signing, it no longer appears in Vault Console.


## Version 3.1

For the October 2026 release of ServiceNow Otto for Vault version 3.1, use an agentic workflow to classify sensitive data across a large table estate without labeling each column by hand, and stay informed about data protection coverage with a monthly Vault coverage report email.

### What's new

-   **Agentic classification for ServiceNow assets**

    Classify sensitive data across a large table estate without labeling each column by hand. Select a category of ServiceNow assets in the Data Catalog, and the agent recommends a data class for each column in scope, with the reason for each recommendation. Recommendations are based on schema metadata, such as table and column names and any existing classifications. Review the recommendations and then confirm to apply them. The classifications appear on the data assets after the next ServiceNow metadata collector run.

-   **Vault coverage report email**

    Stay informed about how much of your sensitive data is protected with a Vault coverage report email. Active administrators receive it on the last Monday of each month. The email is sent only when Vault finds sensitive columns on your instance.


### What's changed

-   **Vault onboarding email design**

    The Vault onboarding email uses an updated template design.


## Brazil Early Availability

ServiceNow Vault reduces the effort of monitoring and protecting sensitive data, adding AI-generated Insights, code signing metrics, and log export monitoring to Vault Console, generating module access policies as part of field encryption, and applying Zero Trust Access default policies on install.

### What's new

-   **AI-generated security posture summary**

    Reduce the time you spend interpreting individual charts by reading an AI-generated summary of your data security, with a recommended next step for each area. Insights appears at the top of the Vault console home page and reports on data discovery, classification, and data protection.

-   **Field encryption and auto-generate access policies agentic workflow**

    Keep encrypted fields readable for the roles that need them by creating the module access policies as part of field encryption. Request encryption for a table field, review the roles that currently have access to it, and confirm the final list. The workflow creates a module access policy for each confirmed role and then encrypts the field, so you no longer review access control lists or Access Observer logs to build the role list yourself.

-   **Zero Trust Access default policies**

    Protect access to data from the start by automatically applying default step-up authentication policies when you install Zero Trust Access with ServiceNow Vault. Review these default policies at any time from Vault Console.

-   **Code signing activity metrics in Vault Console**

    Monitor code signing activity across your instance by tracking the create, update, and delete operations applied to code signing enabled records over the past week, and see which tables have the most such records.

-   **Log Export Service export monitoring widget**

    Monitor your instance's log export activity by tracking total data exported over the past six months, the topics that export the most data, and the data exported by each topic so far in the current month.

-   **ServiceNow Vault in Admin Home**

    Discover and install ServiceNow Vault from Admin Home. Instances with a ServiceNow Vault entitlement show a ServiceNow Vault tile, where an administrator can install Vault Suite and then open the Vault Console from the Configuration Console.

-   **Vault onboarding email notification**

    Receive an email notification when ServiceNow Vault onboarding completes on your instance.


### What's changed

-   **ServiceNow Otto name change**

    ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **Role masking in the Access Observer and Field Encryption workflows**

    The security\_admin role isn't part of the sn\_vault\_console.vault\_console\_admin role. To use the Access Observer and Field Encryption agentic workflows, assign the security\_admin role to sn\_vault\_console.vault\_console\_admin users, and then elevate to security\_admin.

-   **Default policy naming**

    Default policies provisioned for field encryption, data privacy, Zero Trust Access, and Log Export Service are prefixed with Vault by Default, so you can distinguish policies that ServiceNow provisioned from policies your organization created.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


