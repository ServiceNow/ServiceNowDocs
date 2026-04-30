---
title: Configure Critical Event Management groups
description: Create groups and assign roles to individuals in the group.
locale: en-US
release: zurich
product: Critical Event Management
classification: critical-event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Critical Event Management, Health and Safety, Employee Service Management]
---

# Configure Critical Event Management groups

Create groups and assign roles to individuals in the group.

## Before you begin

Role required: admin

## About this task

Admins can create agent groups, add members to these groups, and add roles to these members.

-   Create Agent and On-site Responder Groups:

    Set up agent or assignment groups and on-site responder groups based on your organization’s requirements.

-   Assign Roles to Group Members:

    Add members to these groups and assign appropriate roles for their responsibilities.

-   Map On-site Responder Groups to Locations:

    A CEM admin can map each on-site responder group to a specific location to promote accurate assignment during critical events.


After you configure group-to-location mapping, the responder groups are automatically populated based on the critical event's location.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **User and groups** &gt; **Groups**.

2.  Create a new group by selecting **New**.

3.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the group being created.|
    |Manager|Individual responsible for overseeing the group.|
    |Group email|Email address associated with the group.|
    |Parent|Parent group if applicable.|
    |Description|Additional information about the purpose and scope of this group.|

4.  Select **Submit**.

5.  Open the new group and add members and roles for the members.

    **Note:** Assign the following roles to agent groups to enable them to create Health and Safety incidents through Critical Event Management:

    -   sn\_ohs\_im.incident\_reader
    -   sn\_ohs\_im.incident\_writer
    -   sn\_ohs\_im.incident\_create

-   **[Add members to the group](add-members-group.md)**  
Add members to the group mapped to a location.
-   **[Add roles to a member](add-member-roles.md)**  
Add roles to a member of the group mapped to a location.
-   **[Add roles to the group](add-group-roles.md)**  
Add roles to groups that are mapped to a location.
-   **[Map on-site responder group with location](map-on-site-responder-group.md)**  
Map the on-site responder groups with the location, enabling these groups to be automatically populated when the location is selected in a new critical event.

**Parent Topic:**[Configuring Critical Event Management](../concept/configure-critical-event-management.md)

