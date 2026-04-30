---
title: View a workflow example in the IT Remediation Workspace
description: View an example of an end-to-end workflow in the IT Remediation Workspace. See how IT specialists might use the workspace to monitor critical vulnerable items \(VITs, AVITs, and CVITs\) and test results \(TRs\) and remediate the vulnerabilities assigned to them.
locale: en-US
release: zurich
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# View a workflow example in the IT Remediation Workspace

View an example of an end-to-end workflow in the IT Remediation Workspace. See how IT specialists might use the workspace to monitor critical vulnerable items \(VITs, AVITs, and CVITs\) and test results \(TRs\) and remediate the vulnerabilities assigned to them.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Click the following image to view the steps of the workflow.

    IT Remediation Workspace demo

    The image includes the following tasks:

    -   From the Home page \(IT Remediation Owner landing page\), view the remediation tasks that are assigned to you. Toggle between work that is assigned to you and your group. See the host remediation tasks that have solutions. For more information on the Home page, see [Home page in the IT Remediation Workspace](../../vr-it-remediation-workspace/concept/itr-ws-home-page.md).
    -   Select the **List** view to see the lists of your assigned work.
    -   From the List view with the **Assigned to my group** list selected in the Remediation Tasks list, identify and assign work to yourself. For more information on the List page, see [List page in the IT Remediation Workspace](../../vr-it-remediation-workspace/concept/itr-ws-list-page.md).
    -   Group the remediation tasks by record type: Select the three dot menu on the **Record Type** column and then select **Group by Record type**.
    -   On an open remediation task \(VUL, AVUL, CVUL, and CRG\):
        -   Select the **Overview** tab to see the records \(VITs, AVITs, CVITs and TRs \) and affected configuration items \(CIs\) that are associated with the record.
        -   Select the **Solutions** tab to see preferred and potential solutions for a host remediation task.
        -   Select the **Details** tab to modify editable fields such as State, Assignment group, Assigned to, and Short description and view the actions performed on a remediation task.
        -   Select the **State Change Approval** tab, to view the state change approval records \(CA\#\) which helps you to track the approval workflow.
        -   Select the **Change requests** tab, to view the approval status of the change requests and to create a new change request by selecting the **New** button.
        -   Select the UI actions: **Mark as False Positive**, **Create Change**, **Split Task**, **Update status****Request Exception**, **Delete** and so on. Follow the prompts in the dialogs to help you with your remediation.

