---
title: Subscribe to request for entry updates
description: Send the result of each Employee Health Screening entry request to a third-party system by configuring a webhook.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating with Safe Workplace suite, Safe Workplace, Health and Safety, Employee Service Management]
---

# Subscribe to request for entry updates

Send the result of each Employee Health Screening entry request to a third-party system by configuring a webhook.

## Before you begin

Sending outbound webhook calls requires the following plugins.

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   Workflow Studio Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

These plugins must be requested through the Now Support Service Catalog. For instructions, see [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

When you set up the webhook, the system automatically sends a REST request to a third-party endpoint every time an employee or visitor requests entry. Work with an administrator for the third-party system to determine the correct endpoint to provide.

**Note:** The webhook does not include authentication headers in the request. Ensure that you provide an endpoint that includes query parameters to authenticate the request.

To learn more about the Employee Health Screening Request Entry module, see [Conduct a health screen for entry](../../employee-health-screening/task/screen-returning-employee.md).

Role required: sn\_imt\_core.admin or admin

## Procedure

1.  Navigate to **All** &gt; **Employee Health and Safety Status** &gt; **Outbound Webhooks**.

2.  In the Webhook \[sn\_imt\_core\_webhook\] table, click **New**.

3.  On the form, fill in the fields.

<table id="table_x1v_zf2_hmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Internal identifier for the third-party endpoint.

</td></tr><tr><td>

Event

</td><td>

Event that you want to subscribe to. Options include:-   **Employee requested entry**: Sends an update every time an employee requests entry.
-   **Visitor requested entry**: Sends an update every time a visitor requests entry.


</td></tr><tr><td>

Endpoint

</td><td>

Endpoint to send the Employee Health Screening Request Entry data to.**Note:** The webhook does not include authentication headers in the request. Ensure that you provide an endpoint that includes query parameters to authenticate the request.

</td></tr><tr><td>

Secure parameters

</td><td>

Query parameters for the endpoint that must be handled securely, such as an authorization token. Provide parameters in the format `?param1=value&param2=othervalue`.**Tip:** If the third-party system that you're sending data to doesn't provide a securely generated authorization token, you can generate a token in your ServiceNow instance with the following script.

```
var secureRandom = GlideSecureRandomUtil;
var secret = secureRandom.getSecureRandomString(30);
gs.log(secret);
```

</td></tr><tr><td>

Active

</td><td>

Option to set the record to active.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The Employee Health Screening application sends request entry data to the third-party endpoint every time an employee requests entry. The JSON payload contains the following data.

```
{
  "event": "entry.requested",
  "email": "aileen.mottern@example.com",
  "username": "aileen.mottern",
  "user_id": "a8f98bb0eb32010045e1a5115206fe3a",
  "location": "San Antonio",
  "location_id": "108486c7c611227500b093211aa88dcc",
  "access_granted": false,
  "updated": "2020-07-01 22:19:03"
}
```

<table id="table_tmh_dl2_hmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event

</td><td>

Type of event defined in the Webhook table. Data type: String

</td></tr><tr><td>

email

</td><td>

Email address of the employee.Data type: String

</td></tr><tr><td>

username

</td><td>

Username of the employee from the Health and Safety Users \[sn\_imt\_core\_health\_and\_safety\_user\] table.Data type: String

</td></tr><tr><td>

user\_id

</td><td>

Sys\_id of the user record from the Health and Safety Users \[sn\_imt\_core\_health\_and\_safety\_user\] table. Data type: String

</td></tr><tr><td>

location

</td><td>

Location of the health screening. Data type: String

</td></tr><tr><td>

location\_id

</td><td>

Sys\_id of the location record from the Location \[cmn\_location\] table.Data type: String

</td></tr><tr><td>

access\_granted

</td><td>

Flag that indicates whether the employee was granted access as a result of the health screening. Valid values:-   **true**: The employee passed the health screening and was granted access.
-   **false**: The employee did not pass the health screening and was not granted access.

 Data type: Boolean

</td></tr><tr><td>

updated

</td><td>

Date and time when the employee or visitor requested entry.Data type: Date/Time

</td></tr></tbody>
</table>