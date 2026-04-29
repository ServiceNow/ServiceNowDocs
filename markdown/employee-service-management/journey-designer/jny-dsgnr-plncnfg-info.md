---
title: Journey designer journey template reference
description: The journey template page has information that is useful to the plan configuration owner.
locale: en-US
release: australia
product: Journey Designer
classification: journey-designer
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Journey designer journey template reference

The journey template page has information that is useful to the plan configuration owner.

## Header area

The header of this page displays the plan configuration name and description and the following information.

A ServiceNow administrator assigns owners, co-owners, and approvers.

-   **Owner**

    There can be only one primary owner of a journey template.

-   **Co-owners**

    There can be multiple co-owners for a journey template. Co-owners have the same abilities of the owner to change and publish plan configurations.

-   **Approvers**

    Approvers review and approve or reject changes to a journey template. Changes to a journey template need only one approval.

    **Tip:** Owners can add comments that are displayed in the **Activity** tab of a plan configuration.

    1.  From **My tasks**, open an **Approval request**.
    2.  Select the link at the top of the request.
    3.  In the plan configuration, select the **Activity** tab.
    4.  Read the comments added by the owner to see if there are any special instructions.
-   **Preview**

    Preview a template to make sure the changes you made are what you expected.

    -   **Preview this template**: Preview the template with the roles that are assigned to the owner.
    -   **Preview as an employee**: Preview the template with the roles assigned to the selected user.
    **Note:** The plan configuration preview feature depends on whether the plan configuration owner has access to the selected **Audience type**. These **Audience types** are accessible to all plan configuration owners.

    -   HR Profile
    -   HR Criteria
    -   Users
    -   Users Criteria
    -   Upload file
-   **Publish journey template**

    The changes are visible after an approval by one approver. The template can't be edited until after an approver either approves or rejects the approval request.

    **Note:** Comments are visible as comments in the **Activity** tab.

-   **Cancel approval request**

    The owner or any of the co-owners can cancel the approval request.


## Journey template overview tab

The overview tab shows all the components of a journey that can be modified by owners.

-   **Stages**

    A logical container of a journey that includes tasks that are assigned to employees, mentors, or managers.

-   **Task templates**

    Individual tasks assigned to a user.


## Activity tab

Displays the history of all the changes for a plan configuration in chronological order.

## Email notifications

Owners, co-owners, and approvers can be the recipient of email notifications.

**Note:** Users with **Notification** set to **Disable** won't receive any notifications.

<table><thead><tr><th>

Email notifications are sent when

</th><th>

Email notification recipients are

</th></tr></thead><tbody><tr><td>

An owner or co-owner is assigned to a plan configuration

</td><td>

-   Owner
-   Co-owner

</td></tr><tr><td>

An owner publishes a journey template for approval

</td><td>

Approver

</td></tr><tr><td>

An approver rejects a journey template approval request

</td><td>

-   Owner
-   Co-owner

</td></tr><tr><td>

An owner cancels or rescinds a journey template approval request

</td><td>

Approver

</td></tr><tr><td>

A journey template approval request is approved

</td><td>

-   Owner
-   Co-owner

</td></tr><tr><td>

It has been more than 3 days since a journey template was submitted for approval by the owner**Note:** Notifications are sent on the third day and every other day \(that is, 5th, 7th, 9th days\) until a response is received.

</td><td>

Approver

</td></tr></tbody>
</table>**Parent Topic:**[Journey designer reference](jny-dsnr-reference.md)

