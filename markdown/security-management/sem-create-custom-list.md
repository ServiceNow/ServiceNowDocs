---
title: Create a customized list of records
description: You can create a customized list in the Security Exposure Management Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use the List view in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Create a customized list of records

You can create a customized list in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select the **List** icon and click **My Lists**.

3.  Select **New list**.

4.  In the New List modal, click **Start from existing** and search in the List choice list for an existing list to use as a template.

5.  Edit the List Name.

6.  Add filters.

    For example, you might want to create a list of active records for a particular scanner that you want to monitor for rescans. You might use the filters: `Active is true`, and `Source contains (name of your scanner)`.

7.  Edit the columns that you want displayed on your list.

8.  Click **Create**.

    Your new list is displayed.

9.  Alternatively, click **Create your own**, enter a name, followed by **Select Source**.

10. Start typing in the field and select from the sources that display for your new list.

11. Click **Create**.

    Your new list is displayed.

    **Note:** If you leave the list module, the list displayed when you exit is the list you see when you return.

12. To delete a list, with the list displayed, click the gear icon on the upper right of the page.


