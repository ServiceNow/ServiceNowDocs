---
title: Allocate a sandbox
description: Allocate sandboxes to your development teams so they can start using them for development.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allocating and retiring, Developer Sandboxes, Developing your application, Building applications]
---

# Allocate a sandbox

Allocate sandboxes to your development teams so they can start using them for development.

## Before you begin

You can also watch a short video on how to allocate a sandbox.

Demo of allocating a sandbox 

Role required: admin

## About this task

You can allocate a sandbox at the beginning of a story or during the project planning process.

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Management Home**.

2.  Select **Allocate sandbox**.

    ![Allocate sandbox button on the home dashboard](../image/dev-sbx-home-allocate-btn.png "Developer Sandboxes home")

3.  On the form, fill in the fields.

<table id="table_r2b_zqk_fcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocate to

</td><td>

User that owns the sandbox.

</td></tr><tr><td>

Sandbox template

</td><td>

Template selected for the sandbox.For information on configuring data profiles and templates to generate reusable data, see [Administering Developer Sandboxes data](configuring-sandboxes.md).

</td></tr><tr><td>

Sandbox alias

</td><td>

Name that's used in the unique URL for the sandbox.

</td></tr></tbody>
</table>    ![Fill in the Allocate Sandbox form](../image/dev-sbx-allocate-modal.png "Allocate Sandbox details")

4.  Select **Allocate**.

    ![Provisioned sandbox initializing](../image/dev-sbx-allocate-requested.png "Sandbox initializing after allocation")


## Result

Developer Sandboxes starts the process of provisioning the sandbox.

**Note:** It can take between 10 minutes and two hours for a sandbox to be provisioned, depending on the size of the tables used in the template. You can select the Refresh icon ![](../image/dev-sbx-refresh-icon.png) to see updates to the Sandboxes list.The record for the sandbox appears in the list as **Initializing** until the sandbox is ready.

Once allocated, developers can access their sandbox by pre-pending the **Sandbox alias** value to the instance name followed by devsandboxes. For example, `https://samsbox.[instance].devsandboxes.servicenow.com`.

Sandbox users use the same login credentials for their sandbox as the base instance. If you use Single Sign-On \(SSO\) for login, when you allow it to connect to your account on the base instance, Developer Sandboxes authenticates using the same mechanism and credentials as the base instance. For information on enabling SSO, see [Installing Developer Sandboxes](../concept/dev-sbx-installing.md).

