---
title: Add records to related lists
description: Add records to a related list to provide information related to an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-user-interface/configure-user-experiences/add-records-to-related-lists.html
release: xanadu
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working on records in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Add records to related lists

Add records to a related list to provide information related to an incident.

## Before you begin

Role required: agent

## About this task

If there is an **Add** button on your Related Items menu, your system administrator has made it possible for you to add records to related lists. You'd do this when you find a record that's related to the one that's open. For example, if the open record is about a power outtage in one location, if there's a power outtage in a second location, you might add it to the related list of the first record.

\[Omitted image "related-list-add-button.jpg"\] Alt text: Add to a related list

**Note:** Not all workspaces have the **Add** button. It's added by your system administrator.

When you open an incident, you can add locations that are associated with the incident. For example, let's say that a power outage occurred in a location. You might find additional locations with the same power outage that you can add to the original incident report.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open** and click an incident to open it.

2.  In the Affected Locations related list, click **Add** to associate records with the incident you selected.

3.  In the pop-up modal, select the records that you want to add to the open incident.

    The record data is read-only. Selecting the check box in the table heading selects all of the records in the modal and gives you an option of selecting all of the records in the list. Records that are selected on one page remain selected as you move onto another page.

    \[Omitted image "add-records.jpg"\] Alt text: Add records

4.  In the modal, click **Add**.

    The addresses that you selected appear in the Affected Locations related list. They are added to the cmn\_location table and are associated with this incident.

    \[Omitted image "affected-locations.png"\] Alt text: Affected locations


