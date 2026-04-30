---
title: Create a REST message
description: Configure a REST message for all outbound calls for a particular SCIM Provider.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a REST message

Configure a REST message for all outbound calls for a particular SCIM Provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_z3g_llg_btb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this message.

</td></tr><tr><td>

Endpoint

</td><td>

Base URL of SCIM Provider. For example, `https://example.service-now.com/api/now/scim`.

</td></tr><tr><td>

Authentication Type

</td><td>

Type of authentication to be used to connect to the external SCIM Provider. For more information see, [Outbound REST authentication](https://www.servicenow.com/docs/access?context=c_OutboundRESTAuth&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

HTTP Headers

</td><td>

The content type that is expected from the external SCIM Provider.

 For example, Header Name is the content type in the following API request body: `Content-type: application/scim+json`

</td></tr></tbody>
</table>4.  In the  HTTP Methods  related list, click  **New**.

5.  Configure the following HTTP Methods.

    **Note:** The URLs have variables that you must replace.

<table id="table_j4b_knp_2tb"><thead><tr><th>

Methods

</th><th>

Sample URL

</th></tr></thead><tbody><tr><td>

GET

</td><td>

`https://example.com/api/now/scim/${resourceName}`

</td></tr><tr><td>

PATCH

</td><td>

`https://example.com/api/now/scim/${resourceName}/${resourceId}`

</td></tr><tr><td>

PUT

</td><td>

`https://example.com/api/now/scim/${resourceName}/${resourceId}`

</td></tr><tr><td>

DELETE

</td><td>

`https://example.com/api/now/scim/${resourceName}/${resourceId}`

</td></tr><tr><td>

POST

</td><td>

`https://example.com/api/now/scim/${resourceName}/${resourceId}`

</td></tr></tbody>
</table>    **Note:**

    -   You must create all the HTTP methods for the operation of the SCIM Client.
    -   A sample REST message is shipped from the base system.
    ![REST message](../images/rest-message.png)

6.  Click **Submit**.


## Result

The REST message record is created.

## What to do next

Use the REST message to create a SCIM Provider. For more information, see [Create a SCIM Provider](create-scim-provider.md).

To learn more about how to create a REST message, see [Create a REST message](https://www.servicenow.com/docs/access?context=t_ConfiguringARESTMessage&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

