---
title: Configure elastic connectors for MPN alarm collection
description: Configure a connector instance to collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-nokia-mpn.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 3
keywords: [Nokia MPN, connector instance, Elastic, fault management, alarm collection]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure elastic connectors for MPN alarm collection

Configure a connector instance to collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management.

## Before you begin

1.  [Create Basic Auth Credentials](https://www.servicenow.com/docs/r/it-operations-management/event-management/create-credentials-basic-auth.html)
2.  [Create HTTP\(S\) Connection](https://www.servicenow.com/docs/r/platform-security/connections-and-credentials/create-https-connection.html)
3.  [Activate the Telecommunications Alarm Management Open API endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/activate-endpoint-in-the-telecommunications-alarm-management-open-api.md)

Role required: tsom\_assurance\_admin

## About this task

The MPN connector collects alarm and event data from managed network infrastructure by querying Elastic fault management indices at a configured polling interval. Each connector instance collects from one or more of these indices, each corresponding to a specific network domain. The MPN pull connector definition supports three connector instances: one for alarm collection and two for metrics collection. This procedure covers configuring the alarm collection instance.

You can create multiple connector instances, one per index, and assign each to a dedicated MID Server to distribute the polling workload across your deployment. A default index value is provided for each connector instance.

The alarm collection instance also clears stale alarms: alarms that were cleared at the source but were missed during a normal collection cycle and would otherwise remain open in Event Management. At a regular interval, the connector rechecks the source for active alarms that have not been updated within a set time window and clears any that are no longer active. Default values are provided, so no action is required unless you want to tune this behavior.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Select **Nokia MPN Pull Connector**.

3.  In the **Default schedule** field, enter the polling time \(in seconds\) to be used for all connector instances.

    The default value is 120 seconds.

4.  In the Connector Instances related list, select **Nokia MPN Alarms**.

5.  On the Connector Instances page, in the **Event collection schedule** field, enter how long each event collection should run, in seconds.

    This value overrides the default schedule set on the connector definition. The MPN Alarms instance defaults to 60 seconds.

6.  In the **Index** field, provide the index connector instance values.

    Enter the index pattern for the network domain this connector instance collects from. To collect from more than one domain, enter the patterns as a comma-separated list. The following table lists the standard index patterns:

    \[Omitted image "index-connector-instance-values.png"\] Alt text: Index connector instance values configuration screen.

    |Description|Name|
    |-----------|----|
    |Radio network elements|radio-fm\*|
    |Core network elements|core-fm\*|
    |Application-layer network elements|application-fm\*|
    |IXR \(Interconnect Router\) devices|ixr-fm\*|
    |DAC \(Digital Access Controller\) devices|dac-fm\*|

7.  Add the MID Server.

    1.  In the **MID Servers for Connectors** section, select the plus icon next to **Insert a new row**.

    2.  Enter the name of the MID Server in the **MID Server** field.

    3.  Select the green check mark to save your selection.

8.  Enable the connector instance by selecting the **Active** check box.

9.  Tune how stale alarms are detected and cleared.

    Set the following connector instance values on the alarm collection instance. If you don't set them, the default values apply.

    |Parameter|Default|Description|
    |---------|-------|-----------|
    |`stale_threshold_minutes`|60|How long, in minutes, an active alarm can go without an update at the source before the connector treats it as stale and clears it in Event Management.|
    |`stale_check_interval_minutes`|30|How often, in minutes, the connector runs the stale alarm check. This check runs independently of the event collection schedule.|

10. Select **Update**.

11. View your configured alarms by navigating to **em\_event.LIST** and searching for `API Alarm Notification`.


**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

