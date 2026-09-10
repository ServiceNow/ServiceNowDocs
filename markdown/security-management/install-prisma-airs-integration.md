---
title: Install the Vulnerability Response Integration with Palo Alto Prisma AIRS
description: Install and configure the Vulnerability Response Integration with Palo Alto Prisma AIRS in your ServiceNow AI Platform instance. Import AI security scan results, posture findings, and model validation data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/install-prisma-airs-integration.html
release: zurich
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 2
breadcrumb: [Explore the Palo Alto Prisma AIRS Integration for AI Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Install the Vulnerability Response Integration with Palo Alto Prisma AIRS

Install and configure the Vulnerability Response Integration with Palo Alto Prisma AIRS in your ServiceNow AI Platform® instance. Import AI security scan results, posture findings, and model validation data.

## Before you begin

Role required: admin for installation and activation of the application.

The admin assigns the following ServiceNow AI Platform roles for this integration:

-   sn\_vul\_prisma\_airs.admin — Full access to manage integrations and read the AI security data.
-   sn\_vul\_prisma\_airs.read — Read-only access to view AI security data and integrations.

## Procedure

1.  Install the app-vul-prisma-airs application from yourServiceNow AI Platform instance.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Locate the Prisma AIRS application \[app-vul-prisma-airs\] and select **Install**.

        A confirmation dialog is displayed after the application is successfully activated.

2.  Navigate to **Prisma AIRS AI Security Integration** &gt; **Administration** &gt; **Configuration**.

3.  Configure the connection parameters and select **Save and test**.

    |Parameter|Description|Example|
    |---------|-----------|-------|
    |API base URL|Your Prisma AIRS API endpoint|For example, https://api.sase.paloaltonetworks.com|
    |Integration instance| |For example, Prisma AIRS|
    |Client ID|Client ID of your Prisma AIRS account|Client ID of your Prisma AIRS account|
    |Client secret|Client secret of your Prisma AIRS account|Client secret of your Prisma AIRS account|
    |Domain|The domain where your Prisma account is active.|For example, global|
    |Authorization URL|Authentication endpoint from Prisma AIRS|For example, https://auth.apps.paloaltonetworks.com/oauth2/access\_token|
    |Red Teams Scans Limit|Maximum number of scan records to retrieve per run|100|
    |Palo Alto Prisma tenant service group \(TSG\) ID|TSG ID of your Prisma AIRS account|TSG ID of your Prisma AIRS account, for example, 1420319896|
    |AI vulnerabilities page size limit|Maximum number of scan records to retrieve per run|100|
    |AI validation findings page size limit|Maximum number of validation records to retrieve per run|100|

4.  Navigate to **All** &gt; **Prisma AIRS AI Security Integration** &gt; **Integration Instances**

5.  Select Prisma AIRS to open the record and verify that the system creates the following integrations automatically.

    -   Prisma AIRS - AIMS Scans Integration — Retrieves scan summaries.
    -   Prisma AIRS - AIMS Scan Details Integration — Retrieves detailed scan findings.
    -   Prisma AIRS - Red Team Scans Integration — Retrieves validation job summaries.
    -   Prisma AIRS - Red Team Attacks Integration — Retrieves detailed validation results.
    -   Prisma AIRS - Red Team Scan Guardrails — Retrieves detailed guardrails information.
6.  Configure execution options for each integration.

    -   To run integrations on demand, use the **Execute Now** button. See [Running integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/install-prisma-airs-integration.md).
    -   To run integrations on a recurring schedule, configure a schedule for each integration. See the following section, [Running integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/install-prisma-airs-integration.md).
    **Note:** The integrations use business rules that are activated by default to process incoming data.


## Result

The Prisma AIRS integration is installed and configured. you're now ready to run integrations and view imported data in your instance.

## What to do next

Running integrations manually:

1.  Navigate to **Prisma AIRS AI Security Integration** &gt; **Integrations**.
2.  Find the integration that you want to run and select the record to open it.
3.  Select **Execute Now**.
4.  Monitor the import set for processing status.

Scheduling integrations:

1.  Navigate to **Prisma AIRS AI Security Integration** &gt; **Integrations**.
2.  Select a record to open it.
3.  Select the **Schedule** tab.
4.  Configure your desired frequency, for example, daily or hourly.
5.  Save the integration record.
6.  Perform these steps for each integration.

**Parent Topic:**[Explore the Palo Alto Prisma AIRS Integration for AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/prisma-airs-integration.md)

