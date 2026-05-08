---
title: Service Builder approval flow
description: As you create and edit services and service offerings in Service Builder, various states get assigned and change on the services' way to being published \(approved\). Administrators enable the standard approval flow and can even customize it using the subflow option in Workflow Studio.
locale: en-US
release: australia
product: Service Builder
classification: service-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Builder, IT Service Management]
---

# Service Builder approval flow

As you create and edit services and service offerings in Service Builder, various states get assigned and change on the services' way to being published \(approved\). Administrators enable the standard approval flow and can even customize it using the subflow option in Workflow Studio.

## Standard approval flow

By default, the approval flow in Service Builder is set to approve services automatically.

When editing a service or offering in Service Builder, the standard approval flow is as follows:

-   As you edit a service or offering, it's in a **Draft** state.
-   After you submit your service or offering, it moves into the **Awaiting approval** state.
-   After your service or offering is approved, it moves into the **Published** state.

You can edit \(checkout\) a service or a single offering, one at a time. You can also edit a service without checking out its child offerings — The offerings remain in the **Published** state until they’re separately checked out.

When you check out an offering to edit it, the offering and its parent service both get checked out. The rest of the child offerings of that parent service remain in the **Published** state. After you finish editing the offering, submit it to the parent service so the offering can be republished \(offerings are published via the parent service\).

## Service states

See the following table for each state in the standard service and service offering approval flow.

<table id="table_b2b_rcc_wqb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Published

</td><td>

When a new service or offering is created and submitted in Service Builder, the item goes through an approval process before it's assigned to the **Published** state. The **Published** state indicates that the item is the version being used by the application and available for others.

 When you edit a published item, Service Builder automatically checks out the item for you and creates a copy for you to work on. The copy is set to the **Draft** state.

</td></tr><tr><td>

Draft

</td><td>

A service item is in the **Draft** state in one of these scenarios:

-   A new service or offering is being created in Service Builder and hasn’t yet been submitted.
-   An existing published service or offering has been checked out for editing in Service Builder.
    -   When the item is being edited, Service Builder checks out the item and creates a copy of it and its related records \(offerings and subscribers\).
    -   The copy is in a **Draft** state.

**Note:** In the **Draft** state \(checked out\), the item displays in both Service Builder and in Service Portfolio Management in one or more of the following ways:

        -   The word \[DRAFT\] is in front of the checked out item name.
        -   A red dot \(![Red dot](../image/sb-service-red-dot.png)\) is next to the item, signifying that it's read only.
        -   A clear triangle warning symbol \(![Clear triangle](../image/sb-service-triangle.png)\) is next to the item name, signifying it's the new copy \(DRAFT\) that's being worked on.
    -   The published item remains in the **Published** state and the **Checked out** field is set to **True**.
    -   After editing and submitting the item, the edits to the draft are merged with the related published item, and then the draft version is deleted.

</td></tr><tr><td>

Awaiting approval

</td><td>

After submitting your service or service offering, your submission goes through an approval process. Your organization's approval flow confirms that the service is created according to standards such as naming conventions, descriptions, proper use of commitments, and key performance indicators \(KPIs\). It also enables a quality check to confirm services aren't duplicative.

 The following lists the tasks for each persona in the approval flow:

-   Service owners create or edit services and offerings in the **Draft** state and then submit them for approval.
-   Process owners and portfolio owners review and approve services and offerings before they approve them for publishing.
-   Process owners and admins can access the 'Service Builder publish' subflow in Workflow Studio to set up and modify the approval flow based on the organizations needs.

</td></tr></tbody>
</table>**Important:**

-   You can only edit an item when it's in a **Draft** state. You can't edit a published item that has been checked out.
-   An item in the **Draft** state is always inactive and doesn't show up in a search or when you're browsing.
-   You can't change the **Active** flag of an item in the **Draft** state.
-   The approval process is available starting with the Utah release and after. Depending on your organization, the approval process could take some time. Contact your administrator if you have questions about the approval process time.

## Enable and customize an approval flow

Administrators enable the approval flow that comes with the base system by updating the 'Service Builder publish' subflow in Workflow Studio.

Administrators can also create a customized approval flow that best meets the organization's needs. See the following for more information about these tasks in Workflow Studio:

-   Edit a flow
-   Ask for Approval action
-   Create a flow in Workflow Studio

