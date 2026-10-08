---
title: Configure the Equinix pull connector
description: Configure a connector instance to collect power and environmental metrics from Equinix IBX data center facilities and forward alerts to Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-equinix.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Equinix, connector instance, power metrics, environmental metrics, MID Server]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure the Equinix pull connector

Configure a connector instance to collect power and environmental metrics from Equinix IBX data center facilities and forward alerts to Event Management.

## Before you begin

-   The TSOM EM Connectors plugin \(**sn\_tsom\_em\_conns**\) must be installed.
-   A credential record must exist for the Equinix OAuth2 client secret. Do not store the client secret as a connector instance parameter.

Role required: tsom\_assurance\_admin

## About this task

The Equinix connector collects power and environmental readings and system alerts from the Equinix Colo Portal Open API for each configured account. On each run, the connector authenticates with OAuth2 and retrieves the facility hierarchy for the account \(IBX, zone, cage, and cabinet\). The connector then requests power and environment readings for that hierarchy and polls for system alerts on a separate, paginated request.

You can configure multiple accounts on a single connector instance by entering a comma-separated list of account numbers.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

    **Note:** You can also discover and open this connector from Service Operations Workspace. From the navigation pane, select the AIOps Configuration Center icon, select **Add integration**, and search for **Equinix IBX SmartView** in the Integration Launchpad.

2.  Select **Equinix IBX SmartView**.

3.  Create a connector instance or select an existing instance to edit by selecting **New** or selecting an existing instance.

4.  Complete the following fields.

    |Field|Description|
    |-----|-----------|
    |**host**|Base URL of the Equinix Colo Portal Open API. Required.|
    |**client\_id**|OAuth2 client ID for your Equinix account.|
    |**accounts**|Comma-separated list of Equinix account numbers to poll. Example: `578555,548686,111850`.|
    |**auth\_url**|OAuth2 token endpoint path.|
    |**last\_event**|ISO 8601 timestamp used as the starting point for incremental alert collection. Example: `2026-06-19T00:00:00.000Z`.|
    |**debug**|Enables additional logging for troubleshooting.|

5.  Link the credential record that contains the OAuth2 client secret.

    The connector retrieves the client secret from this credential record at runtime. The connector never reads the secret from a plain connector instance parameter.

6.  Add the MID Server.

    1.  In the **MID Servers for Connectors** section, select the plus icon next to **Insert a new row**.

    2.  In the **MID Server** field, enter the name of the MID Server.

    3.  Select the green check mark to save your selection.

7.  Enable the connector instance by selecting the **Active** check box.

8.  Select **Update**.

9.  Verify the connection by running `testConnection()` on the connector instance.

    A successful test returns a structured result with individual pass or fail status for the authentication, hierarchy, and power checks.


## Result

The connector begins polling on the configured schedule. Power and environmental readings appear in MetricBase for each cabinet and zone in the account's facility hierarchy, and system alerts are forwarded to Event Management.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

