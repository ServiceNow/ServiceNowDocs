---
title: Example: Use a custom field to dynamically control set size
description: This example demonstrates how to hide a standard field and replace it with a custom field.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Configure sets, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Example: Use a custom field to dynamically control set size

This example demonstrates how to hide a standard field and replace it with a custom field.

## About this task

This article demonstrates how to hide the Size field \(shown below\) on a layout and replace it with a different field. A rule populates the value from the new field into the hidden field.

![User interface](../images/cpq-layout-size.png)

## Before you begin

Role required: Admin

## Procedure

1.  In the layout wizard, turn off the Show Size Field setting.

    ![Size settings](../images/cpq-layout-wizard-settings-show-size-field.png)

    Although the set size field still exists, it no longer appears in the layout. For more information about sets and layouts, see [Using sets in layouts](layouts-sets.md).

2.  Create your replacement number field and add it to the layout.

    You can change the display type as desired. In the example below, we created a number field using a slider.

    ![User interface](../images/cpq-layout-new-number-field-with-slider.png)

    The final task is to create a rule to take the value from the new field and enter it into the \(hidden\) Size field.

3.  Create a rule, set your conditions, and create a Determination Action.

    In the rule action:

    -   Define your original Set Size field as the field in which the value will be injected.
    -   Select **Advanced**.
    -   Click **Edit Advanced Function** and input a single line of code that returns the value of your new field.
    For example, assume that the new field has a value of numberOfHardDrives. As seen in the image below, our line of code would simply be:

    ```
    return cfg.numberOfHardDrives;
    ```

    ![Determination action](../images/cpq-layout-determination-action.png)

4.  Deploy and test your updated blueprint.

    When you modify the values of the field that you created, the size of the Set should be updated accordingly.


