---
title: Set up push notifications from Dynatrace
description: Set up push notifications of events from Dynatrace into a ServiceNow instance that has the Service Graph Connector for Observability - Dynatrace installed.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set up push notifications from Dynatrace

Set up push notifications of events from Dynatrace into a ServiceNow instance that has the Service Graph Connector for Observability - Dynatrace installed.

## Before you begin

If you don't have an alerting profile in Dynatrace, then complete the following steps to create one:

1.  Navigate to **Settings** &gt; **Alerting** &gt; **Alerting Profiles**.
2.  Set up an alerting profile according to your business needs.

    **Note:** For more information about how to set up an alerting profile, see [Alerting profiles](https://www.dynatrace.com/support/help/how-to-use-dynatrace/problem-detection-and-analysis/notifications-and-alerting/alerting-profiles/) on the Dynatrace documentation site.


You must have Observability Commons for CMDB installed.

Role required: admin

## Procedure

1.  In the Dynatrace instance, navigate to **Settings** &gt; **Integration** &gt; **Problem notifications**.

2.  Click **Add Notification**.

3.  On the form, fill in the fields.

<table id="table_xxf_tjs_sqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Notification Type

</td><td>

Custom Integration

</td></tr><tr><td>

Display Name

</td><td>

Name of the notification

</td></tr><tr><td>

Webhook URL

</td><td>

Use the following URL: `https://<name_of_your_servicenow_instance_name> /api/sn_em_connector/em/inbound_event?source=SGO-Dynatrace`

</td></tr><tr><td>

Additional HTTP Headers &gt; Create basic authorization

</td><td>

1.  In the ServiceNow instance, set a password for the pre-created Dynatrace API user by doing the following:
    1.  Navigate to **System Security** &gt; **Users**.
    2.  Select the Dynatrace API user.
    3.  Set the **Password** field with a new password.
    4.  Clear the **Password needs reset** check box.
    5.  Update or save the user.
2.  Set the **Username** field to `DynatraceAPI`.
3.  Set the **Password** field to the password that you had created.
4.  Click **Add**.


</td></tr><tr><td>

Custom Payload

</td><td>

Use the following payload: ```
{ 
  "connectionId": <connections_alias_sys_id>,
  "ImpactedEntities": {ImpactedEntities}, 
  "ImpactedEntity": "{ImpactedEntity}", 
  "PID": "{PID}", 
  "ProblemDetailsHTML": "{ProblemDetailsHTML}", 
  "ProblemDetailsJSONv2": {ProblemDetailsJSONv2},  
  "ProblemDetailsMarkdown": "{ProblemDetailsMarkdown}", 
  "ProblemDetailsText": "{ProblemDetailsText}", 
  "ProblemID": "{ProblemID}", 
  "ProblemImpact": "{ProblemImpact}", 
  "ProblemSeverity": "{ProblemSeverity}", 
  "ProblemTitle": "{ProblemTitle}", 
  "ProblemURL": "{ProblemURL}", 
  "State": "{State}", 
  "Tags": "{Tags}" 
}
```

**Note:** For the &lt;connections\_alias\_sys\_id&gt;:

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
2.  Select to open the connector for which you want to get the &lt;connections\_alias\_sys\_id&gt;.

![Dynatrace connection aliases list.](../image/dynatrace-connection-aliases.png)

3.  Right-click the context menu \(![menu icon](../../../common/image/Form_MenuIcon.png)\) and then select **Copy sys\_id**.

![sys_id of the connection.](../image/dynatrace-static-sys-id.png)

</td></tr><tr><td>

Alerting Profile

</td><td>

Select the alerting profile created in the Before you begin section or another alerting profile.

</td></tr><tr><td>

Sending Test Notifications

</td><td>

Click to send a test notification, and verify that the response status is 200.

</td></tr></tbody>
</table>
