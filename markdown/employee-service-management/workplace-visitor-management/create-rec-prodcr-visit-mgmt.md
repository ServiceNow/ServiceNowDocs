---
title: Create a record producer for visitor management
description: Make visitor-related services available to employees as a self-service option. Create a record producer to display these services as catalog items in the Workplace Services catalog.
locale: en-US
release: zurich
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Create a record producer for visitor management

Make visitor-related services available to employees as a self-service option. Create a record producer to display these services as catalog items in the Workplace Services catalog.

## Before you begin

Role required: sn\_wsd\_visitor.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Visitor Management** &gt; **Administration** &gt; **Record producers**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_xrk_mql_dnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record producer.

</td></tr><tr><td>

Table name

</td><td>

Visitor Registration \(sn\_wsd\_visitor\_visitor\_registration\) table that the record producer is associated with. **Note:** Make sure that the Visitor Registration table for the record producer matches that of the associated workplace service.

</td></tr><tr><td>

Model

</td><td>

Product model table if relevant for the record producer.

</td></tr><tr><td>

Application

</td><td>

This field is set to `Workplace Visitor Management`.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record producer for use.

</td></tr><tr><td>

Expand help for all questions

</td><td>

Select this option to enable users to expand help for all questions.

</td></tr></tbody>
</table>4.  Fill the following tab fields appropriately:

    -   **What it will contain**
    -   **Accessibility**
    -   **Generated Record Data**
    -   **Portal Settings**
5.  In the **What it will contain** tab, provide the following script:

    ```
    var visitorService = new sn_wsd_visitor.WSDVMVisitorService();
    visitorService.createVisitorRegistrationRecord(producer, current.sys_id);
    
    producer.portal_redirect = "?id=my_requests";
    ```

6.  In the **Variables** tab, configure the variables for the Workplace Services catalog item as appropriate.

    Variables collect information from the user, and are used to ask questions and map answers to fields.

    To learn more about the different types of variables and how to configure them, see [Types of service catalog variables](https://www.servicenow.com/docs/access?context=r_VariableTypes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

7.  Click **Submit**.


## Result

The record producer is created.

**Parent Topic:**[Configuring Workplace Visitor Management](../concept/configure-visitor-mgmt.md)

**Related topics**  


[Install Workplace Visitor Management](install-workplace-visitor-mgmt.md)

[Create a visitor policy](create-visitor-policy.md)

[Create a visitor badge template](create-visitor-badge-template.md)

[Configuring Workplace Visitor Management for Workplace Services Kiosk](../concept/config-visitor-for-kiosk.md)

[Quick start test for Workplace Visitor Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-wsd-visitor-mgmt.md)

