---
title: File access permissions
description: The Workspace administrators with the sn\_grc\_workspace.admin role can configure the file access permissions for the users and groups.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a File access permission record to manage the permissions, Create a Cloud file configuration on engagements and audit tasks, Manage your documents and work papers with Audit Management as cloud files, Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# File access permissions

The Workspace administrators with the sn\_grc\_workspace.admin role can configure the file access permissions for the users and groups.

## Conditions for file access permissions

The Workspace administrators with the sn\_grc\_workspace.admin role can configure different conditions for file access permissions:

-   For a combination of the **Table** field, **Access permission** field, and **Users** field, you can have only one File access permission record. If you have an existing record for a table with a given set of user and access permissions, you cannot create a duplicate record with the same access permissions. For example, if a contributor has Read access permission for the policy \(sn\_compliance\_policy\) record, creating another record for the same condition is not permitted.
-   For a given combination of the **Table** field, **Provider** field, and **Active** option, only one Cloud file configuration record is permitted. A duplicate configuration is not permitted for an active table as shown in the following example.

    ![Duplicate configuration.](../image/doc-access-config-no-duplicate-config.png)

-   If a user is part of multiple **User** fields or a **Group** field, a higher access is granted to the user.

## Source link and reference link to the GRC record

When a cloud file is connected to a GRC record for the first time, the connection is considered as a source link to the GRC record.

When the same cloud file is mapped to another GRC record, then it is considered as a reference link to the GRC record.

A source link to the GRC record always has the write access and the reference link to the GRC record always has the read access.

When a record is mapped as a source link to the cloud file, the configuration is applied as it is to the cloud file. For example, if the configuration contains write access for some users and read access for some users, the same configuration is maintained and applied to the users.

The Document reference table shows how one document record is being referenced such as its source link and reference link to the GRC record as shown in the following example ![Document reference table.](../image/doc-ref-table.png)

Consider the example of Engagement\_memo.xslx for which Control test CTR0020005 is a source link and Control test CTR0020004 is a reference link. For any configuration that matches the configuration of Control test CTR0020004, all the users under this configuration even though they have Write access in the configuration has only read access.

Consider the following example where a Risk and Controls Matrix Report is connected to Engagement record 1 and Engagement record 2.

|Document|Record that the document is connected to|
|--------|----------------------------------------|
|Risk and Controls Matrix Report|Engagement record 1. It is the source for the access document.|
|Risk and Controls Matrix Report|Engagement record 2. It is the reference for the access document.|

See the following table for the permissions assigned for the example.

|Access doc connected to the record|Users field value|Type of access|Description|
|----------------------------------|-----------------|--------------|-----------|
|Engagement record 1|Contributors|Have Write access|For the source record, the permission configuration is considered as it is configured. Therefore, the contributors have the Write access to Engagement 1.|
|Engagement record 2|Reviewers|Have Write access|The same access record is mapped to Engagement 2, for which the reviewers should have the Write access. Because Engagement record 2 is a reference record, the reviewers have the Read access instead of the Write access.|

## Another use case for source link

When the cloud document is mapped to a record, it becomes a source link for the cloud document. If the same record is removed and the cloud document is mapped to another GRC record, the next record becomes the source link for the cloud document.

For example, the Engagement\_memo.xlsx file is mapped to the engagement 1 and engagement 2 records. The engagement 1 record is the source link and the engagement 2 record is the reference link. If the mapping between the Engagement\_memo.xlsx file and the engagement 1 record is removed, the Engagement\_memo.xlsx file does not have any source link. If the Engagement\_memo.xlsx file is mapped to the engagement 3 record, then the engagement 3 record becomes the source link for the document.

## Request access and Refresh file access actions

By default, the file access permissions are enabled on the engagement and audit task records. For other records, you can use the **Request access** and **Refresh file access** actions on the form. By default, the file access permissions are enabled on the engagement and audit task records. If a user is part of a group, they can use the **Request access** UI action to request access to the file. The **Request access** UI action is available only to the group members. If the user is part of a cloud file configuration, they can use the **Refresh file access** action to refresh or configure the file access. The **Refresh file access** action is available to the users mentioned in the cloud file configuration.

To configure the file access permissions on other tables such as control records or policy records \(instead of using the manual **Request access** and **Refresh file access** actions\), see the configuration steps in KB1587297.

The users that are part of a group should request access to the cloud file by using the **Request access** action button. When a user who is part of the Audit Managers group selects **Request access** on the form, a UI message is displayed as shown in the example: `The file access is being processed.`

![Request access.](../image/request-access.png)

Requesting access to the cloud file is a one-time activity for the users of a group. If a user selects **Request access** more than once and the access has already been granted, the following message is displayed: `File access has already been granted.`

If the user requests access to the cloud file and if the request is not processed in time, an error message is displayed on the screen. The user must select **Refresh file access** to request an access to the file again.

