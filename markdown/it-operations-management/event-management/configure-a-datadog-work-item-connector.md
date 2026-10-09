---
title: Configure a Datadog work item connector instance
description: Configure a Datadog work item to aggregate related alerts and signals from Datadog into a trackable operational problem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/configure-a-datadog-work-item-connector.html
release: brazil
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure a Datadog work item connector instance

Configure a Datadog work item to aggregate related alerts and signals from Datadog into a trackable operational problem.

## Before you begin

-   Verify you already have a Datadog account with API access and Case Management in use.
-   Role required: evt\_mgmt\_operator

## About this task

ServiceNow represents a work item as an alert. Each related alert is retained individually, enabling grouping and correlation across multiple resources and monitoring systems. Alerts aren't limited to those Datadog grouped. As a result, ServiceNow identifies broader incidents, reduces duplicate alerts, and provides a more comprehensive operational view.

Note the following before you start:

-   If you already use the Datadog push connector, use the same push connector URL to send work items. Configure the Datadog Case Management notification rule and the case payload template described on the push connector page.
-   The push connector receives the work item and creates the work item alert and its tracking records. The pull connector then fetches the correct work item title, retrieves related alerts, and drives bi-directional close-back.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Push Connectors**.

    **Note:** Create this push connector to auto-create the pull connector with the matching name. The connector names must match for bi-directional and fetch related alerts.

2.  Select a **Datadog Push Connector** instance used to send work items.

3.  Select the **Configure Work Item Alerts** button.

    You're redirected to the pull connector instance form.

4.  Fill in the fields.

<table><thead><tr><th align="left" id="d658136e159">

Field

</th><th align="left" id="d658136e162">

Description

</th></tr></thead><tbody><tr><td id="d658136e168">

**Name**

</td><td>

Name of the connector. The pull connector instance name must match the push connector instance name.

</td></tr><tr><td id="d658136e177">

**Description**

</td><td>

Any optional information that you want to use to identify this record.

</td></tr><tr><td id="d658136e186">

**Host IP**

</td><td>

Use your Datadog site's API host. For example, `api.datadoghq.eu`

</td></tr><tr><td id="d658136e200">

**Credential**

</td><td>

The ServiceNow credential record that stores your Datadog API key or access token. The authentication method is controlled by the `useAccessToken` connector instance value. For more information, see the Connector instance value parameters table.

</td></tr><tr><td id="d658136e219">

**Active**

</td><td>

This option appears only after the form is saved.

</td></tr><tr><td id="d658136e228">

**Bi-directional**

</td><td>

Select to enable bi-directional exchange of values to and from the external event source. This option is available only when the connector definition has bi-directional values configured. After a work item alert is closed in ServiceNow, the corresponding case is automatically closed in Datadog.

</td></tr><tr><td id="d658136e246">

**Last bi-directional status**

</td><td>

The value of this field is automatically populated. This option appears only when the **Bi-directional** option is selected.The status values are:

 -   None - A valid connection has not yet been established.
-   Success - A successful connection was established.
-   Error - A connection was established. However the external event source was not updated.


</td></tr></tbody>
</table>    Connector instance value parameters:

    |Parameter|Description|
    |---------|-----------|
    |**useAccessToken**|Controls the authentication method. By default, this value is false. The **Credential** option must store the Datadog API key and you must set **application\_key**. The connector sends the `DD-API-KEY` and `DD-APPLICATION-KEY` headers. When this value is true, the **Credential** option must store the Datadog OAuth access token. The connector sends `Authorization: Bearer <token> header (application_key is not used)`.|
    |**application\_key**|The application key of the Datadog connector. By default, this value is empty which indicates Basic authentication.|
    |**fetchCaseRelatedAlerts**|Controls whether related alerts are fetched for the work item. The default is true. Set it to false to disable.|
    |**caseApiPath**|Set as `/api/v2/cases/`.|
    |**eventApiPath**|Set as `/api/v2/events/`.|

5.  Right-select the form header and select **Save**.

6.  Select **Test connector** to verify the connection.

7.  After a successful test, select the **Active** check box and then select **Update**.


**Parent Topic:**[Configure a pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a push connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/push-event-listener.md)

