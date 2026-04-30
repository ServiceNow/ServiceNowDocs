---
title: Create a custom step configuration category
description: Create a custom step config category.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating custom test step configurations, Administering the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Create a custom step configuration category

Create a custom step config category.

## Before you begin

Role required: atf\_test\_admin

## About this task

Categories are used for filtering the step list in the Add Step dialog. For more information, see [Category field example](../reference/atf-step-config-xmpls.md#hbm_xwc_yw).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Step Configuration Categories**.

2.  Click **New**.

    The system shows the **Test Step Config Category** form.

3.  In the **Name** field, enter a name for your step category.

4.  In the **Step Environment** field, enter the step environment in which steps under this category execute:

    -   Server - Independent, if you want this category to contain steps that execute on the Server.
    -   UI, if you want this category to contain steps that execute on browser.
    -   Server - REST, if you want this category to contain steps that send Inbound REST messages to the instance.
5.  In the **Display name** field, enter the category name you want to appear in the middle column of the Add Test Step dialog when this category is selected.

    ![Add test step](../image/atf-category-xmpl.png)

6.  Click **Submit**.

    The system creates a test step category and returns to the list of test step environments.


**Parent Topic:**[Creating custom test step configurations](../concept/atf-custom-step-types.md)

