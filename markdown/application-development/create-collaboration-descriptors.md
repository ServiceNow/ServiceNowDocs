---
title: Create collaboration descriptors to assign permissions
description: Create descriptors in the collaboration application so that you can assign permissions to users or groups.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application collaboration, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Create collaboration descriptors to assign permissions

Create descriptors in the collaboration application so that you can assign permissions to users or groups.

## Before you begin

Role required: admin

## About this task

**Note:** You should create collaboration descriptors in addition to Owner and Editor in the global scope. If you want collaboration descriptors to appear and be used in AES, you should also set them to `standard = TRUE`. AES doesn't support collaboration descriptors that are created in custom scopes, and non-standard collaboration descriptors don't render in AES.

Use the predefined collaboration descriptors that are standard with activation, or create a custom collaboration descriptor. Collaboration descriptors enable you to assign, manage, and monitor delegated development permissions for each application or uniformly across multiple applications. You can assign each collaborator with one collaboration descriptor for an application. However, users can have multiple collaboration descriptors simultaneously if they belong to groups where collaboration descriptors have been assigned.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Descriptors**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_gk1_tzs_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the descriptor.

</td></tr><tr><td>

Description

</td><td>

Description of the descriptor that includes permissions capabilities. Examples are as follows: -   Owner
-   Editor


</td></tr><tr><td>

Application

</td><td>

Scope of the collaboration descriptor. Currently, all collaboration descriptors must be created into the global scope.

</td></tr><tr><td>

Standard

</td><td>

Option for inviting other collaborators with this role.

</td></tr></tbody>
</table>4.  Click **Submit**.


