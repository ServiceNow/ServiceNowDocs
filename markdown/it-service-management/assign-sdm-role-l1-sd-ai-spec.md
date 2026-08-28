---
title: Assign the Service Desk Manager role from SOW Admin Center
description: Assign the Service Desk Manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role to add the L1 IT Service Desk AI Specialist to your team \(assignment group\) to help with incident resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/assign-sdm-role-l1-sd-ai-spec.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Assign the Service Desk Manager role from SOW Admin Center

Assign the Service Desk Manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role to add the L1 IT Service Desk AI Specialist to your team \(assignment group\) to help with incident resolution.

## About this task

You can assign the Service Desk Manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role manually using the Service Operations Workspace \(SOW\) Admin Center.

Additionally, if you are an existing customer, the Service Desk Manager role is automatically assigned to users who meet any of the criteria below during the upgrade process using a fix script:

-   Assignment group managers with the Service Desk Agent \[sn\_itsm\_common.sn\_service\_desk\_agent\] role
-   Managers of users with the SDA role assigned directly or via group membership
-   Managers of an assignment group specified in the Service Desk Group Inclusion user criteria record
-   Managers of users in assignment groups listed in the Service Desk Group Inclusion criteria.

## Before you begin

-   Ensure the IT Service Management for AI Agent Collection \[sn\_itsm\_aia\] 5.1 is activated.
-   Ensure the Service Operations Workspace \(SOW\) for ITSM application is updated to 8.4 version.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Admin Center** &gt; **Overview**.

2.  Select the **Configuration** tab.

3.  In the Initial setup section, select **Service desk manager role**.

    The Service desk manager page displays the following two tabs:

    -   Service Desk Managers – Contains list of users and user groups assigned to the Service Desk manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role.
    -   All available groups and users - Contains list of users and user groups that are available for assigning the Service Desk manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role.
    **Note:** If no user or user group is currently assigned to the Service Desk manager \[sn\_itsm\_common.sn\_service\_desk\_manager\] role, the **Service Desk Managers** tab displays the **Assign Service Desk manager** role action, which redirects you to the **All available groups and users** tab.

4.  Select the **All available groups and users** tab.

5.  Select any user or user group or both and then select **Add**.

    You can select to add multiple users or user groups.

    The selected user or user group is added to the list of user or user groups in the **Service Desk Managers** tab.


