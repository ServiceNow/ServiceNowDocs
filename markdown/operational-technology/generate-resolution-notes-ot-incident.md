---
title: Generate resolution notes for an Operational Technology incident
description: Automatically update the resolution notes for an Operational Technology \(OT\) incident. You can improve the quality of the resolution notes by providing a summary of the steps taken to resolve the issue. By generating the resolution notes, you can provide information about the incident resolution to other users who might encounter similar issues.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Now Assist for OTSM, Operational Technology]
---

# Generate resolution notes for an Operational Technology incident

Automatically update the resolution notes for an Operational Technology \(OT\) incident. You can improve the quality of the resolution notes by providing a summary of the steps taken to resolve the issue. By generating the resolution notes, you can provide information about the incident resolution to other users who might encounter similar issues.

## Before you begin

Role required: sn\_ot\_incident\_write

## About this task

OT incident resolution notes are generated from the following information:

-   Short description
-   Description
-   Work notes
-   Additional comments
-   State
-   Site
-   Equipment model entity
-   OT device

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Open the Industrial Workspace list view.

3.  On the OT Incidents module, select one of the available lists.

4.  Open the OT incident record that you want to generate resolution notes for.

5.  In the **Resolution notes** field, select the **Use Now Assist to generate notes** \(![Use Now Assist to generate notes quick action feature](../image/resolution-note-quick-action.png)\) quick action.

6.  Select **Generate resolution notes**.

7.  Review the resolution summary in the **Resolution notes** field and make any necessary corrections.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

8.  When you're finished generating OT resolution notes, you can insert the resolution notes, refine the resolution notes, provide feedback, copy it, or view information about it.

<table id="choicetable_oyw_3jm_ydc"><thead><tr><th align="left" id="d66071e192">

Option

</th><th align="left" id="d66071e195">

Procedure

</th></tr></thead><tbody><tr><td id="d66071e201">

**Insert the resolution notes**

</td><td>

To insert the generated OT resolution notes in the **Resolution note** field, select **Insert**.

</td></tr><tr><td id="d66071e216">

**Refine the resolution notes by elaborating or shortening**

</td><td>

If you want to provide more details in the OT resolution notes, select **Refine** and then **Elaborate**. If you want to shorten the resolution notes, select **Shorten**.

</td></tr><tr><td id="d66071e234">

**Provide feedback for the summary**

</td><td>

If you think that the OT resolution notes were helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the resolution notes weren't helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d66071e257">

**Copy the resolution notes**

</td><td>

If you want to reuse the OT resolution notes, select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\).

</td></tr><tr><td id="d66071e273">

**View the information about the resolution notes**

</td><td>

If you want to check some details about the OT resolution notes, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>9.  In the **Resolution code** field, update the resolution code and select **Resolve**.

    A resolution code categorizes how the incident is resolved. For example, Known error and Solved \(Permanently\).

    The resolution information is updated and the state of the OT incident is set to **Resolved**.


**Parent Topic:**[Using Now Assist for Operational Technology Service Management \(OTSM\)](../concept/using-now-assist-otsm.md)

