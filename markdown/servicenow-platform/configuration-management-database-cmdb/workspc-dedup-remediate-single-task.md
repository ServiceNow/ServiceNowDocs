---
title: Remediate a single de-duplication task
description: Remediate a single de-duplilcation task using a de-duplication template in CMDB Workspace, in Service Graph Workspace, or manually, using the Duplicate CI Remediator.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remediate a single de-duplication task

Remediate a single de-duplilcation task using a de-duplication template in CMDB Workspace,in Service Graph Workspace, or manually, using the Duplicate CI Remediator.

## Before you begin

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform this task, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Dashboard** link in Management tools, in the Manage section.

3.  In the De-duplication templates section, select **View de-duplication tasks**.

4.  In the De-duplication tasks list view, select the task that you want to remediate.

5.  Select **Remediate** on the task form.

6.  In the Remediate dialog box, choose which method you want to use for remediation, and then select **Remediate**.

<table id="choicetable_khq_wpd_fzb"><thead><tr><th align="left" id="d259440e154">

Choice

</th><th align="left" id="d259440e157">

Description

</th></tr></thead><tbody><tr><td id="d259440e163">

**Remediate manuallyUse the Duplicate CI Remediator**

</td><td>

Use the Duplicate CI Remediator built on Core UI to remediate the task.

 To continue with this choice of remediation, see [Remediate a de-duplication task \(manual\)](reconcile-dup-task.md).

</td></tr><tr><td id="d259440e188">

**Use the Duplicate CI Remediator in Restricted Mode**

</td><td>

Appears only if the **glide.duplicate\_ci\_remediator.enable\_restricted\_mode** system property is set to **true**. You might need to use this option if remediation is blocked because loading the de-duplication task times out. This option might be relevant when there is a large number of related items associated with a de-duplication task, allowing remediation to continue with the limited features in a restricted mode. For more information about using this option to restrict the use of related items in de-duplication remediation and allow remediation to proceed, see [Using restricted mode within the Duplicate CI Remediator \[KB1542272\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1542272).

 To continue with this choice, see [Remediate a de-duplication task \(manual\)](reconcile-dup-task.md). Skip to step \#5 in the procedure.

</td></tr><tr><td id="d259440e220">

**Remediate using a template**

</td><td>

Use a de-duplication template to remediate the task.

 To continue with this choice of remediation: In the Remediate dialog box, select the **Library** and the **Template** to use for the remediation, and then select **Remediate**.

</td></tr></tbody>
</table>
## What to do next

On the task form:

-   Track the progress and the details of remediation in the Activity stream until remediation is complete.
-   Select the **Duplicate Audit Results** tab to see the results of the duplicate audit.

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

