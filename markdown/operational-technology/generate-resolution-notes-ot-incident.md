---
title: Generate resolution notes for an Operational Technology incident
description: Automatically update the resolution notes for an Operational Technology \(OT\) incident. You can improve the quality of the resolution notes by providing a summary of the steps taken to resolve the issue. By generating the resolution notes, you can provide information about the incident resolution to other users who might encounter similar issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/generate-resolution-notes-ot-incident.html
release: zurich
topic_type: task
last_updated: "2026-01-14"
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

5.  In the **Resolution notes** field, select the **Use Now Assist to generate notes** \(\[Omitted image "resolution-note-quick-action.png"\] Alt text: Use Now Assist to generate notes quick action feature\) quick action.

6.  Select **Generate resolution notes**.

7.  Review the resolution summary in the **Resolution notes** field and make any necessary corrections.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

8.  When you're finished generating OT resolution notes, you can insert the resolution notes, refine the resolution notes, provide feedback, copy it, or view information about it.

<table id="choicetable_oyw_3jm_ydc"><thead><tr><th align="left" id="d60220e190">

Option

</th><th align="left" id="d60220e193">

Procedure

</th></tr></thead><tbody><tr><td id="d60220e199">

**Insert the resolution notes**

</td><td>

To insert the generated OT resolution notes in the **Resolution note** field, select **Insert**.

</td></tr><tr><td id="d60220e214">

**Refine the resolution notes by elaborating or shortening**

</td><td>

If you want to provide more details in the OT resolution notes, select **Refine** and then **Elaborate**. If you want to shorten the resolution notes, select **Shorten**.

</td></tr><tr><td id="d60220e232">

**Provide feedback for the summary**

</td><td>

If you think that the OT resolution notes were helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the resolution notes weren't helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d60220e255">

**Copy the resolution notes**

</td><td>

If you want to reuse the OT resolution notes, select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\).

</td></tr><tr><td id="d60220e271">

**View the information about the resolution notes**

</td><td>

If you want to check some details about the OT resolution notes, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>9.  In the **Resolution code** field, update the resolution code and select **Resolve**.

    A resolution code categorizes how the incident is resolved. For example, Known error and Solved \(Permanently\).

    The resolution information is updated and the state of the OT incident is set to **Resolved**.


**Parent Topic:**[Using Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/using-now-assist-otsm.md)

