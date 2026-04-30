---
title: Create an automated test steps template
description: Reduce testing time by creating a template containing a list of steps to add all at once to an automated test.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with test step templates, Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create an automated test steps template

Reduce testing time by creating a template containing a list of steps to add all at once to an automated test.

## Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

Many tests follow similar patterns. One common pattern, for example, is to open a form, set some field values, validate some field values, click a UI action, open a record producer, open a catalog item, and submit the current form. If a template exists containing these steps, you can add them to a test all at once. The Automated Test Framework comes with default templates in the base system. With this procedure, you create your own templates.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Test Templates**.

    The system displays the Test Templates list.

2.  Click **New**.

    The system displays the Test Template form.

3.  In the **Name** field, enter a name for your template.

4.  In the **Test Template** field, click the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\).

    The **Test Template** field unlocks and expands to allow editing.

5.  In the **Test Template** field, enter the name of the first test step to add to this template.

    The system adds the test step to the Test template list.

6.  Continue adding test steps – in the order that you want them to appear – until you've added all the steps that you want to include in the list.

    **Note:** The test template supports tables, catalog items, and the record producer.

7.  In the **Description** field, enter a description for this template.

8.  Click **Submit**.


**Parent Topic:**[Working with test step templates](../concept/atf-templates.md)

**Related topics**  


[Add a predefined list of steps \(template\) to an automated test](atf-use-template.md)

