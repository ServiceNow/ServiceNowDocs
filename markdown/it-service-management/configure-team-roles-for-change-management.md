---
title: Configure team roles for Simplified Change Management
description: Assign the right people to the right roles in Change Management so your team can approve, implement, and manage changes with the correct access. Team roles control who can approve, build, or review a change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-team-roles-for-change-management.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 2
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure team roles for Simplified Change Management

Assign the right people to the right roles in Change Management so your team can approve, implement, and manage changes with the correct access. Team roles control who can approve, build, or review a change.

## Before you begin

All groups you plan to assign must already exist in ServiceNow.

Role required: sn\_itsm\_chg\_admin.team\_roles\_config

## About this task

When you add a user to the **Change Manager** or **Implementation groups** field, that user receives the corresponding role, either change\_manager or sn\_change\_write, respectively. Adding a group to either field extends the same role to all users within that group. Removing a user or group from either field revokes the associated role, whether for the individual user or all members of the group.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Team roles**. \[Omitted image "simplified-change-team-roles.png"\] Alt text: Team roles configuration page

5.  In the Who are your change managers? section, assign one or more groups or individuals in the **Change Manager** field.

    **Note:** To add a group to the Change Manager group, make sure its parent group is not already assigned. Adding a group under an assigned parent will result in an error.

    This is a required field. Change managers have full process authority, including approving changes, managing the CAB, overriding escalations, and admin-level access to Change Management configuration.

6.  In the Who raises, reviews, and implements changes? section, assign one or more groups in the **Implementation groups** field.

    This is a required field. Implementers receive change write access; they can create change requests, be assigned as implementers, and complete review tasks.

7.  Select **Save** to save your role assignments.

    To revert unsaved changes, select **Undo**.

8.  When you have finished configuring, select **Mark as configured** to save your settings and mark this step as complete.

    To revert changes made in the current session before saving, select **Undo**.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with Now Assist** conversational flow, accessible from the banner at the top of the page.


## Result

Team roles are now configured and available for use for managing change requests.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

