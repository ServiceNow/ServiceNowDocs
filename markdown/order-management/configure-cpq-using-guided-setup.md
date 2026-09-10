---
title: Set up CPQ Configurator using guided setup
description: The guided setup organizes the configuration activities into modules and tracks completion as each activity is completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/configure-cpq-using-guided-setup.html
release: zurich
topic_type: task
last_updated: "2026-05-31"
reading_time_minutes: 1
breadcrumb: [With guided setup, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up CPQ Configurator using guided setup

The guided setup organizes the configuration activities into modules and tracks completion as each activity is completed.

## Before you begin

Role required: admin

Complete the prerequisites for the ServiceNow CPQ Integration. For more information, see [Prerequisites for configuring CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/guided-setup-prereq.md).

## Procedure

1.  Navigate to the guided setup using either of the following ways.

    -   For either a new configuration or to reconfigure navigate to **All** &gt; **CPQ Integration** &gt; **Start guided setup**.

        **Important:** If you have already set up the Configurator using the guided setup and want to reconfigure, access the guided setup only through the navigation **All** &gt; **CPQ Integration** &gt; **Start guided setup**.

    -   To configure for the first time, you can alternatively navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** &gt; **CPQ Integration** &gt; **Get started** &gt; **Configure**.
2.  Select the **Prerequisites** module and ensure the tasks are completed.

3.  Complete the **Certificate setup** module.

4.  Complete the ServiceNow CPQ **Connection Setup** module.

    1.  Enter the ServiceNow CPQ tenant URL that was shared with you when your ServiceNow CPQ instance was provisioned.

    2.  Generate Admin API key in CPQ Administrator, and add the key in the guided setup; the system updates the HTTPS connection record automatically.

        Consider the following points while generating the Admin API key.

        -   Enter the same value for both Name and User ID fields.
        -   Select **Admin** for the **Permissions** field.
    **Warning:** The admin API key generated in the tenant displays only once. Copy the key immediately. The key can't be retrieved later.

5.  In the **Setup Confirmation** section execute the steps.

6.  Select **Confirm end-to-end flow works** check-box after you have verified that the Configurator works as expected.

    **Important:** If the Configurator is not working as expected during workflow verification, don't select the **Confirm end-to-end flow works** check-box. Contact your administrator for assistance.


