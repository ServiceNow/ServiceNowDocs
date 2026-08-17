---
title: Migrate a classic Dynatrace connection to the Dynatrace SaaS connector
description: Copy the sys\_id of your classic Dynatrace connection alias into a property in your Dynatrace SaaS connection to enable the cleanup of stale Process CIs from the classic connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-migration-task.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
breadcrumb: [Observability - Dynatrace SaaS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Migrate a classic Dynatrace connection to the Dynatrace SaaS connector

Copy the sys\_id of your classic Dynatrace connection alias into a property in your Dynatrace SaaS connection to enable the cleanup of stale Process CIs from the classic connector.

## Before you begin

Role required: admin

## About this task

For additional information about migrating to the Service Graph Connector for Dynatrace SaaS, see the [New Service Graph Connector for Observability – Dynatrace SaaS](https://www.servicenow.com/community/service-graph-connectors/new-service-graph-connector-for-observability-dynatrace-saas/ta-p/3572958) article on the ServiceNow Community site.

## Procedure

1.  Copy the sys\_id of your classic Dynatrace connection alias.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Dynatrace Observability** &gt; **Connections**.

    2.  Select the active connection record.

    3.  On the form, locate the Connection Alias field.

    4.  Open the record, select and hold \(or right-click\) the header, and then select **Copy sys\_id**.

        Save the sys\_id value for use in step [2.d](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-migration-task.md).

2.  Add the sys\_id of the classic Dynatrace connection alias to the Dynatrace SaaS connection.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Dynatrace SaaS** &gt; **Connections**.

    2.  Open the Dynatrace SaaS connection record that corresponds to the classic Dynatrace connection record.

    3.  From the Service Graph Connection Properties related list, select the **dynatrace\_classic\_connection\_alias\_sys\_id** connection property.

    4.  Enter the sys\_id that you copied in step [1.d](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-migration-task.md) into the **Value** field.

    5.  Save the record.

        **Note:** If no value is specified in the **Value** field of the dynatrace\_classic\_connection\_alias\_sys\_id connection property, stale Process CIs from the classic connector aren't cleaned up.


## Result

The SGO-Dynatrace Classic Migration Cleanup scheduled import job of the Service Graph Connector for Dynatrace SaaS runs with the next scheduled execution. Using the sys\_id of the classic Dynatrace connection alias, the Process CIs that are exclusively owned by the classic connector are identified and soft-retired automatically \(operational\_status is set to 2 or Non-Operational\).

The SGO-Dynatrace Classic Migration Cleanup scheduled import runs only once. This scheduled import is automatically deactivated after the first successful run.

