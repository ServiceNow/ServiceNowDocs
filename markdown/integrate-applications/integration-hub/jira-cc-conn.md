---
title: Create a connection record for the Jira spoke
description: Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/jira-cc-conn.html
release: brazil
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Option 2: Using OAuth authentication \(Client Credentials grant type\), Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection record for the Jira spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for **Jira** that shipped with the spoke.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values and click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Jira cloud OAuth Connection`.|
    |Credential|Select the Credential record created for Jira. For example, select **Jira cloud OAuth credential**.|
    |Connection URL|Enter the URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/<Cloud-ID>`.|

5.  Click **Submit**.

    The Jira spoke is configured to use OAuth 2.0 Client Credentials via the service account.


