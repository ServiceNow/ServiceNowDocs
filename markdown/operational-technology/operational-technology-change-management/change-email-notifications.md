---
title: Change email notifications
description: Use email notifications to alert users when an Operational Technology \(OT\) change request or a change task is updated.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Change email notifications

Use email notifications to alert users when an Operational Technology \(OT\) change request or a change task is updated.

The notifications for OT change requests and change tasks are listed in the following tables.

<table id="table_n1f_vgd_mzb"><thead><tr><th>

Name

</th><th>

When to send

</th><th>

Who receives it

</th><th>

What it contains

</th></tr></thead><tbody><tr><td>

Change assigned to me

</td><td>

When the **Assigned to** field changes and is not empty

</td><td>

User who's assigned the change

</td><td>

Subject: &lt;Change request \#&gt; notification Body:

Short Description: &lt;Short description&gt;

Click here to view Change Request: &lt;URL to the change request&gt;

Site: &lt;Site name&gt;

OT Device: &lt;OT device&gt;

Equipment Model Entity: &lt;Equipment model entity&gt;

Description: &lt;Description&gt;

</td></tr><tr><td>

Change assigned to my group

</td><td>

When the **Assignment group** field changes and is not empty

</td><td>

Assignment group

</td><td>

Subject: &lt;Change request \#&gt; has been assigned to group &lt;assignment group&gt;Body:

Short Description: &lt;Short description&gt;

Click here to view Change Request: &lt;URL to the change request&gt;

Site: &lt;Site name&gt;

OT Device: &lt;OT device&gt;

Equipment Model Entity: &lt;Equipment model entity&gt;

Description: &lt;description&gt;

</td></tr><tr><td>

Change commented

</td><td>

When the change request is commented

</td><td>

-   Requested By
-   Watch list

</td><td>

Subject: &lt;Change request \#&gt; comments addedBody:

Short description: &lt;Short description&gt;

Click here to view Change Request: &lt;URL to the change request&gt;

Comments: &lt;Comments added to the change request&gt;

</td></tr><tr><td>

Change worknoted

</td><td>

When a work note is added to the change request.

</td><td>

-   Work note list
-   Assigned to
-   Assignment group

</td><td>

Subject: &lt;Change request \#&gt; work notes added Body:

Short description: &lt;Short description&gt;

Click here to view Change Request: &lt;URL to change request&gt;

Work Notes: &lt;Work notes added to change request&gt;

</td></tr><tr><td>

Change approved

</td><td>

When the change request is approved

</td><td>

-   Assigned to
-   Assignment group

</td><td>

Subject: &lt;Change request \#&gt; has been approvedBody:

Short Description: &lt;Short description&gt;

Click here to view &lt;URL to change request&gt;

Description: &lt;Description&gt;

</td></tr><tr><td>

Change rejected

</td><td>

When the change request is rejected

</td><td>

-   Assigned to
-   Assignment group

</td><td>

Subject: &lt;Change request \#&gt; has been rejectedBody:

Short Description: &lt;Short description&gt;

Click here to view &lt;URL to change request&gt;

Description: &lt;Description&gt;

</td></tr><tr><td>

Change on hold

</td><td>

When the change request is put on hold

</td><td>

Requested By

</td><td>

Subject: &lt;Change request \#&gt; has been put on holdBody:

Hello &lt;user who created change request&gt;,

The &lt;Change request \#&gt; you requested has been put on hold. The reason for the request being put on hold is: &lt;Reason for change request being put on hold&gt;

Click here to view your change request: &lt;URL to change request&gt;

</td></tr><tr><td>

Change off hold

</td><td>

When the change request is taken off hold

</td><td>

Requested By

</td><td>

Subject: &lt;Change request \#&gt; has been taken off holdBody:

Hello &lt;user who created change request&gt;,

The &lt;Change request \#&gt; you requested has been taken off hold and is in the &lt;Updated state field&gt; state.

Click here to view your change request: &lt;URL to change request&gt;

</td></tr></tbody>
</table><table id="table_cdj_cpg_szb"><thead><tr><th>

Name

</th><th>

When to send

</th><th>

Who receives it

</th><th>

What it contains

</th></tr></thead><tbody><tr><td>

Change task assigned to me

</td><td>

When the **Assigned to** field changes and is not empty

</td><td>

Person who is assigned the change task

</td><td>

Subject: &lt;Change task \#&gt; notification -- &lt;Short description&gt;Body:

Short Description: &lt;Short description&gt;

Click here to view Change Task: &lt;URL to change task&gt;

Site: &lt;Site name&gt;

OT Device: &lt;OT device&gt;

Equipment Model Entity: &lt;Equipment model entity&gt;

Description: &lt;Description&gt;

</td></tr><tr><td>

Change task assigned to my group

</td><td>

When the **Assignment group** field changes and is not empty

</td><td>

Assignment group

</td><td>

Subject: Subject: &lt;Change task \#&gt; notification -- &lt;Short description&gt;Body:

Short Description: &lt;Short description&gt;

Click here to view Change Task: &lt;URL to change task&gt;

Site: &lt;Site name&gt;

OT Device: &lt;OT device&gt;

Equipment Model Entity: &lt;Equipment model entity&gt;

Description: &lt;Description&gt;

</td></tr><tr><td>

Change task worknoted

</td><td>

When a work note is added to the change task

</td><td>

-   Work note list
-   Assigned to
-   Assignment group

</td><td>

Subject: &lt;Change task \#&gt; work notes added -- &lt;Short description&gt;Body:

Short description: &lt;Short description&gt;

Click here to view Change Task: &lt;URL to change task&gt;

Work Notes: &lt;Work notes added to change task&gt;

</td></tr></tbody>
</table>**Parent Topic:**[Using Operational Technology Change Management](../concept/using-operational-technology-change-management.md)

