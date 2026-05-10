---
title: Create HTTP response headers for Engagement Messenger
description: Configure a name-value pair for HTTP response headers for the Engagement Messenger module. The ability to configure and pass response headers enables special handling of the page content by a client, which is most typically a browser.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Engagement Messenger, Set up self-service, Configure, Customer Service Management]
---

# Create HTTP response headers for Engagement Messenger

Configure a name-value pair for HTTP response headers for the Engagement Messenger module. The ability to configure and pass response headers enables special handling of the page content by a client, which is most typically a browser.

## Before you begin

-   [Configure Engagement Messenger](create-engagement-messenger-module.md).
-   [Create an identity provider \(IdP\) for Engagement Messenger](../concept/create-identity-providers-for-engagement-messenger.md).
-   [Configure a CORS rule for Engagement Messenger](create-cors-for-rest-api-ec.md).
-   Role required: admin

## About this task

Use the Engagement Messenger API and your website URL to create a CORS rule.

## Procedure

1.  In the navigation pane, enter `sys_response_header.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_vyw_3js_f4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option for indicating that this HTTP response header configuration is active.

</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Applies to

</td><td>

Type of record that the HTTP response header configuration applies to.

 Select **Specific Type** to indicate that this HTTP response header configuration is for the specific type and record that you select in the **Type** and **Record** fields.

</td></tr><tr><td>

Type

</td><td>

Type of record that the HTTP response header configuration applies to.

 Select **Service Portal** to indicate that the records are related to the Service Portal.

</td></tr><tr><td>

Record

</td><td>

Engagement Messenger module record that the HTTP response header configuration applies to.

 Select a record:

1.  Select the Search \(![Search icon.](../../../common/image/List_SearchIcon.png)\) icon to access the Select the document pop-up form.
2.  In the **Table name** field, ensure that the value is set to **Service Portal**.
3.  In the **Document** field, select the Search \(![Search icon.](../../../common/image/List_SearchIcon.png)\) icon.
4.  From the list of Service Portal records, select the messenger module that you configured.
5.  Select **OK**.


</td></tr><tr><td>

Name

</td><td>

Name for the name-value pair for the HTTP response header.

 Set this field value to **Content-Security-Policy**.

</td></tr><tr><td>

Value

</td><td>

Value for the name-value pair for the HTTP response header.

 Set this field value to **frame-ancestors 'self' &lt;enter your website URL&gt;**.

 For example, **frame-ancestors 'self' https://www.example.com**.

</td></tr><tr><td>

Description

</td><td>

Detailed description for the HTTP response header.

</td></tr></tbody>
</table>
## What to do next

[Activate an Engagement Messenger module](activate-engagement-messenger-module.md)

.

**Related topics**  


[HTTP Response Headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/http-response-header.md)

