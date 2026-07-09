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

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** and open the ServiceNow CPQ Integration application record.

2.  In the **Get started** section, select **Configure** to open the guided setup.

3.  Complete the **Prerequisites** module.

    Confirm that the required plugins are active, that the DevOps request for the ServiceNow CPQ instance is complete, and that the tenant URL is available. Submit the prerequisites confirmation questionnaire to mark the module complete.

4.  Complete the ServiceNow CPQ Connection Setup module.

    Enter the tenant URL and sector value, generate an admin API \(application programming interface\) key in the tenant, and paste the key into the guided setup. The system updates the HTTPS connection record automatically.

    **Warning:** The admin API key generated in the tenant displays only once. Copy the key immediately. The key can't be retrieved later.

5.  Select **Close** to exit the guided setup.


