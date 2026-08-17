---
title: Configuring trace connections
description: Collect trace data from AI agents running on supported cloud platforms and monitoring services to generate evaluation metrics, populate AI inventory, and support security monitoring in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configuring-trace-connections.html
release: zurich
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Configuring trace connections

Collect trace data from AI agents running on supported cloud platforms and monitoring services to generate evaluation metrics, populate AI inventory, and support security monitoring in AI Control Tower.

## Key benefits

-   Collect trace data from AWS, Google Cloud, and Microsoft Azure platforms through a single interface, without SDK instrumentation in your agent code.
-   Discover AI agents running on third-party platforms and add them to your AI asset inventory automatically.
-   Generate evaluation and security metrics from collected traces when evaluations and security monitoring capabilities are enabled.
-   Access cloud platforms securely through a MID Server, which authenticates to your cloud provider and keeps credentials protected within your ServiceNow instance.

## Trace connections and SDK instrumentation

AI Control Tower supports two ways to collect trace data from AI systems: a trace connection, which polls a supported cloud platform at a configured interval, or SDK instrumentation, which sends trace data using an API key. Use a trace connection when your AI systems run on a supported platform.

For AI systems hosted on other platforms or third-party agents, send trace data using the API instead. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

## Trace connection limitations

-   Up to 5 trace connections for each connector run in parallel. You can create more than 5, but only 5 run at a time.
-   Manually running a trace connection, instead of waiting for its scheduled interval, counts against a separate limit: up to 2 manual runs at a time.

-   **[Add an AWS CloudWatch trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configure-aws-cloudwatch-trace.md)**  
Monitor AI agents built with AWS Bedrock AgentCore by adding an AWS CloudWatch trace connection. AI Control Tower collects trace data through your AWS credentials and a MID Server, without requiring SDK instrumentation.
-   **[Add an Azure trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configure-azure-trace.md)**  
Monitor AI agents running on Microsoft Azure by adding an Azure trace connection. AI Control Tower collects trace data through your Azure credentials and a MID Server, without requiring SDK instrumentation.
-   **[Add a GCP Cloud Trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configure-gcp-cloud-trace.md)**  
Monitor AI agents running on Google Cloud by adding a GCP Cloud Trace connection. AI Control Tower collects trace data through your Google Cloud credentials and a MID Server, without requiring SDK instrumentation.
-   **[Troubleshoot a trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-troubleshoot-trace-connection.md)**  
Identify why a trace connection is not collecting data by reviewing its execution log and error messages.
-   **[Edit a trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-edit-trace-connection.md)**  
Update the configuration of an established trace connection to change its credentials, collection frequency, MID Server, or other settings.
-   **[Deactivate a trace connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-deactivate-trace-connection.md)**  
Stop trace collection for an established connection without deleting it, so you can reactivate it later.

**Parent Topic:**[Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-integrations.md)

