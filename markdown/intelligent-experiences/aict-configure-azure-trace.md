---
title: Add an Azure trace connection
description: Monitor AI agents running on Microsoft Azure by adding an Azure trace connection. AI Control Tower collects trace data through your Azure credentials and a MID Server, without requiring SDK instrumentation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-azure-trace.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an Azure trace connection

Monitor AI agents running on Microsoft Azure by adding an Azure trace connection. AI Control Tower collects trace data through your Azure credentials and a MID Server, without requiring SDK instrumentation.

## Before you begin

Confirm the following:

-   An active MID Server is installed and configured in your ServiceNow instance. See [MID Server installation](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-installation.html).
-   Credentials for each Azure source system you plan to configure are available.
    -   Each credential must be created in Azure for the source system it applies to. For details, see the [Azure Trace Collector Credentials Configuration \[KB3144350\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144350) article in Now Support.
    -   After each credential is created in Azure, work with your instance administrator to store it as a record in **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  On the **Available** sub-tab, select **Azure**.

3.  Enter a descriptive name for the connection.

    The name distinguishes this connection from others you create. For instance, you may choose a name that identifies the account, project, or environment.

4.  Select the Azure source systems to integrate with.

    -   **Classic Foundry** — collects traces from Azure AI Foundry \(classic\).
    -   **New Foundry** — collects traces from the updated Azure AI Foundry experience.
    -   **Application Insights** — collects traces from Azure Monitor Application Insights.
5.  Select **Next**.

6.  Fill in the credentials for each source system you selected.

    If you selected multiple source systems, provide the credentials for the first system and then select **Next** to continue to the credentials page for the next source system.

<table id="choicetable-azure-credentials"><thead><tr><th align="left" id="d254009e199">

Source system

</th><th align="left" id="d254009e202">

Steps

</th></tr></thead><tbody><tr><td id="d254009e208">

**Classic Foundry**

</td><td>

1.  Select the name of the credential in the **Azure AI Services Credential Alias** field.
2.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

3.  Select the name of the credential in the **Azure Machine Learning Credential Alias** field.
4.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

5.  Select **Active** to begin collecting traces when you save. Clear this option to save the connection without starting collection. You can activate the connection later from its record.


</td></tr><tr><td id="d254009e254">

**New Foundry**

</td><td>

1.  Select the name of the OAuth 2.0 credential in the **Azure Machine Learning Credential** field.
2.  Select the name of the API key credential in the **Application Insights Credential** field.
3.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

4.  Enter the **Application Insights Application ID**.
5.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

6.  Select **Active** to begin collecting traces when you save. Clear it to save the connection without starting collection. You can activate the connection later from its record.


</td></tr><tr><td id="d254009e307">

**Application Insights**

</td><td>

1.  Select the name of the OAuth 2.0 credential in the **Azure App Insights Credential** field.
2.  Enter the **Application Insights Resource ID**.
3.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

4.  Select the name of the OAuth 2.0 credential in the **Azure Machine Learning Credential** field.
5.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

6.  Select **Active** to begin collecting traces when you save. Clear it to save the connection without starting collection. You can activate the connection later from its record.


</td></tr></tbody>
</table>7.  Select **Save**.


## Result

One or more trace connections appear on the **Established** sub-tab. If the connection is active, AI Control Tower begins collecting trace data after the first polling interval.

## What to do next

Choose which metrics to include in evaluation scoring. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md)

