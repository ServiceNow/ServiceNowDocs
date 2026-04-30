---
title: Configurable Workspace category
description: Interact directly with the configurable workspace components for simpler test creation.Navigate to a workspace page using a URL. The feature allows for URLs to be entered with or without the preceding domain name.Interact with a seismic component on a workspace page using the Test Page test step.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Configurable Workspace category

Interact directly with the configurable workspace components for simpler test creation.

## Open Workspace Page

Navigate to a workspace page using a URL. The feature allows for URLs to be entered with or without the preceding domain name.

![Screenshot shows the workspace url form](../image/atf-ws-url-form.png)

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

Workspace URL

</td><td>

URL of the workspace page you want to use.**Note:** The URL can be entered with or without the domain, but it will be trimmed upon saving for compatibility between test instances.

</td></tr></tbody>
</table>## Test Page

Interact with a seismic component on a workspace page using the Test Page test step.

Enter the URL of the workspace page you want to inspect for the Configurable Workspace URL field on the Configurable Workspace Test Authoring modal.

![Screenshot shows the test page modal](../image/atf-test-page-modal.png)

**Note:** By default, the URL from the preceding Open Workspace Page test step is displayed. If this step is not immediately preceded by an Open Workspace Page step, you must enter the target workspace page URL manually for inspection.

