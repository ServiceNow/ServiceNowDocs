---
title: Install and configure AI Security Exposure Management
description: Install and configure the required applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/ai-security-exposure-install-config.html
release: australia
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 3
breadcrumb: [Configure AI skills and agentic workflows, Implement, Unified Security Exposure Management, Security Operations]
---

# Install and configure AI Security Exposure Management

Install and configure the required applications.

## Before you begin

The following ServiceNow Plugins are required:

-   Unified Security Exposure Management \(sn\_vul\_usem\_common\)
-   AI Security Exposure Management \(sn\_sec\_ai\).
-   AI Security Common \(sn\_sec\_ai\_cmn\).
-   \(Optional\) If you want to use the AI guardrails helper skill and agentic workflow you must install the Now Assist for Vulnerability Response application \(sn\_vul\_ai\).
-   Vulnerability Response and Configuration Compliance for Containers \(sn\_vul\_container\)
-   Vulnerability Response \(sn\_vul\)
-   Configuration Compliance \(sn\_vulc\)

At least one of these AI defense integrations supported by the application must be installed and activated.

-   Cisco AI Defense Integration - import AI security exposures such as model vulnerabilities and model validation findings \(automated red teaming alerts\).
-   Palo Alto Prisma AIRS Integration

Although not mandatory, it's recommended that you install the one of the following service graph connectors. You should choice depends on the AI security tool that you're using in your organization to import AI inventory data into your CMDB.

-   AI Service Graph Connector for Palo Alto Prisma AIRS.
-   AI Service Graph Connector for HiddenLayer - import AI asset inventory data.

Role required: admin

## Procedure

1.  Log in to the instance you want to install the AI Security Exposure Management application on.

2.  Navigate to the ServiceNow Store.

3.  In the ServiceNow Store, search for the AI Security Exposure Management application.

4.  Select the application tile.

    **Note:**

    In the ServiceNow Store, you must verify that you have entitlements \(or licenses\) to the application and its dependent applications. After you have logged in, you can use the menu in the upper right with your initials to manage entitlements and opt-in.

    This application is compatible with Unified Security Exposure Management \(USEM\). See [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/migrating-to-usem.md) for more information about USEM and the Unified Security Exposure Management migration.

5.  Select **Request Install**.

6.  Log in to the ServiceNow AI Platform instance where you want to install the application.

7.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

8.  From the applications listed, locate the AI Security Exposure Management application, select a version from the list, and select **Install**.

    The Application installation dialog is displayed. Any dependencies that are installed are displayed.

    **Note:** The AI guardrails helper is a Now Assist skill that is activated by default. See [Exploring Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/exploring-ai-for-now-assist-for-vulnerability-response.md) and [Using generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/using-now-assist-skills-vulnerability-response.md) for more information about skills and agents.

9.  Select **Close** after the application is successfully installed.

10. Assign the following AISEC roles:

    -   sn\_sec\_ai.remediation\_owner - Can read and update AI Security Exposure Management findings and remediation tasks assigned to the user or their groups.
    -   sn\_sec\_ai.vulnerability\_admin - Full administrative access to all AI Security Exposure Management findings, scans, and remediation tasks.
    -   sn\_sec\_ai.vulnerability\_analyst -Can view and update all AI Security Exposure Management scan findings and remediation tasks.
    -   Add sn\_sec\_ai\_read and write roles to a persona and add that persona to sn\_sec\_ai.vulnerability\_analyst.
    Assign the following Infrastructure Vulnerability Response roles.

    -   sn\_vul.remediation\_owner - Reads and writes vulnerable items and remediation tasks assigned to them. Vulnerability and Solution records are readable by user with this role.
    -   sn\_vul.vulnerability\_admin - Configures all rules, integrations, etc. for the Vulnerability Response product.
    -   sn\_vul.vulnerability\_analyst - Monitors remediation of all vulnerable items.
    Assign the following Container Vulnerability Response roles.

    -   sn\_vul\_container.remediation\_owner - Reads and writes container vulnerable items assigned to them. Vulnerability records are also readable by user with this role.
    -   sn\_vul\_container.vulnerability\_admin - Configures all rules, integrations, etc. for the Container Vulnerability Response product.
    -   sn\_vul\_container.vulnerability\_analyst - Monitors remediation of all container vulnerable items.
    Assign the following Configuration Compliance roles.

    -   sn\_vulc.admin - Configuration Compliance administrator is able to modify application property and configuration.
    -   sn\_vulc.remediation\_owner - Configuration Compliance related records can be remediated by the user with this role.
    -   sn\_vulc.vulnerability\_analyst - Monitors remediation of all test results.
    Assign other findings-related roles for sn\_sec\_ai.\* tables that users might require access to.

    See [Viewing AI Exposures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/ai-security-exposure-home.md) for more information about the AI Security Exposure Management tables.


