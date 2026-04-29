---
title: Create a Google BigQuery connection
description: Establish a zero copy connection to the Google BigQuery data warehouse service in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Google BigQuery, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Google BigQuery connection

Establish a zero copy connection to the Google BigQuery data warehouse service in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Google BigQuery. For additional information about connecting to Google BigQuery, refer to the [Google BigQuery documentation](https://cloud.google.com/iam/docs/service-account-creds).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Google BigQuery connector and select **Connect**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|

4.  Enter the full Google Cloud service account JSON key used for authentication.

    You can obtain the JSON key from the Google Cloud Console when you create a service account.

<table id="choicetable_nbh_ccm_rfc"><thead><tr><th align="left" id="d452295e198">

Option

</th><th align="left" id="d452295e201">

Description

</th></tr></thead><tbody><tr><td id="d452295e207">

**Upload service account key**

</td><td>

1.  Select **Attach Service Account Key \(JSON\)**.
2.  Browse and select the file.


</td></tr><tr><td id="d452295e228">

**Enter service key contents manually**

</td><td>

Copy and paste the contents of the file, ensuring the content begins with `{` and contains fields like `"type"`,`"project_id"`, and `"private_key"`, and ends with `}`.For example:

 ```
{
"type": "service_account",
"project_id": "your-project-id",
...
"private_key": "-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n",
...
}
```

</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

