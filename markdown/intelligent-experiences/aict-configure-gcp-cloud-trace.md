---
title: Add a GCP Cloud Trace connection
description: Monitor AI agents running on Google Cloud by adding a GCP Cloud Trace connection. AI Control Tower collects trace data through your Google Cloud credentials and a MID Server, without requiring SDK instrumentation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configure-gcp-cloud-trace.html
release: zurich
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add a GCP Cloud Trace connection

Monitor AI agents running on Google Cloud by adding a GCP Cloud Trace connection. AI Control Tower collects trace data through your Google Cloud credentials and a MID Server, without requiring SDK instrumentation.

## Before you begin

Confirm the following:

-   An active MID Server is installed and configured in your ServiceNow instance. See [MID Server installation](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-installation.html).
-   A Google Cloud OAuth 2.0 credential with permission to read trace data is available.
    -   The credential must be configured in Google Cloud. For details, see the [Configuring GCP Permissions and Credentials for ServiceNow AI Control Tower Trace Ingestion \[KB3144347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144347) article in Now Support.
    -   After the credential is configured in Google Cloud, work with your instance administrator to store it as a new Google Cloud credential record in **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  On the **Available** sub-tab, select **GCP Cloud Trace**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name for this trace connection. Use a name that distinguishes this connection from others you create, such as one that identifies the account, project, or environment.|
    |**Collection frequency \(minutes\)**|Interval, in minutes, at which the MID Server polls for new trace data. The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.|
    |**Credential**|Google Cloud OAuth 2.0 credential that authenticates AI Control Tower to GCP Cloud Trace. The credential must have permission to read trace data.|
    |**MID server**|MID Server that runs trace collection. The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.|
    |**Active**|Option to begin collecting traces when you save the connection. Clear it to save the connection without starting collection. You can activate the connection later from its record.|

4.  Select **Save**.


## Result

The trace connection appears on the **Established** sub-tab. If the connection is active, AI Control Tower begins collecting trace data after the first polling interval.

## What to do next

Choose which metrics to include in evaluation scoring. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md)

