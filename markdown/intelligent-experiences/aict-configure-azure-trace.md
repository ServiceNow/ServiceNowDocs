---
title: Add an Azure trace connection
description: Monitor AI agents running on Microsoft Azure by adding an Azure trace connection. AI Control Tower collects trace data through your Azure credentials and a MID Server, without requiring SDK instrumentation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configure-azure-trace.html
release: zurich
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an Azure trace connection

Monitor AI agents running on Microsoft Azure by adding an Azure trace connection. AI Control Tower collects trace data through your Azure credentials and a MID Server, without requiring SDK instrumentation.

## Before you begin

Confirm the following:

-   An active MID Server is installed and configured in your ServiceNow instance. See [MID Server installation](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-installation.html).
-   Credentials for the Azure source system you plan to configure are available.
    -   Each credential must be created in Azure for the source system it applies to.
    -   The Azure service principal or managed identity behind each OAuth-based credential has the Reader role on the resource or resource group it collects traces from.
    -   The Azure Application Insights API key credential, used for the **New Foundry** source system, has the "Read telemetry" permission.
    -   After each credential is created in Azure, work with your instance administrator to store it as a record in your instance. For details, see the [Azure Trace Collector Credentials Configuration \[KB3144350\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144350) article in Now Support.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  On the **Available** sub-tab, select **Azure**.

3.  Select the Azure source systems to integrate with.

    -   **Classic Foundry** — collects traces from Azure AI Foundry \(classic\).
    -   **New Foundry** — collects traces from the updated Azure AI Foundry experience.
    -   **Application Insights** — collects traces from Azure Monitor Application Insights.
4.  Fill in the credentials for the source system you selected.

<table id="choicetable-azure-credentials"><thead><tr><th align="left" id="d226025e175">

Source system

</th><th align="left" id="d226025e178">

Steps

</th></tr></thead><tbody><tr><td id="d226025e184">

**Classic Foundry**

</td><td>

1.  Enter a descriptive name for the connection.

The name distinguishes this connection from others you create. For instance, you may choose a name that identifies the account, project, or environment.

2.  Select the Azure AI Services OAuth 2.0 credential alias in the **Azure AI Services Credential Alias** field.
3.  Select the Azure Machine Learning Services OAuth 2.0 credential alias in the **Azure Machine Learning Credential Alias** field.
4.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

5.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

6.  Select **Active** to begin collecting traces when you save. Clear this option to save the connection without starting collection. You can activate the connection later from its record.


</td></tr><tr><td id="d226025e236">

**New Foundry**

</td><td>

1.  Enter a descriptive name for the connection.

The name distinguishes this connection from others you create. For instance, you may choose a name that identifies the account, project, or environment.

2.  Select the Application Insights API key credential in the **Application Insights Credential** field.
3.  Select the Azure Machine Learning Services OAuth 2.0 credential in the **Azure Machine Learning Credential** field.
4.  Enter the **Application Insights Application ID**.

Find this value in the Azure portal, under your Application Insights resource settings.

5.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

6.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

7.  Select **Active** to begin collecting traces when you save. Clear it to save the connection without starting collection. You can activate the connection later from its record.


</td></tr><tr><td id="d226025e296">

**Application Insights**

</td><td>

1.  Enter a descriptive name for the connection.

The name distinguishes this connection from others you create. For instance, you may choose a name that identifies the account, project, or environment.

2.  Select the Azure App Insights OAuth 2.0 credential alias in the **Azure App Insights Credential** field.
3.  Select the Azure Machine Learning Services OAuth 2.0 credential alias in the **Azure Machine learning credential** field.
4.  Enter the **Application Insights Resource ID**.

Find this value in the Azure portal, under your Application Insights resource settings.

5.  Select the MID Server that runs trace collection.

The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.

6.  Enter the interval, in minutes, at which the MID Server polls for new trace data in the **Collection frequency \(minutes\)** field.

The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.

7.  Select **Active** to begin collecting traces when you save. Clear it to save the connection without starting collection. You can activate the connection later from its record.


</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The trace connection appears on the **Established** sub-tab. If the connection is active, AI Control Tower begins collecting trace data after the first polling interval.

## What to do next

Choose which metrics to include in evaluation scoring. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md)

