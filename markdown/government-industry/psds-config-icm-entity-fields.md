---
title: Configure property entity fields in Investigative Case Management
description: Extend the Property Index by adding a new field. This field can be used when logging property entity records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-config-icm-entity-fields.html
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Evidence Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure property entity fields in Investigative Case Management

Extend the Property Index by adding a new field. This field can be used when logging property entity records.

## About this task

## Before you begin

Role required: admin

**Note:** The Property Index is an extension of the Master Index Table. To create a brand new entity type to be displayed as a new tab on the case record, see [Configure entity types in the Investigative Case Management Entity Management workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-config-icm-add-entity-type.md) .

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables**.

2.  In the Extends table column, search for Master Index.

    Here, you can view all the default tables that extend from the Master Index.

3.  Select the Property Index record.

4.  Navigate to **Columns** &gt; **New** to create a new Dictionary Entry field.

5.  On the form, fill in the following fields:

    | | |
    |---|---|
    |Table|Property Index \[sn\_icm\_property\]|
    |Type|Choice|
    |Column Label|Brief description of the column field.|
    |Choice List Specification|Dropdown with **None**|

6.  Select **Submit**.

    **Note:** Refresh the page if the newly created Dictionary Entry field does not appear, or select the next arrow to move to the next page.

7.  Select the newly created Dictionary Entry in the Column related list.

8.  Navigate to the **Choices** related list and select **New** to configure the choice options.

9.  Complete the fields with your desired choice selections, selecting **Update** after each entry.

10. Select the back arrow to return to the Property Index table.

11. Select **Form Builder Related Links** on the Property Index table.

    **Note:** There are two views for Property index: Workspace for Workspace List view and ICMCase for ICM Case Property Tab view, and both are in different application scopes. First, change the view, then change the application scope.

12. In the Default view dropdown, select **ICMCase**, and set the application scope to Investigative Case Management.

13. In the **Add form elements** panel, search for the newly created field

14. 15. 16. 17. 
