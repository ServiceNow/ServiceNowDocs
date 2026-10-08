---
title: Configure runtime permissions for a playbook
description: Add permission sets to a playbook to restrict who can view and act on it at runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-runtime-permissions-playbook.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Runtime permissions, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Configure runtime permissions for a playbook

Add permission sets to a playbook to restrict who can view and act on it at runtime.

## Before you begin

Role required: playbook.admin, pd\_author

## About this task

Permissions configured at playbook level apply to the whole playbook unless a stage overrides them. For an explanation of how permissions combine, see [Runtime permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/runtime-permissions-playbooks.md).

**Note:** The default parent record requirements always apply. Permissions you add here narrow access further and can't widen it.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to restrict.

3.  From the **More actions** menu, select **Properties**.

    \[Omitted image "pb-run-perm-plybk.png"\] Alt text: Screenshot showing Properties option.

4.  Select **Runtime permissions**.

5.  Review the **Parent record permissions**.

    \[Omitted image "pb-run-perm-plybk1.png"\] Alt text: Screenshot showing Runtime permissions tab and Parent record permissions.

6.  Add permissions and select its source.

    1.  Select **Add permission set** to restrict an operation.

        \[Omitted image "pb-run-perm-plybk2.png"\] Alt text: Screenshot showing Add permission set button.

    2.  Grant the permission set by **User**, **User group**, **Roles**, or a **User criteria** record.

        \[Omitted image "pb-run-perm-plybk3.png"\] Alt text: Screenshot showing user set options.

    3.  Select **View** to grant general access to the playbook.

    4.  Select **Manage** to open and configure additional runtime options.

    5.  Select **Trigger on-demand** to grant access to view the record generator before the playbook is triggered.

        \[Omitted image "pb-run-perm-plybk4.png"\] Alt text: Screenshot showing Additional runtime management options.

    6.  Select the Add permission set icon \[Omitted image "Check.png"\] Alt text: Green check mark icon when you're done configuring the permission.

        \[Omitted image "pb-run-perm-plybk5.png"\] Alt text: Screenshot showing Add permission set button.

    7.  Select **Add permission set** to add more permissions to the same operation.

        Permissions added to one operation combine with OR, so any one of them satisfies it.

7.  Select **Save and close**.


## Result

Users must satisfy the default parent record requirement and at least one permission you added for each operation you restricted.

## Example: Restricting a playbook to expert agents

For example, a case resolution process has two playbooks: a detailed L1 playbook for newer agents, and a shorter L3 playbook for expert agents. Add a permission set to the L3 playbook that names the expert role or a user criteria record, so only those agents can access it at runtime.

## What to do next

Reactivate the playbook. Permission changes affect new executions after reactivation, not existing executions.

**Parent Topic:**[Runtime permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/runtime-permissions-playbooks.md)

**Related topics**  


[Apply runtime permissions for a stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/override-runtime-permissions-stage.md)

