---
title: Set File Access Permissions
description: Create a File access permission record and manage the access permissions on the cloud document.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud File Access Setup, Cloud Document Management, Use, Audit Management, Governance, Risk, and Compliance]
---

# Set File Access Permissions

Create a File access permission record and manage the access permissions on the cloud document.

## Before you begin

Role required: sn\_grc\_workspace.admin \(CRUD\), sn\_grc\_workspace.user \(Read\)

## About this task

By default, the file access permissions are enabled on the engagement and audit task records. A user that is part of a group can select **Request access** to request an access to the file. The **Request access** UI action is available only to the group members. A user that is part of a cloud file configuration can use **Refresh file access** to refresh or configure the file access. The **Refresh file access** action is available to the users that are listed in the cloud file configuration.

Instead of using the manual **Request access** and **Refresh file access** actions, you can configure file access permissions on other tables such as control records or policy records. For more information, see the configuration steps in KB1587297.

## About this task

The File access permission record enables the users to manage access permissions on the cloud document.

## Procedure

1.  Navigate to **All** &gt; **GRC Administration** &gt; **Cloud file configuration**.

2.  Select an active parent cloud file configuration record.

    The cloud file configuration record is displayed.

    ![Cloud file configuration record.](../image/cloud-file-configuration-record.png)

3.  In the File access permissions related list, select **New**.

    You can use the **Users** field to select one of the user \(sys\_user\) fields from an engagement or audit task such as engagement lead, auditors, and others. The users selected in the **Users** field are granted access to the cloud file.

    You can configure the file access permissions for one or more users of the record as shown in the following example.

    ![File access permission record.](../image/file-access-permissions-record.png)

    You can use the **Group** field on the form to select one of the group \(sys\_user\_group\) fields from an engagement or audit task such as an assignment group. The users that are part of the group are granted access to the cloud file. A File access group permission record is displayed in the following example.

    ![File access group permission.](../image/file-access-group-permissions.png)

4.  On the form, fill in the fields.

    For more information on the fields in the form, see [File access permission record form](../reference/file-access-permission-record-form.md).

5.  Select **Submit**.

    Based on the configuration set up in the form, the permissions on the cloud document are evaluated.


