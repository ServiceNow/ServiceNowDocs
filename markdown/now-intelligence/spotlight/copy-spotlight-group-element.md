---
title: Copy a Spotlight group to breakdown elements
description: You can copy a Spotlight group across multiple elements of a single breakdown.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Copy a Spotlight group to breakdown elements

You can copy a Spotlight group across multiple elements of a single breakdown.

## Before you begin

Finish configuring the Spotlight group that you want to copy.

Role required: admin, pa\_spotlight, pa\_spotlight\_copy\_breakdown

## About this task

When you first create a Spotlight group, you can associate it with at most one element of one breakdown. To create identical Spotlight groups for multiple elements of a breakdown, use the copying function. For example, if you want to use the same Spotlight group configuration for multiple elements of the **Countries** breakdown, create a Spotlight group for one country and copy it to the other countries.

## Procedure

1.  Locate and open the Spotlight group record from the **Spotlight Groups** list.

2.  Click **Copy to breakdown element**.

3.  In the Copy Spotlight Group dialog, select a value for **Name Preference**.

<table id="choicetable_vdg_jsl_dhb"><thead><tr><th align="left" id="d34397e84">

Value

</th><th align="left" id="d34397e87">

Description

</th></tr></thead><tbody><tr><td id="d34397e93">

**Do not change the name**

</td><td>

All copies will have the same name as the original Spotlight group.

</td></tr><tr><td id="d34397e102">

**Change the name**

</td><td>

Manually write a new name that will be given to all copies of the Spotlight group.

</td></tr><tr><td id="d34397e111">

**Add element name to new name as prefix**

</td><td>

For each copy of the Spotlight group, the [breakdown element](../concept/performance-analytics-glossary.md#) name is added to the beginning of the Spotlight group name. You can keep the base name from the original Spotlight group or specify a new one.The **New Name** field does not show these prefixes.

</td></tr><tr><td id="d34397e130">

**Add element name to new name as suffix**

</td><td>

For each copy of the Spotlight group, the breakdown element name is added to the end of the Spotlight group name. You can keep the base name from the original Spotlight group or specify a new one.The **New Name** field does not show these suffixes.

</td></tr></tbody>
</table>4.  Fill out the remaining fields of the **Copy Spotlight Group** dialog:

    |Field|Description|
    |-----|-----------|
    |New Name|Editable field showing the name of the Spotlight group copies you are creating. This field appears if you select any value for **Name Preference** other than **Do not change the name**. All copies have the same name unless you select **Add element name to new name as prefix** or **Add element name to new name as suffix**. The element name prefixes or suffixes do not appear in this field.|
    |Breakdown|If you specified a breakdown when you created the original Spotlight group, the breakdown name appears in this field. Otherwise, select a breakdown. Only the breakdowns that are associated with the main indicator are available.|
    |Element|Select any number of elements for the specified breakdown. A copy of the Spotlight group is made for each selected element.|

5.  Click **OK**.

    The Spotlight group is copied. If copying is successful, a list of the new Spotlight groups that you have created opens. If any error messages or warnings appeared during the copying process, read the [Spotlight group copy logs](../concept/spotlight-copy-logs.md#).

6.  Open each of the Spotlight groups you have created and perform the following steps:

    1.  Review the Spotlight job schedule and adjust as necessary.

    2.  Activate the Spotlight group.


## Copying a Spotlight group for multiple breakdown elements

In this example, you copy the Incident Spotlight group for the breakdown elements Category: Hardware and Category: Software.

1.  Open the Spotlight Groups list and click **Incident Spotlight**.![The Spotlight Groups list with Incident Spotlight highlighted](../image/spotlight-select-group.png)
2.  The Incident Spotlight group record opens, and you click **Copy to Breakdown Element**. ![Spotlight group record with the Copy to Breakdown Element button highlighted](../image/spotlight-copy-for-element.png)
3.  In the **Copy Spotlight Group** dialog, you specify the Category breakdown and select the Hardware and Software elements. You want the element names to appear at the end of the group names, so you also select **Add element name to new name as suffix**.![Copy Spotlight Group dialog filled in with the Category breakdown and the Hardware and Software elements selected.](../image/spotlight-copy-group-elements.png)
4.  You click **OK**, and you go to a list showing you the Spotlight groups that you have created. Both Spotlight groups have the base name Incident Spotlight, as shown in the New Name field of the **Copy Spotlight Group** dialog, with the element name added as a suffix. ![List of the new Spotlight groups you have created by copying a group](../image/spotlight-new-group-copies-elements.png)
5.  Open the Incident Spotlight - Hardware group. Here you verify that the Spotlight job schedule is appropriate, and you activate the group.

    ![Activating the Incident Spotlight - Hardware group](../image/spotlight-group-element-activate.png)

6.  You verify the schedule for the Incident Spotlight - Software group and activate the group.

## What to do next

If any error messages or warnings appeared during the copying process, read the [Spotlight group copy logs](../concept/spotlight-copy-logs.md#).

**Parent Topic:**[Ranking records with Spotlight](../concept/spotlight.md)

