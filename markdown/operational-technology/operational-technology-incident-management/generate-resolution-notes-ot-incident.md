---
title: Generate resolution notes for an Operational Technology incident
description: Generate resolution notes for an Operational Technology \(OT\) incident to share incident resolution information with other users who encounter similar issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-incident-management/generate-resolution-notes-ot-incident.html
release: zurich
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Use ServiceNow Otto for OT Service Management, Use, Operational Technology Incident Management, Operational Technology]
---

# Generate resolution notes for an Operational Technology incident

Generate resolution notes for an Operational Technology \(OT\) incident to share incident resolution information with other users who encounter similar issues.

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

4.  Open the OT incident record to generate resolution notes for.

5.  In the **Resolution notes** field, select the **Use AI to generate notes** \(\[Omitted image "resolution-note-quick-action.png"\]\) quick action.

6.  Select **Generate resolution notes**.

7.  Review the resolution summary in the **Resolution notes** field and make any necessary corrections.

    **Note:** AI-generated content may contain inaccuracies. Review all output before saving.

8.  Manage the OT resolution notes using the available options.

<table id="choicetable_oyw_3jm_ydc"><thead><tr><th align="left" id="d67042e188">

Option

</th><th align="left" id="d67042e191">

Procedure

</th></tr></thead><tbody><tr><td id="d67042e197">

**Insert the resolution notes**

</td><td>

To insert the generated OT resolution notes in the **Resolution note** field, select **Insert**.

</td></tr><tr><td id="d67042e212">

**Refine the resolution notes by elaborating or shortening**

</td><td>

To provide more details in the OT resolution notes, select **Refine** and then **Elaborate**. To shorten the resolution notes, select **Shorten**.

</td></tr><tr><td id="d67042e230">

**Provide feedback for the summary**

</td><td>

If the OT resolution notes were helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text:\). If the resolution notes weren't helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text:\).**Note:** This feedback improves the generative AI model and can help improve future versions of this skill.

</td></tr><tr><td id="d67042e251">

**Copy the resolution notes**

</td><td>

To reuse the OT resolution notes, select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text:\).

</td></tr><tr><td id="d67042e266">

**View the information about the resolution notes**

</td><td>

To view details about the OT resolution notes, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text:\).

</td></tr></tbody>
</table>9.  In the **Resolution code** field, update the resolution code and select **Resolve**.

    A resolution code categorizes how the incident is resolved. For example, Known error and Solved \(Permanently\).

    The resolution information is updated and the state of the OT incident is set to **Resolved**.


**Parent Topic:**[Using ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/using-now-assist-otsm.md)

