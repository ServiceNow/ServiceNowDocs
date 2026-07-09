---
title: Set up ServiceNow CPQ Configurator using guided setup
description: The guided setup organizes the configuration activities into modules and tracks completion as each activity is completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-cpq-using-guided-setup.html
release: australia
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 1
breadcrumb: [With guided setup, ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow CPQ Configurator using guided setup

The guided setup organizes the configuration activities into modules and tracks completion as each activity is completed.

## Before you begin

Role required: admin

Complete the prerequisites. For more information, see [Prerequisites for configuring ServiceNow CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/prereq-for-cpq-config.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** and open the CPQ Integration application record.

2.  In the **Get started** section, select **Configure** to open the guided setup.

3.  Complete the **Prerequisites** module.

    Confirm that the required plugins are, the request for a new ServiceNow CPQ tenant is complete, and ServiceNow CPQ tenant URL is available. Submit the prerequisites confirmation questionnaire to mark the module complete.

    **Note:**

    Certificate setup is not required and OAuth is configured automatically. Proceed with ServiceNow CPQ Connection Setup module.

4.  Complete the ServiceNow CPQ Connection Setup module.

    Enter tenant URL and sector value, generate an admin API \(application programming interface\) key in the tenant, and add the key in the guided setup. The system updates the HTTPS connection record automatically.

    **Warning:** The admin API key generated in the tenant displays only once. Copy the key immediately. The key can't be retrieved later.

5.  Select **Close** to exit the guided setup.


**Related topics**  


[Using the ServiceNow CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-servicenowcpq.md)

