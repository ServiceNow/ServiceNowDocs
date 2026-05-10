---
title: Request activation approval for a badge reader device
description: Request activation approval for your badge reader device. Badge Reader Integration will not trigger event handlers until the badge reader is activated. Badge reader device approval and activation is granted by users with the itil role.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Request activation approval for a badge reader device

Request activation approval for your badge reader device. Badge Reader Integration will not trigger event handlers until the badge reader is activated. Badge reader device approval and activation is granted by users with the itil role.

## Before you begin

Role required: sn\_badge.badge\_admin

## About this task

When you request activation approval, via the Badge Reader record, you initiate the device registration flow. Activation requests are routed to a badge reader approvers group. System approvals require the itil role. Ensure users with the itil role are added to the badge reader approvers group.

If there are no people in the approval group, the flow will skip past the approval group requirement, and activate the badge reader. For detailed information about approvals, groups, and adding users to groups, refer to [Approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/r_Approvals.md) [Creating groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-groups.md) and [Add a user to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AddAUserToAGroup.md).

**Note:** Badge Reader record required fields are read only when the badge reader device is activated. Badge reader devices can be deactivated by de-selecting the **Active** field on the Badge Reader record. Reactivation of a badge reader requires going through the approval process again.

## Procedure

1.  Navigate to **All** &gt; **Badge Reader Integration** &gt; **Badge Readers**.

2.  Select the name of the badge reader you want to activate.

    The Badge Reader record opens.

3.  Ensure that all mandatory form fields are populated.

    The fields included are the **Name**, **Badge Event Handler**, **Device Identifier**, and **Secret Key** fields. See [Define and register a badge reader device using the badge reader client](assisted-config-badge-read-settings.md) or [Define and register a badge reader device manually](config-badge-reader-settings.md) for information regarding populating Badge Reader form fields.

4.  Select **Request Activation** to initiate the activation approval workflow.

    The request is approved by a user with the itil role in the badge reader approvers group. If there is no badge reader approvers group or the group is empty, then the badge reader is activated when a user with the sn\_badge.badge\_admin role requests activation.


**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

