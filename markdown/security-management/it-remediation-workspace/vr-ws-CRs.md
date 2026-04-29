---
title: Create a change request in the IT Remediation Workspace
description: From a remediation task \(VUL, AVUL, CVUL, or CRG\), create a change request. Alternatively, add a remediation task to an existing change request.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Create a change request in the IT Remediation Workspace

From a remediation task \(VUL, AVUL, CVUL, or CRG\), create a change request. Alternatively, add a remediation task to an existing change request.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

**Note:** The itli role is required if you want to submit change requests from the IT Remediation Workspace.

## About this task

There might be various reasons that you want to create a change request for a remediation task. Usually, it is because your investigation requires manual intervention to fix the vulnerabilities.

For more information about the change requests and creating change requests from the classic environment, see [Change management for Vulnerability Response](../concept/vuln-change_mgmnt_ovrvw.md).

**Note:** Starting with v19.0 of Vulnerability Response, the following terms have been renamed:

|Terminology prior to v19.0|Terminology v19.0 onwards|
|--------------------------|-------------------------|
|Test Result Groups|Remediation Tasks|
|Configuration Issues|Configuration Test Results|
|Policy|Test group|

## Procedure

1.  Navigate to **Workspaces** &gt; **IT Remediation Workspace**.

2.  Select the List icon.

3.  On the List page, in the Remediation tasks list, locate a remediation task \(VUL, AVUL, CVUL, or CRG\) that you want to create a change request for.

4.  In the UI action buttons on the right, expand the list and choose one:

    -   Click **Create Change**
    -   **Add to existing change**
5.  To create a new change request, in the modal that displays, fill in the fields.

    For information on the form fields, see [Create change request form fields](../../vr-it-remediation-workspace/reference/itr-ws-create-cr-fields.md).

6.  Select **Create Change Request**.

    The remediation task record displays and a message indicates that the change request is successfully created.

    Click the Change Requests related link on a record to view all the change requests associated with the record.

7.  Alternatively, to add this remediation task to an existing change request, follow these steps.

    1.  Click the down arrow to expand the list on the **Create Change** button.

    2.  Select **Add to existing change**.

    3.  In the modal that displays, click the search icon to view the list of existing change requests.

    4.  To add conditions to the list to focus the list of change requests, in the upper right of the modal, click the filter icon \(funnel\).

    5.  In the new pane that is displayed, click **Advanced view**.

    6.  Use the condition builder to create your conditions.

    7.  Select **Update**.

    8.  From the list, click a change request to select it.

        An updated modal is displayed with your choice.

    9.  In the modal, select the Add CIs to CR check box to add configuration items from all the active vulnerable items to the change request.

    10. Select **Add change**.

        The remediation record displays, and a message indicates that the change request is successfully created and submitted for approval.

        -   Click the **View change** link in the message to open the change request \(CHG\) record.
        -   Select the **Change Requests** related item menu link on the remediation task record to view all the change requests associated with the record.
        Alternatively, in the classic environment, navigate to **Self-service** &gt; **My Requests**. After you submit the change and it is implemented, if state synchronization is enabled, the remediation task automatically moves to `Resolved`. For more information about states and state synchronization in change requests, see [Create a change request from a remediation task](vuln-change_mgmnt_create_change.md).


