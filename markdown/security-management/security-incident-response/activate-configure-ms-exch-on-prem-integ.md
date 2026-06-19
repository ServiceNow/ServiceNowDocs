---
title: Get started with the Microsoft Exchange On-Premises integration
description: The Microsoft Exchange On-Premises integration provides tools for security analysts to contain and remediate phishing and spear phishing email threats in on-premises instances. Before you can use the Microsoft Exchange On-Premises integration, you must download it from the ServiceNow Store and identify the appropriate Exchange and MID servers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/activate-configure-ms-exch-on-prem-integ.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Exchange On-Premises integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Microsoft Exchange On-Premises integration

The Microsoft Exchange On-Premises integration provides tools for security analysts to contain and remediate phishing and spear phishing email threats in on-premises instances. Before you can use the Microsoft Exchange On-Premises integration, you must download it from the ServiceNow Store and identify the appropriate Exchange and MID servers.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/download-app-first-time.md).

2.  When the installation os complete, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

3.  Select **Configure**.

4.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |Exchange Server|Specify the Exchange server to be used.|

    **Note:** Configuring this integration activates flows. To manage the flows, navigate to the **Workflow Studio/ Flow Designer**.

5.  Select **Submit**.

    The integration configuration card displays.

6.  When viewing the new configuration card, you can select **Configure** or **Delete** to change or delete the configuration, respectively.

7.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.

8.  Navigate to **Orchestration** &gt; **MID Servers**.

9.  Open the record and verify the status of the MID Server which is reachable to the exchange server and its **Status** option is set to **Up** and **Validated** option as **Yes**.

10. Add the MID Server capability:

    -   Select the respective MID Server to add the capability.
    -   select on the **Capabilities** related list and select **Edit**.
    -   Remove **All** and add **Microsoft Exchange Server for SecOps**.
    -   Select the **IP Ranges** from the **Related Lists** section and set the value to either **ALL** or any desired value.
    -   Select the **Supported Applications** from the **Related Lists** section and either set the value to ALL or Orchestration.
    -   **Save** the record.
11. Validate the connections &amp; credentials.

    -   Navigate to Orchestration &gt; Credentials &amp; Connections &gt; Credentials.
    -   Select **New** to create credentials for the MID Server.
    -   Select **Windows Credentials**.
    -   Enter **Username** and **Password**.
    -   Select **Submit**.
    -   Select **Test Credential** in related links.
    -   Enter target, port, MID Server.
    -   Select **OK** and validate your connection and credentials.
12. Once the credentials are validated, the configuration on ServiceNow instance is complete and is ready to perform email search and deletion operations using this integration.


