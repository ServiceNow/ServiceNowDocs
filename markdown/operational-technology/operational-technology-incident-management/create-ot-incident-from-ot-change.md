---
title: Create an Operational Technology incident from an Operational Technology change request
description: Create an Operational Technology \(OT\) incident related to an OT change request directly from the OT change record in the Industrial Workspace.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-17"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Create an Operational Technology incident from an Operational Technology change request

Create an Operational Technology \(OT\) incident related to an OT change request directly from the OT change record in the Industrial Workspace.

## Before you begin

Role required: sn\_ot\_change\_write and sn\_ot\_incident\_write

## About this task

The following related lists are available in an OT change record in the Industrial Workspace so you can create an OT incident or add an existing OT incident related to the change request.

-   **Incidents Fixed by Change**

    OT incidents that are fixed by the selected change record.

-   **Incidents Caused by Change**

    OT incidents that are caused by the selected change record.


## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Open the Industrial Workspace list view.

3.  In the OT Change Requests list module, select one of the available lists.

4.  Select the change record in one of your sites that you want to create an incident from.

5.  To create an OT incident, complete the following actions.

    1.  In the Incidents Fixed by Change related list or the Incidents Caused by Change related list, select **New**.

    2.  On the form, fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |Number|Unique system-generated incident number that is prefixed with Operational Technology Incident \(OTINC\).|
        |Opened|The date the incident is submitted.|
        |Short description|Brief description of the incident.|
        |Site|Site where the issue happened.|
        |Equipment model entity|Affected equipment model equipment model entity at the site.|
        |OT Device|Affected OT device at the site.|

    3.  Select **Save**.

6.  To add an existing OT incident to the change request record, complete the following actions.

    **Note:** An OT incident can be fixed by one OT change request at most, and caused by one OT change request at most. You can add an OT incident already associated to another OT change request, but doing so overrides the existing relationship.

    1.  In the Incidents Fixed by Change related list or the Incidents Caused by Change related list, select **Add**.

    2.  Select the OT incident that you want to add.

    3.  Select **Add**.


## Result

After you create the incident from the change request, you can view the incident record in the related list or by navigating back to the Industrial Workspace list view. Then select one of the available lists under the **OT Incidents** list module.

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

