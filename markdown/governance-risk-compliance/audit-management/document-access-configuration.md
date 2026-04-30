---
title: Create a Cloud file configuration on engagements and audit tasks
description: The GRC Workspace administrators can create a Cloud file configuration on engagements and audit tasks from the Cloud file configuration module.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage your documents and work papers with Audit Management as cloud files, Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Create a Cloud file configuration on engagements and audit tasks

The GRC Workspace administrators can create a Cloud file configuration on engagements and audit tasks from the Cloud file configuration module.

## Roles required to access the Cloud file configuration module

Workspace users with the following roles can access the Cloud file configuration module:

|Role|Permissions|
|----|-----------|
|Workspace administrator \[sn\_grc\_workspace.admin\]|CRUD permissions|
|Workspace user \[sn\_grc\_workspace.user\]|Read permissions|

## Cloud file configuration module

If you are the Workspace administrator with the sn\_grc\_workspace.admin role, you can update the following fields in the Cloud file configuration module to configure the permissions as shown in the example.

![File access permissions.](../image/cloud-file-config-file-access-permission.png)

-   Name: Name of the document access record. For example, Engagement document access.
-   Table: Table that is used for the document access record. For example, Engagement \[sn\_audit\_engagement\].
-   Active flag: Flag to mark the cloud file configuration as active.
-   Provider: Provider for the document access record. The default option for this field is Microsoft OneDrive.
-   Cloud action condition: Filter conditions for the cloud files. Based on the configured conditions, the action buttons are rendered in the Cloud files related list.

