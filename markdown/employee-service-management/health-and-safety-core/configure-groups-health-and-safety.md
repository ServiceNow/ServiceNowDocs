---
title: Configure groups for Health and Safety
description: Configure user groups for Health and Safety for assignment of safety records. You can assign roles to groups to provide access to all group members or assign roles to individual users.
locale: en-US
release: yokohama
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure settings, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Configure groups for Health and Safety

Configure user groups for Health and Safety for assignment of safety records. You can assign roles to groups to provide access to all group members or assign roles to individual users.

## Before you begin

Role required: sn\_ohs\_im.admin and admin

## About this task

User groups are used across most processes in the ServiceNow AI Platform for assigning work to teams and requesting approvals.

Any rule that is applied to a group is automatically assigned to group members. For example, roles and assignment rules applied to a group are automatically assigned to group members.

The following groups and their related roles are installed by default as part of the Health and Safety applications regardless of whether demo data is installed:

-   Health and Safety Meeting Managers
-   Health and Safety Meeting Minute Takers
-   Health and Safety Agents
-   Health and Safety Meeting Sensitive Content Group

These groups are available for assignment.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Create a group or modify an existing group.

    -   To create a group, select **New**.
    -   To review an existing group, open the group that you want to configure.
3.  On the form, fill in the fields.

    For detailed instructions and field descriptions, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

4.  Select **Submit** or **Update**.


## What to do next

-   Assign roles to the group. For more information, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Add users to the group.

**Parent Topic:**[Setting up Health and Safety Core](../../hs-core/concept/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core](../../hs-core/task/install-hs-core.md)

[Set up your workplace location data](configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping for generating reports](create-safety-report-field-mapping.md)

[Configure scheduled job to generate frequency rates](configure-job-generate-frequency-rates.md)

[Assign Health and Safety profile to a user](assign-hs-profile-user.md)

[Add a Health and Safety visitor](hs-add-health-safety-visitor.md)

[Migrate existing safety documents to the Document library](../../hs-core/task/hs-migrate-sync-existing-safety-document-docs-library.md)

