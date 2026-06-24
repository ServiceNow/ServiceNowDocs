---
title: Configure elastic event pull connectors for MPN
description: Configure a mobile private network \(MPN\) pull connector instance to collect metrics from specified KPI domains in Elastic data store and publish them for assurance monitoring and analytics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure elastic event pull connectors for MPN

Configure a mobile private network \(MPN\) pull connector instance to collect metrics from specified KPI domains in Elastic data store and publish them for assurance monitoring and analytics.

## Before you begin

The MID Server MID Server must have Access Control \(ACL\) records for each of the following tables:

-   `sn_tsom_em_conns_kpi_definitions` \(KPI definitions table\)
-   `cmdb_ci_network_service_instance`
-   `cmdb_ci_app`

For more information, see [Set up a MID Server role](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t_SetupMIDServerRole.html).

Roles required: tsom\_assurance\_admin and assigned roles for MID Server.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Select **Nokia MPN Pull Connector**.

3.  Open an existing connector instance or create one:

    -   To use an existing instance, select it from the **Connector Instances** list and edit only the fields you need to change.
    -   To create an instance, select **New** and complete all required fields as described in the following steps.
4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Host IP|URL of the MPN host|
    |Credential|Username and password for basic authentication|
    |kpi\_domain identifier|Domains to collect metrics from. Leaving the field empty collects metrics from all domains. Entering one or more domain identifiers, with values separated by commas \(for example, `RAN, Core`\) collect metrics only from specific domains.|
    |Metrics collection schedule|How long, in seconds, each metrics collection should run.|

5.  Add a MID Server.

    1.  In the **MID Servers for Connectors** section, select the plus icon next to **Insert a new row**.

    2.  In the **MID Server** field, enter the name of the MID Server.

    3.  Save your selection by selecting the green check mark.

6.  Enable the connector instance by selecting the **Active** check box.

    The connector begins collecting metrics from Elastic data store.

7.  Select **Update**.


**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[View metric to CI and resource binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/view-metric-to-CI-binding.md)

[Event field mapping configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_EMEventFieldMapping.md)

[Create an event rule to bind metric events to host CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-rule-bind-metrics-to-host.md)

[View metric values in the Insights Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/view-metrics-explorer.md)

[Create an Insights Explorer view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-metric-explorer-view.md)

