---
title: Allocate a sandbox
description: Allocate sandboxes to your development teams so they can start using them for development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/allocating-sandboxes.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Administering, Developer Sandboxes, Developing your application, Building applications]
---

# Allocate a sandbox

Allocate sandboxes to your development teams so they can start using them for development.

## Before you begin

You can watch a short video on how to allocate a sandbox.

\[Omitted video\] Description: Demo of allocating a sandbox

Role required: admin or sandbox\_manager

## About this task

You can allocate a sandbox at the beginning of a story or during the project planning process.

When you allocate a sandbox, you claim one from a pre-created pool rather than waiting for a new instance to be provisioned. This makes sandboxes available faster, so you can start working sooner.

**Note:** Because pooled sandboxes are pre-created, they may be out of date from the current base instance state, but are refreshed every 24 hours.

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Management Home**.

2.  Select **Allocate sandbox**.

    \[Omitted image "dev-sbx-home-allocate-btn.png"\] Alt text: Allocate sandbox button on the home dashboard

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Allocate to|User that owns the sandbox.|
    |Sandbox alias|Name that's used to identify the sandbox, for example, in the sandbox management table. The name is configurable, but you can't change the URL.|

    \[Omitted image "dev-sbx-allocate-modal.png"\] Alt text: Fill in the Allocate Sandbox form

4.  Select **Allocate**.

    \[Omitted image "dev-sbx-allocate-requested.png"\] Alt text: Provisioned sandbox initializing


## Result

Developer Sandboxes starts the process of provisioning the sandbox.

**Note:** Sandboxes from the pool are allocated quickly. If the pool is exhausted, it can take between ten minutes and two hours to allocate a sandbox. You can select the refresh icon \[Omitted image "dev-sbx-refresh-icon.png"\] Alt text: to see updates to the Sandboxes list.The record for the sandbox appears in the list as **Initializing** until the sandbox is ready.

Once allocated, developers can access their sandbox by one of two ways:

-   Selecting the sandbox name on the Sandbox Management Home page.
-   Using the context menu and copy the URL to the clipboard and paste it to the browser.

Sandbox users use the same login credentials for their sandbox as the base instance. If you use Single Sign-On \(SSO\), enabling it on the base instance also authenticates Developer Sandboxes \[var.developer-sandboxes-long\] using the same credentials. For information on enabling SSO, see [Installing Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-installing.md).

Two automatically created update set sources enable you to retrieve, preview, and commit completed update sets between the sandbox and base instance using the standard update set process. For more information, see [Update sets transfer between sandboxes and base instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-update-sets.md).

