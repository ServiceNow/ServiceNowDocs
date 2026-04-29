---
title: Configure a webhook event
description: Configure a webhook API event in the Provider configuration table to enable badging vendors to share the badging data collected from badging tables using the webhook event.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Provider connector configuration, Setup Workplace Connectors for badging data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure a webhook event

Configure a webhook API event in the Provider configuration table to enable badging vendors to share the badging data collected from badging tables using the webhook event.

## Before you begin

Role required: sn\_wsd\_wc.admin

## About this task

The badging data \(JSON\) is processed using the ServiceNow Rest API explorer. Single or multiple raw badging data records \(payload\) can be shared and processed using the REST API explorer. The webhook event for badging data is loaded to the Connector Events table in single or multiple JSON records. Multiple records are sent as an array. For more information, see [Attendance Analytics](attendance-analytics.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Provider Connector Configurations**.

2.  Select **Create New**.

    On the form, fill in the fields.

<table id="table_vct_344_vyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the provider configuration.

</td></tr><tr><td>

Source Type

</td><td>

Source from where the badging data is collected and loaded into the target Employee attendance table. Select **Webhook** to configure the webhook event.

</td></tr><tr><td>

Token Param Name

</td><td>

The **Token Param Name** and **Token value** is a secret key-value pair, which is used to authenticate the API call from the vendor badging system to the Workplace Connectors application. Both systems have the token name value. Using the token name, the application authenticates the API request.

</td></tr><tr><td>

Token value

</td><td>

The token value is the secret key used by the badging vendor while calling the API event to let the server authenticate the API request.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the provider configuration is Active.

</td></tr><tr><td>

Connector Configuration

</td><td>

Option to search for and select the lookup list icon \(![Lookup list icon.](../../workplace-lease-administration/images/look-up-icon.png)\) to select **Badging**. For more information, see [Configure connectors for badging data](workplace-connector-configuration.md).

</td></tr><tr><td>

Callback URL

</td><td>

Option to select the callback URL icon \(![Callback URL icon.](../images/wsd-callback-url-icon.png)\) to lock or edit the callback URL.

</td></tr></tbody>
</table>3.  Select **Update**.

4.  Select the newly created webhook event.

    The Generate Callback URL button is available to generate a callback URL for the REST API request.

5.  As a badging vendor, share the badging data in JSON format by navigating to **All** &gt; **System Web Services** &gt; **REST** &gt; **Rest API Explorer**.

6.  In the Rest API Explorer page, select the following:

    -   Namespace: From the drop-down list, select **sn\_wsd\_wc**
    -   API Name: Workplace Connector Webhook
    -   API Version: v1
7.  On the Workplace Connector Webhook event page, provide the following values:

    -   token\_name: Token param name used in step 2. The token name value is used by badging vendors to share the badging data \(JSON\) with Workplace Connectors. The raw data \(payload or badging data\) is processed and loaded into the Connector Events table.
    -   ni.nolog.id: Copy the System ID of the webhook created in step 2 and paste it. Select the additional actions menu icon \(![Additional actions menu icon.](../../human-resources/image/additional-actions-icon.png)\) from the pane.
    -   token\_value: Token value provided in step 2. The token value is the secret key used by the badging vendor while calling the API event to let the server authenticate the API request.
    1.  In the API Request body, select **Raw** and copy the badging data \(payload\) in JSON format.

        This badging data is collected from badging sensors.

    2.  Select **Send**.

        If the Response code is **200 OK** and the response result is **Success**, the badging data is loaded into the Connector Events table.

        -   The Connector Events table \(sn\_wsd\_wc\_connector\_events\) loads the badging data shared by badging vendors. The State of the badging data is **New** when it’s loaded by the REST API Explorer.
        -   The scheduled Job **Process webhook provider data records** runs every minute to load the badging data from the Connector Events table \(data with the State **New**\) to the Employee Attendance Data table.
    The scheduled job takes the source data from the **Webhook** event to transform the data in the required format and then place it in the target Employee Attendance Data table.

    **Note:** To access the Workplace Connectors scheduled jobs, navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**. Search for **Workplace connectors** in the Application column. Two scheduled jobs are available for Workplace Connectors.

    -   **Process provider data records**: Reads data from vendor badging data \(source table\). After processing the badging data, the record loads it into the Employee Attendance Data table \(target table\). For more information, see [Configure badging table data](provider-configuration-wsd-connectors.md).
    -   **Process webhook provider data records**: Reads data from the Connector Events table. Processes the webhook event data and loads it into the Employee Attendance Data table \(target table\).
    -   Data is loaded to the Employee Attendance Data table. The state of the badging data in the Connector Events table changes to **Processed**.
    -   From the Employee Attendance Data table, the data is loaded into the Attendance Analytics table.

        **Note:** Badging data records in the Connector Events table with the state of Processed are purged after two days from the date of creation or the current date by the Connector Events table \[sn\_wsd\_wc\_connector\_events\]. Data in the Error state is purged after seven days from the date of creation. Data in the New state isn’t purged.


**Parent Topic:**[Provider connector configuration](../concept/provider-configuration-ovw.md)

**Previous topic:**[Configure badging table data](provider-configuration-wsd-connectors.md)

**Next topic:**[Employee attendance data](employee-attendance.md)

