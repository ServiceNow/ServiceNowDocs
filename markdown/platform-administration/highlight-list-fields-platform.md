---
title: Highlight list fields
description: Color fields in lists to call an agent's attention to them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Highlight list fields

Color fields in lists to call an agent's attention to them.

## Before you begin

Role required: admin

## About this task

Highlighted fields in lists appear colored and optionally, have a leading bullet.

![highlight list fields](../image/highlight-list-fields.png)

The set up involves specifying the fields that gets highlighted and the conditions that trigger the highlighting.

![When records are listed from the selected Table, the selected Field is highlighted based on the conditions added in the Highlighted Value Conditions tab.](../image/highlight-reasoning.png)

You cannot highlight the following field types:

-   Reference
-   URL
-   Document IDs

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Highlighted Values** and click **New**.

2.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Table|Name of the table that contains the fields you want to highlight.|
    |Field|Name of the field you want to highlight if the triggering conditions are met.|
    |Application|Scope of applications this highlighting pertains to.|
    |Workspace|The workspace this highlighting applies to.|

    The **Field** value can be unrelated to the condition that triggers the highlighting. In the following example, if the **Caller** is Fred Luddy, Workspace highlights the **Priority** field, not the **Caller** field.

    ![Condition and Field are different](../image/caller-fred-luddy.png)

3.  Right-click the header and click **Save**.

    You've specified the field where the highlights appear. Now, it's time to specify the conditions that trigger the highlighting.

4.  In **Highlighted Value Conditions**, click **New**.

5.  In the Highlighted Value Condition form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Conditions|Conditions that trigger the highlighting. The condition can be different from the field that gets highlighted. For example, you might highlight the **Priority** field in a record if the **Caller** in that record is Fred Luddy. A simpler example is highlighting the **Priority** field if the priority value is **critical**.|
    |Status|The highlighting color.|
    |Show Icon|Toggle to display \(selected\) or hide the leading bullet when highlighting. ![Highlighting bullet](../image/bullet-highlighting.png)|
    |Value Override|Text that replaces the field values from the table. If you don't supply a **Value Override**, Workspace highlights the field value from the table. If you supply a value, Workspace replaces the field value with your text and highlights that. ![Override text](../image/override-text.png)|
    |Application|Scope of applications this highlighting pertains to.|
    |Order|The order in which to evaluate the conditions. When you have multiple conditions for highlighting the same field, they are evaluated in order from lowest to highest. If any of the conditions are True, Workspace highlights the field.|

6.  Click **Submit**.

    In the following example, the highlighting was triggered on the **Priority** field because the priority value was critical.

    ![Highlight list fields](../image/highlight-list-fields.png)

7.  Click **New** on the **Highlighted Value Conditions** Related List and create another condition for highlighting the same field.

    For example, highlight the **Priority** field associated with the Incident table when the **Priority** value is "critical," or when the **Caller** value is "Fred Luddy." The conditions are ranked according to the **Order** value. Workspace evaluates the lowest value first.

    ![Two conditions](../image/two-conditions.png)

8.  Remove all highlighting from a filtered list that would otherwise have highlighting.

    When setting up highlighting for a table, all filtered lists associated with the table display highlighted fields unless you disable highlighting for specific, filtered lists.

    1.  Navigate to `sys_aw_list.list`.

    2.  In the **Name** column, enter the name of the table with highlighted fields, for example, Incident.

        All filtered lists associated with the table appear.

    3.  Click the filtered list you want to remove highlighting from.

    4.  On the Workspace List form, if Global is the current application, click **here** in **To edit this record click here.**

    5.  Select the **Ignore Highlight in List**check box and click **Update**.

        Now, regardless of the conditions, Workspace will not highlight any fields in the specified filtered list. This option does not work, however, for filtered lists in **My Lists**, which are the filtered lists agents create.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../../field-administration/concept/customize-fields-now-platform-landing.md)

