---
title: Define conditions for your variant
description: You can define conditions to determine when a page variant is shown. The conditions are based on setting an order, and declaring the criteria that must be met for the page variant to display.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/learn-by-example-define-conditions.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Learn UI Builder by example, Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Define conditions for your variant

You can define conditions to determine when a page variant is shown. The conditions are based on setting an order, and declaring the criteria that must be met for the page variant to display.

This video shows you how to perform the following procedure.

## Before you begin

Role required: ui\_builder\_admin

## About this task

If you have multiple page variants that all have the same conditions, the variants go by the order setting.

## Procedure

1.  Open the main page for your demo experience.

2.  Select the experience you created, and select **Default**.

    \[Omitted image "demo-experience-conditions.png"\] Alt text: Demo Experience Editor page.

3.  On the Default variant under the **All users record page**, select the **Menu** icon \(\[Omitted image "three-dot-icon.png"\] Alt text: Menu icon\), and select **Duplicate variant**.

4.  On the **Tell us about your variant** screen, enter **Incident record page** in the **Name** field.

5.  Since the intent of this task is to restrict this page to users who are opening a record in the Incident table, enter the following under Conditions:

    1.  In the **Parameter** field, select **table**.

    2.  In the **Operator** field, select **is**.

    3.  In the **Value** field, replace the text with `incident`.

        When you created this page earlier in the series, you set this condition to the Task table. Now, you are configuring the page to display only to users accessing a record from the Incident table.

    \[Omitted image "demo-experience-declare-conditions.png"\] Alt text: Parameter field with dropdown options 'table' and 'sysId', along with Operator and Value fields.

6.  Select **Create**.

    \[Omitted image "demo-experience-boxed.png"\] Alt text: Incident record page in Demo Experience Editor page.

    **Note:** You can view the structure of your pages and variants in this experience. The **Conditions** column shows a **View** link for each page. You can select **View** to see the condition for that variant \(that is, table=incident\). The **Audiences** column for the Admin only variant shows a 1. You can select the **1** to view the role required to view that variant.


**Parent Topic:**[Learn UI Builder by example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/learning-uib-by-example.md)

**Related topics**  


[Create a demo experience to explore UI Builder]()

[Create a blank page]()

[Create a record page using a template]()

[Define an audience for your variant]()

[Customize forms within a form component]()

