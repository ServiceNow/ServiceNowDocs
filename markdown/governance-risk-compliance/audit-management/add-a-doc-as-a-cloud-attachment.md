---
title: Link to a cloud file
description: Link a cloud file on Microsoft using file path and file name with a GRC ​record in the Workspace.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Document Management, Audit Management Overview, Audit Management, Governance, Risk, and Compliance]
---

# Link to a cloud file

Link a cloud file on Microsoft using file path and file name with a GRC ​record in the Workspace.

## Before you begin

Role required: sn\_audit\_ws.auditor, sn\_audit\_ws.supervisor

Ensure that the cloud file UI actions on the Cloud files related list are visible on the forms based on the configured conditions. Ensure that file access permissions of read and write are added for the auditor and engagement leads. For more information, see [Create Cloud File Access on engagements and audit tasks](../concept/document-access-configuration.md).

## About this task

Beginning with the Washington DC release, cloud file integration is enabled on the engagement and audit task records using Microsoft integration. Therefore, this task refers to linking a cloud file from Microsoft OneDrive to an engagement record.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the tasks icon \(![Tasks icon](../image/new-task-icon.png)\).

    The list displays the engagements that are assigned to you.

3.  Create an audit engagement or navigate to an existing engagement and go to the **Cloud files** tab.

4.  In the **Cloud files** tab, select **Link cloud file**.

    An Add file pop-up is displayed.

5.  In the **File location** field, enter the path of the folder where the file resides on Microsoft.

6.  In the **File name** field, enter the name of the file with the file format.

    The file name should also include the file extension such as .docx, .ppt, .xls.

7.  Select the **Mark as non-sharable** option.

    When this option is selected, the cloud file that is linked to the record is marked as non-shareable. It cannot be linked with other records in ServiceNow. If you attempt to link a non-shareable file to another ServiceNow record, an error message is displayed.

8.  Select **Link** in the pop-up.

    After the file is connected to Microsoft, the auditor or engagement lead gets read or write access based on the defined access permissions.

    For more information on file access permissions, see [Create Cloud File Access on engagements and audit tasks](../concept/document-access-configuration.md).


