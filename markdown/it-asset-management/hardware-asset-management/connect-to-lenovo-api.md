---
title: Connect to the Lenovo Warranty API
description: Create a connection and credential to connect to the Lenovo Warranty API and download the warranty information for hardware assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/connect-to-lenovo-api.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Receive asset warranty details from Lenovo, Use, Hardware Asset Management, IT Asset Management]
---

# Connect to the Lenovo Warranty API

Create a connection and credential to connect to the Lenovo Warranty API and download the warranty information for hardware assets.

## Before you begin

You should have the Client ID provided by Lenovo. If you don’t have one, contact your organization's Lenovo sales or service representative.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select **Lenovo**.

3.  From the **Related Links**, select **Create New Connection and Credential**.

4.  Change the default connection name for the connection to the Lenovo Warranty API In the **Connection Name** field.

    By default, this field is set to **Lenovo Connection**.

    **Important:** Don’t change the default URL specified in the Connection URL field.

5.  In the **Client ID** field, enter the Client ID provided by Lenovo.

6.  Select **Create**.


## Result

The Lenovo connection is successfully created and listed in the Connections tab.

## What to do next

After you save the connection and credential records, the Lenovo Warranty API is ready to use. For information about the process for downloading warranty information for hardware assets, see [Integration with Lenovo for asset warranty details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/integration-with-lenovo-asset-warranty.md).

**Tip:** No connection test is available for the Lenovo Warranty API. To confirm that the connection is working, check the **Asset Job Log** \[asset\_job\_log\] table after the warranty download job runs. If the credentials are incorrect or the connection fails, the job runs but doesn't download warranty information, and logs the details for each run.

**Parent Topic:**[Receive asset warranty details from Lenovo](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/receive-warranty-details-lenovo.md)

**Related topics**  


[Track the warranty details of your Lenovo assets]()

