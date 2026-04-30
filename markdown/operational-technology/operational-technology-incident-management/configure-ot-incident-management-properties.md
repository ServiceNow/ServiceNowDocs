---
title: Set the system properties
description: Set the system properties for the Operational Technology Incident Management application so that you can enable the incident properties as needed.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2024-08-05"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Set the system properties

Set the system properties for the Operational Technology Incident Management application so that you can enable the incident properties as needed.

## Before you begin

-   Set the application scope to **Operational Technology Incident Management** by selecting the Globe icon \(![Globe icon](../../mftg-manufacturing-ot-vulnerability-response/image/icon-scope.png)\) in the navigation bar.
-   Role required: sn\_ot\_incident\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Operational Technology Incident Management** &gt; **System Properties**.

2.  Enable the following properties as needed for your organization.

<table id="choicetable_xc5_cxy_wvb"><thead><tr><th align="left" id="d51076e100">

Property

</th><th align="left" id="d51076e103">

Description

</th></tr></thead><tbody><tr><td id="d51076e109">

**com.sn\_ot\_inc\_mgmt.sn\_ot\_incident\_task.closure**

</td><td>

Property to close the open OT incident tasks when the related incident is closed or canceled.If you want to close the open incident tasks when the related incident is closed or canceled, set this field to **Yes**.

</td></tr><tr><td id="d51076e123">

**com.snc.sn\_ot\_incident.create.child.enable**

</td><td>

Property to create a child incident feature for the OT incident records.If you want to create a child incident for inciden records, set this field to **Yes**.

</td></tr><tr><td id="d51076e137">

**com.snc.sn\_ot\_incident.copy.attributes**

</td><td>

Property to list the attributes that you want to copy from the parent incident to the child incident.Add any additional attributes needed in the comma-separated list.

</td></tr><tr><td id="d51076e148">

**glide.ui.sn\_ot\_incident\_activity.fields**

</td><td>

Fields that are visible in the activity formatter.Add any additional fields needed in the comma-separated list.

</td></tr></tbody>
</table>3.  Select **Save** to save your changes.


**Parent Topic:**[Configuring Operational Technology Incident Management](../concept/configuring-operational-technology-incident-mgt.md)

