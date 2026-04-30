---
title: Define conditions for your variant
description: You can define conditions to determine when a page variant is shown. The conditions are based on setting an order, and declaring the criteria that must be met for the page variant to display.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Learn UI Builder by example, Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Define conditions for your variant

You can define conditions to determine when a page variant is shown. The conditions are based on setting an order, and declaring the criteria that must be met for the page variant to display.

This video shows you how to perform the following procedure.This video shows you how to define conditions for your page variant in a UI Builder experience.

## Before you begin

Role required: ui\_builder\_admin

## About this task

If you have multiple page variants that all have the same conditions, the variants go by the order setting.

## Procedure

1.  Open the main page for your demo experience.

2.  Select the experience you created, and select **Default**.

    ![Demo Experience Editor page.](../image/demo-experience-conditions.png "Demo Experience")

3.  On the Default variant under the **All users record page**, select the **Menu** icon \(![Menu icon](../image/three-dot-icon.png)\), and select **Duplicate variant**.

4.  On the **Tell us about your variant** screen, enter **Incident record page** in the **Name** field.

5.  Since the intent of this task is to restrict this page to users who are opening a record in the Incident table, enter the following under Conditions:

    1.  In the **Parameter** field, select **table**.

    2.  In the **Operator** field, select **is**.

    3.  In the **Value** field, replace the text with `incident`.

        When you created this page earlier in the series, you set this condition to the Task table. Now, you are configuring the page to display only to users accessing a record from the Incident table.

    ![Parameter field with dropdown options 'table' and 'sysId', along with Operator and Value fields.](../image/demo-experience-declare-conditions.png "Condition fields")

6.  Select **Create**.

    ![Incident record page in Demo Experience Editor page.](../image/demo-experience-boxed.png "Incident record page")

    **Note:** You can view the structure of your pages and variants in this experience. The **Conditions** column shows a **View** link for each page. You can select **View** to see the condition for that variant \(that is, table=incident\). The **Audiences** column for the Admin only variant shows a 1. You can select the **1** to view the role required to view that variant.


**Parent Topic:**[Learn UI Builder by example](../concept/learning-uib-by-example.md)

**Related topics**  


[Create a demo experience to explore UI Builder](learn-by-example-create-experience.md)

[Create a blank page](learn-by-example-create-blank-page.md)

[Create a record page using a template](learn-by-example-create-page-with-template.md)

[Define an audience for your variant](learn-by-example-define-audience.md)

[Customize forms within a form component](learn-by-example-edit-form-component.md)

