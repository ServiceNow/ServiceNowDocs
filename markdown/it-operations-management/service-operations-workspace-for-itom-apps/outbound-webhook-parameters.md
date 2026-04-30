---
title: Outbound webhook parameters
description: The parameters to be configured when sending data to other systems using an outbound webhook.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Outbound webhook parameters

The parameters to be configured when sending data to other systems using an outbound webhook.

<table id="table_rc3_swn_4bc"><thead><tr><th>

Parameter

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Destination URL field

</td><td>

The webhook endpoint \(URL\) where the alert is to be sent.

</td></tr><tr><td>

JSON payload data tab

</td><td>

The alert data, composed in JSON format, being sent to the indicated URL.Enter the details you want to be notified about in the JSON object when the automation is triggered. You can insert alert fields by selecting **Insert Field Values** or add custom fields by typing \{custom\_field.JSON\_path\}.

To add additional alert fields, select **Insert alert fields**.

</td></tr><tr><td>

Payload headers

</td><td>

Add predefined or custom metadata headers in the **Key** and **Value** fields. A key is the name of a header field, and a value is the corresponding data assigned to that header field.

</td></tr><tr><td>

Test payload

</td><td>

Select to verify that the webhook is functioning correctly and that the receiving system can process the data as expected.

</td></tr></tbody>
</table>To return to the procedure, see [Create Respond automation](../task/esc-notify-alert-sow-itom.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

