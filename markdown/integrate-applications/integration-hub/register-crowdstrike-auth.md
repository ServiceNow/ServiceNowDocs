---
title: Register a CrowdStrike OAuth application
description: Register the CrowdStrike OAuth application to access the CrowdStrike API and to receive a Client ID and Client secret.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Register a CrowdStrike OAuth application

Register the CrowdStrike OAuth application to access the CrowdStrike API and to receive a Client ID and Client secret.

## Before you begin

The CrowdStrike Integration Hub spoke must be active. For more information, see [CrowdStrike spoke](../concept/crowdstrike-spoke.md).

Role required: CrowdStrike Falcon administrator

**Important:**

-   To use the Sensor Usage APIs, your API client must be assigned the Sensor usage scope with read permissions.
-   To use the Look up Hourly Sensor Usage and Look up Weekly Sensor Usage actions, contact your account team to enable the following feature flags:
    -   Hourly usage data feature flag: This flag must be enabled for your Customer Identification \(CID\) to view hourly usage data.
    -   Aggregated usage data feature flag: This flag must be enabled to get aggregated usage data in multi-CID \(non-Flight Control\) accounts.

## Procedure

1.  Log in to [Falcon](https://falcon.crowdstrike.com/login/) using your admin credentials.

2.  Navigate to **Support** &gt; **API Clients and Keys**.

3.  Select **Add new API Client**.

4.  Provide the client name and description.

5.  Select the appropriate check boxes for the following scopes:

    -   To use the Look up Active Hosts and Look up Host Details actions, select the **Read** check box for the **Hosts** scope.
    -   To use the Look up Hourly Sensor Usage and Look up Weekly Sensor Usage actions, select the **Read** check box for the **Sensor usage** scope
    -   To use all the supported actions, select the **Read** check box for both **Hosts** and **Sensor usage** scopes.
6.  Select **ADD**.

    The API client created screen is displayed.

7.  Copy the Client ID and Client secret for later use.


