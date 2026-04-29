---
title: Define a breakdown source
description: Specify a facts table to serve as a data source for breakdowns. External data is supported via Workflow Data Fabric tables. Apply conditions to specify the elements for this breakdown source.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Breakdown sources, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Define a breakdown source

Specify a facts table to serve as a data source for breakdowns. External data is supported via Workflow Data Fabric tables. Apply conditions to specify the elements for this breakdown source.

## Before you begin

Roles required: pa\_data\_collector, pa\_admin, or admin. The breakdown source creator needs access to the table and reference column that the indicator source uses.

## About this task

Always use a facts table with a field that has a unique value for every record, usually **Sys ID**. For example, the Incident.Category breakdown source takes its elements from the **Choice** table. The elements are identified by the **Sys ID** field. The breakdown source filters the choices to those that are on the **Incident** table, in English, and not inactive.

**Tip:** As in this example, if you use Choice \[sys\_choice\] for the facts table, put conditions on the Table, Element, and Language fields. Also filter out Inactive records.

![The filled out breakdown source form for Incident.Category, showing facts table, field, and conditions](../image/CreatingBreakdownSourcesExample.png)

The breakdown source uses the following records from the Choice table:

![Filtered choice table records corresponding to breakdown source example.](../image/choices-table-category-element.png)

**Note:** The Choice table includes every possible choice from every table, which is why it has Table and Element columns. Most other facts tables you would use for a breakdown source are simpler.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Breakdown Sources** and click **New**.

2.  Give the breakdown source a meaningful **Name**.

3.  Add a detailed **Description** to help others understand the use and purpose of this breakdown source and to help them avoid creating duplicates.

4.  For the **Facts Table**, select the table that the breakdown source gets elements from.

    For example, for the breakdown source to specify user groups as elements, select **Group \[sys\_user\_group\]**.

    **Warning:** Do not change the facts table for a source after you have started collecting data. If you change the facts table, you lose all historical scores for the associated indicators at the next score collection.

5.  In the **Field** table, select a field that contains a unique value for every record.

    This field is usually **Sys ID**.

6.  Set the **Conditions** to filter out unneeded elements.

    If you set Choice \[sys\_choice\] as the facts table, always filter on table, element, and language, and filter out inactive records. For example:

    **\[Table\] \[is\] \[Incident\]** and

    **\[Element\] \[is\] \[Category\]** and

    **\[Language\] \[is\] \[en\]** and

    **\[Inactive\] \[is\] \[false\]** or

    **\[Inactive\] \[is\] \[empty\]**

7.  To see how many records match the selected conditions, click **Preview**.

8.  Define **RELATED LIST CONDITIONS** to include a relationship with another table in the filter.

    For more information, see [Add related list conditions](https://www.servicenow.com/docs/access?context=create-related-list-query&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    For example, consider a breakdown source for Configuration Item \(CI\) Managers. The facts table is User \[sys\_user\], but the only condition you can apply from this table is to filter for active users. No field on the table lets you select only users who are CI Managers. You get hundreds of results.

    ![Breakdown source only filtering on active users](../image/bkdown-source-wo-related-list.png)

    If you add a condition that the Name on the User record must match at least one entry in the Managed by column of the Configuration Item \[cmdb\_ci\] table, the breakdown source only returns the users who are CI Managers.

    ![Breakdown source with related list condition](../image/bkdown-source-rel-list-cond.png)

9.  In **Label for unmatched**, write a custom label to use when the value in a mapped field on an indicator source record does not match any elements on the breakdown source.

    The default label is **Unmatched**.

    The Incident.Category breakdown source references records on the Choices \[sys\_choices\] table where the value of the Table field is incident and the value of the Element field is category. The Category breakdown includes a mapping from the Incident.Category breakdown source to the Category field on the Incidents \[incident\] table. If an Incident record has a null value in the Category field, the value when you apply the Category breakdown to this record is **Unmatched**, by default.

10. In the **Security** tab, set whether to exclude or include breakdown source elements by role based on element security lists.

    For more information, see [Define an elements security list](t_ControlAccessToABreakdown.md#).


## What to do next

Create breakdowns that use this breakdown source. You can open the **Breakdowns** tab and click **New**. The **Breakdown** form opens, as described in [Create an automated breakdown](t_CreatingABreakdownForIndicators.md). After you create breakdowns that use this source, these breakdowns are listed in the **Breakdowns** tab.

**Parent Topic:**[Breakdown sources](../concept/breakdown-sources.md)

