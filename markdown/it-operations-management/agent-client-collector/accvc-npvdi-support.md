---
title: ACC-VC NPVDI endpoints
description: Agent Client Collector for Visibility Content \(ACC-VC\) adjusts how its discovery and software checks run on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints, so that data collected during a short-lived session reaches your instance before the session ends.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/accvc-npvdi-support.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 4
keywords: [Agent Client Collector for Visibility, ACC-VC, non-persistent VDI, NPVDI]
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# ACC-VC NPVDI endpoints

Agent Client Collector for Visibility Content \(ACC-VC\) adjusts how its discovery and software checks run on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints, so that data collected during a short-lived session reaches your instance before the session ends.

## How ACC-VC identifies an NPVDI endpoint

An NPVDI endpoint is a virtual desktop that is provisioned from a golden image for each user session and is reset or removed when the user logs off. Because the endpoint might not exist at the next scheduled discovery interval, ACC-VC changes when and how certain checks run on these endpoints so that session data isn't lost.

NPVDI support applies only to non-persistent Windows agents. Discovery of persistent Windows, macOS, and Linux devices remains unchanged. ACC-VC doesn't detect NPVDI endpoints automatically. An endpoint that isn't explicitly configured as non-persistent, including an endpoint with missing or unclear configuration, is treated as a persistent endpoint. The agent is marked as non-persistent when you install it on the golden image. For more information, see [Enable a non-persistent virtual desktop infrastructure agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/enable-npvdi-agent.md).

## ACC-VC policies that support NPVDI

The following VDI policies list determines which policies run on NPVDI agents. ACC-VC has already added the following policies to this list, so you don't have to add them yourself. The list has no effect on persistent endpoints.

-   **Enhanced Discovery**
-   **SAM Discovery**
-   **SAM background**
-   **SAM background \(Non OsqueryD\)**

For more information about each policy, see [Agent Client Collector for Visibility Content default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-visibility-checks-policies.md).

The **Software installed** policy isn't registered as a VDI policy because it applies only to servers. To add other published policies to an NPVDI agent, see [Prepare agent deployment on a non-persistent virtual desktop infrastructure machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/npvdi-agent-instance-prep.md).

## Data collection when an NPVDI session ends

The SAM Discovery policy runs on its regular schedule and also when the endpoint shuts down. Each run sends the software installation data it collects to your instance. The shutdown run makes sure that data collected since the previous run reaches your instance before the session and its data are removed.

The Enhanced Discovery, SAM background, and SAM background \(Non OsqueryD\) policies run on their regular schedule only.

## Reduced Enhanced Discovery on NPVDI endpoints

Some **Enhanced Discovery** inventory modules don't have to be collected again in every short-lived session. On NPVDI endpoints, ACC-VC can skip the following modules:

-   File systems
-   Network adapters
-   Storage devices
-   Local users
-   Intel EMA
-   Memory modules

By default, all six modules are skipped. You control the skipped modules and whether the installed software scan results are cached within the same session with a system property. For details, see [Configure ACC-VC data collection for NPVDI endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/configure-accvc-npvdi-data-collection.md).

The following inventory areas run on every check and can't be skipped:

-   **Basic Inventory**
-   **Enhanced Inventory**
-   **TCP Connections**
-   **Running Processes**

## Installed software caching on NPVDI endpoints

The software installations and usage metrics check discovers the software installed on an endpoint and collects usage metrics for that software, such as last used date and total usage duration.

On NPVDI endpoints, you can enable caching of the installed software inventory. When caching is enabled, the full installed software scan runs one time for each golden image. Later check runs reuse the cached results instead of rescanning. Caching is turned off by default.

Caching applies only to the installed software inventory. Software usage metrics are collected on every check run, because usage is specific to each session and can't be reused.

## Behavior when NPVDI configuration is unavailable

If an NPVDI endpoint can't read its NPVDI configuration, for example, because the acc.yml file is missing or malformed, ACC-VC doesn't skip any Enhanced Discovery modules and treats caching as turned off. Discovery then runs the same way it does on a persistent endpoint.

-   **[Configure ACC-VC data collection for NPVDI endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/configure-accvc-npvdi-data-collection.md)**  
Choose which **Enhanced Discovery** modules Agent Client Collector for Visibility Content \(ACC-VC\) skips on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints. Optionally, choose whether installed software scan results are cached within the same session.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

