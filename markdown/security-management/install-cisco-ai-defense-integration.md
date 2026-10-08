---
title: Install the Vulnerability Response Integration with Cisco AI Defense
description: Install and configure the ServiceNow AI Platform Integration with Cisco AI Defense application in your ServiceNow AI Platform instance to import scan results and model validation data from Cisco AI Defense.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/install-cisco-ai-defense-integration.html
release: zurich
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 2
breadcrumb: [Cisco AI Defense Integration for AI Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Install the Vulnerability Response Integration with Cisco AI Defense

Install and configure the ServiceNow AI Platform Integration with Cisco AI Defense application in your ServiceNow AI Platform® instance to import scan results and model validation data from Cisco AI Defense.

## Before you begin

If you have not already downloaded it onto your instance, visit the ServiceNow Store and locate the **Cisco AI Defense Integration for AI Security Exposure Management** application and download it onto your ServiceNow AI Platform® instance.

Obtain the following information from Cisco AI Defense before you configure the connection:

-   Integration instance \(name\)
-   API URL - Provided by Cisco for example - https://api.ciscoaidefense.com
-   Tenant API key — authentication key provided by Cisco

Role required: admin.

The admin assigns the following ServiceNow AI Platform roles for this integration:

-   Role required: admin for installation and activation of the application.
-   The admin assigns the following ServiceNow AI Platform roles for this integration:
    -   sn\_vul\_cisco\_ai\_df.admin — Full access to manage integrations and read the AI security data.
    -   sn\_vul\_cisco\_ai\_df.read — Read-only access to view AI security data and integrations.

## Procedure

1.  Install the Vulnerability Response Integration with Cisco AI Defense \[app-vul-cisco-ai-defense\] application you downloaded from the ServiceNow Store.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Locate the **Cisco AI Defense Integration for AI Security Exposure Management** application and select **Install**.

        A dialog box appears after the application is installed.

2.  Navigate to **All** &gt; **Cisco AI Defense Integration** &gt; **Administration** &gt; **Configuration**.

3.  Complete the configuration fields.

    |Field|Description|Example|
    |-----|-----------|-------|
    |Integration Instance|Name for your Cisco AI Defense Integration instance|Name for your Cisco AI Defense Integration|
    |API URL|Your Cisco AI Defense API endpoint|For example, https://api.ciscoaidefense.com|
    |Tenant API Key|Authentication key from Cisco|Your api key|

4.  Select **Save and test**.

5.  Navigate to **All** &gt; **Cisco AI Defense Integration** &gt; **Administration** &gt; **Integrations**.

6.  Confirm that the following integrations were created automatically.

    -   Cisco AI Defense Model Validation Details Integration — Retrieves detailed validation results.
    -   Cisco AI Defense Model Validation Integration — Retrieves validation job summaries.
    -   Cisco AI Defense Policies Integration — Retrieves policies.
    -   Cisco AI Defense Policy Details Integration — Retrieves policy details.
    -   Cisco AI Defense Scan Details Integration — Retrieves detailed model vulnerability scan findings.
    -   Cisco AI Defense Scans Integration — Retrieves vulnerability scan summaries.
7.  Select an integration record and configure execution options for each integration.

    -   Execute manually — Select **Execute Now**.
    -   Schedule automatically — Configure a schedule for each integration.
    See the steps in the following section.

    **Note:** The integrations use business rules that are activated by default to process incoming data.


## What to do next

After installation, run the integrations manually or on a schedule to pull data from Cisco AI Defense.

Manual execution:

1.  Find the record for the Cisco AI Defense integration that you want to run.
2.  Select **Execute Now**.
3.  Monitor the import set for processing status.

Scheduled execution:

1.  Navigate to **All** &gt; **Cisco AI Defense Integration** &gt; **Administration** &gt; **Integrations**.
2.  Open an integration record.
3.  Locate the **Schedule** tab and select it.
4.  Configure your desired frequency \(for example, daily or hourly\).
5.  Save the integration.

You're now ready to view your Cisco AI Defense data in your instance.

**Parent Topic:**[Cisco AI Defense integration for AI security exposure management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/exploring-cisco-ai-defense-integration.md)

