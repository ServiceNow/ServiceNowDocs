---
title: Propose a single change to a CI in Service Operations Workspace
description: Propose new values for one or more CI attributes, review the proposed values, and apply them after the change request reaches the Implement state in Service Operations Workspace \(SOW\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/propose-single-change-ci.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [propose single change, affected CI, change request]
breadcrumb: [Create a change request in Service Operations Workspace, Change Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Propose a single change to a CI in Service Operations Workspace

Propose new values for one or more CI attributes, review the proposed values, and apply them after the change request reaches the Implement state in Service Operations Workspace \(SOW\).

## Before you begin

Role required: itil or admin

## About this task

When you view a CI, you can see proposed changes before they are applied. This is useful when you want to plan modifications prior to the approval stage and apply them only after the change is implemented.

If the change is not approved, no records need to be reversed. If it is implemented, select **Apply proposed changes** to apply all proposed changes.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Open a change request.

    The **Open**, **Closed**, and **All** list views are available.

3.  From the **Overview** tab, scroll down to **Scope and impact**.

4.  Select the **Affected CIs** card.

5.  Confirm that the CI you want to propose changes for is listed in the **Affected CIs** card.

    If the CI is not yet in the list:

    1.  Select **Add**.

    2.  In the **Configuration item** field, search for and select the CI.

    3.  Select **Save** to add the CI to the **Affected CIs** list.

6.  To propose a single change to affected CIs, do the following:

    1.  In the **Affected CIs** list, select the Propose a single change \(\[Omitted image "propose-single-change-icon.png"\] Alt text: Propose a single change icon\) icon next to the CI you want to propose changes for.

        The Propose single change dialog opens and displays the CI class, such as Computer.

        \[Omitted image "propose-single-change-dialog.png"\] Alt text: Propose single change dialog with the Class set to Computer, the Field set to Asset, and Update to set to Apple iPad 3.

    2.  In the **Field** list, select the attribute to change.

        The available fields come from the CMDB CI table for the CI class, such as **Asset tag** or **Asset**.

    3.  In the **Update to** field, enter the proposed value.

        **Tip:** To add multiple fields and their proposed changes, select **Add field**.

    4.  Select **Propose**.

7.  Select the View proposed change \(\[Omitted image "view-proposed-change-icon.png"\] Alt text: View proposed change icon\) icon next to the CI.

    The Proposed change dialog lists each change with its current value, proposed value, and the time the change was proposed.

    \[Omitted image "proposed-change-dialog.png"\] Alt text: Proposed change dialog listing the Asset tag and Attested changes with their current and proposed values.

8.  After reviewing the proposed changes, approve and move the change request to the Implement state.

    For more information, see [Create a change request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-change-sow.md).

9.  Open the change request and select **Apply proposed changes**.

    **Note:** The **Apply proposed changes** button appears only when the change is in the Implement state.

    \[Omitted image "apply-proposed-changes-sow.png"\] Alt text: Change request in the Implement state with the Apply Proposed Changes action available and three affected CIs.

    The proposed values are written to the CI records. The **View proposed change** action no longer appears for the applied CIs.


**Parent Topic:**[Create a change request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/create-change-sow.md)

