---
title: Set up the FRISS spoke
description: You can integrate a ServiceNow instance and FRISS account by using the API key and Tenant ID to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FRISS Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the FRISS spoke

You can integrate a ServiceNow instance and FRISS account by using the API key and Tenant ID to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the FRISS spoke.
-   Contact the FRISS support team and obtain the connection URL to connect to your FRISS account.
-   Role required: admin.

## Procedure

1.  Create a credential record for the FRISS spoke in your ServiceNow instance:

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

        The system displays the message **What type of Credentials would you like to create?**

    3.  Select **API Key Credentials**.

        An empty API Key Credentials form is displayed.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record. For example, enter `FRISS Spoke Credential`.|
        |Active|Option to actively use the credential record.|
        |API Key|FRISS token in this format: `<Value of ID+key>`.|
        |Applies to|Option that is not applicable to this spoke.|
        |Order|Order to apply this credential. For example, enter `100`.|

    5.  Select **Submit**.

2.  Create a connection record for the FRISS spoke in your ServiceNow instance:

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the FRISS record.

    3.  From the **Connections** tab, select **New**.

        The system displays an empty HTTP\(s\) Connection form.

    4.  On the form, fill in these fields.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the connection record. For example, enter `FRISS`.

</td></tr><tr><td>

Credential

</td><td>

Credential record that you created for FRISS. For example, select **FRISS Spoke Credential**.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL to connect to FRISS account.

</td></tr><tr><td>

Attributes

</td><td>

Subsequent calls that you can authorize to the FRISS API. To authorize calls, use the following two parameters:-   **tenant\_id**: An identifier of the tenant, as defined in the FRISS Identity. This identifier is provided to you by FRISS.
-   **api\_version**: The API version key that was retrieved from the FRISS Identity by the earlier request.

**Note:** This API version key is short-lived, so each time it expires, you must generate a new one.

</td></tr></tbody>
</table>    5.  Select **Submit**.


