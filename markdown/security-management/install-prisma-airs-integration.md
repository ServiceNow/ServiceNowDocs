---
title: Install the Vulnerability Response integration with Palo Alto Prisma AIRS
description: Use this task to set up the Vulnerability Response integration with Palo Alto Prisma AIRS and import AI security scan results, posture findings, and model validation data into your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/install-prisma-airs-integration.html
release: brazil
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 2
breadcrumb: [Palo Alto Prisma AIRS Integration for AI Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Install the Vulnerability Response integration with Palo Alto Prisma AIRS

Use this task to set up the Vulnerability Response integration with Palo Alto Prisma AIRS and import AI security scan results, posture findings, and model validation data into your ServiceNow AI Platform® instance.

## Before you begin

Obtain the following information from Palo Alto Prisma AIRS before configuring the connection:

-   API Base URL \(default: `https://api.sase.paloaltonetworks.com`\)
-   Client ID - Provided by Palo Alto
-   Client Secret - Provided by Palo Alto
-   Tenant Service Group \(TSG\) ID - Provided by Palo Alto

If you have not already downloaded it onto your instance, visit the ServiceNow® Store and locate the **Prisma AIRS Integration for AI Security Exposure Management** application and download it onto your ServiceNow AI Platform® instance.

Role required: admin for downloading and installing the application.

The admin assigns the following ServiceNow AI Platform roles for this integration:

-   sn\_vul\_prisma\_airs.admin—Full access to manage integrations and read the AI security data.
-   sn\_vul\_prisma\_airs.read—Read-only access to view AI security data and integrations.

## Procedure

1.  Install the app-vul-prisma-airs application you downloaded from the ServiceNow Store.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Locate the **Palo Alto Prisma AIRS Integration for AI Security Exposure Management** and select **Install**.

        A confirmation dialog is displayed.

2.  Navigate to **All** &gt; **Prisma AIRS AI Security Integration** &gt; **Administration** &gt; **Configuration**.

3.  Configure the connection parameters.

    |Parameter|Description|Example|
    |---------|-----------|-------|
    |API base URL|Your Prisma AIRS API endpoint|`https://api.sase.paloaltonetworks.com`|
    |Integration instance| |Prisma AIRS|
    |Client ID|Client ID of your Prisma AIRS account|your-client-id-value|
    |Client secret|Client secret of your Prisma AIRS account|your-client-secret-value|
    |Domain|The domain where your Prisma account is active.|global|
    |Authorization URL|Authentication endpoint from Prisma AIRS|`https://auth.apps.paloaltonetworks.com/oauth2/access_token`|
    |Red Teams Scans Limit|Maximum number of scan records to retrieve per run|100|
    |Palo Alto Prisma tenant service group \(TSG\) ID|TSG ID of your Prisma AIRS account|TSG ID of your Prisma AIRS account, for example, 1420319896|
    |AI vulnerabilities page size limit|Maximum number of scan records to retrieve per run|100|
    |AI validation findings page size limit|Maximum number of validation records to retrieve per run|100|

4.  Select **Save and test**.

5.  Navigate to **All** &gt; **Prisma AIRS AI Security Integration** &gt; **Integration Instances**.

6.  Select **Prisma AIRS** in the Name column to open the record and verify that the system has created the following integrations.

    -   Prisma AIRS - AIMS Scans Integration — Retrieves scan summaries.
    -   Prisma AIRS - AIMS Scan Details Integration — Retrieves detailed scan findings.
    -   Prisma AIRS - Red Team Scans Integration — Retrieves validation job summaries.
    -   Prisma AIRS - Red Team Attacks Integration — Retrieves detailed validation results.
    -   Prisma AIRS - Red Team Scan Guardrails — Retrieves detailed guardrails information.
7.  Select a record to open it.

8.  Configure execution options for each integration.

    **Note:** The integrations use business rules that are activated by default to process incoming data.


## Result

The Prisma AIRS integration is installed and configured. You're now ready to run integrations and view imported data in your instance.

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

