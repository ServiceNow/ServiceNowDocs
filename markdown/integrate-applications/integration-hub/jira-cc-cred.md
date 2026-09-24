---
title: Create credential record for the Jira spoke
description: Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/jira-cc-cred.html
release: brazil
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Option 2: Using OAuth authentication \(Client Credentials grant type\), Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create credential record for the Jira spoke

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira spoke. For example, `Jira client credential cred`.|
    |OAuth Entity Profile|Select the OAuth entity profile record that was created when the application registry record is configured. For more information, see [Create an application registry record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/jira-setup-cc-app-reg.md).|

5.  Right-click the form header and click **Save**.

6.  Click the **Get OAuth Token** related link.


