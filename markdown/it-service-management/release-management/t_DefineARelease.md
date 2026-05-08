---
title: Define a release in Release Management
description: During the release planning process, release managers define the type of the release \(major, minor, and so on.\), schedule of the release \(planned start and end dates\), required phase, phase tasks, and the scope.
locale: en-US
release: australia
product: Release Management
classification: release-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Release Management v2, Release Management, IT Service Management]
---

# Define a release in Release Management

During the release planning process, release managers define the type of the release \(major, minor, and so on.\), schedule of the release \(planned start and end dates\), required phase, phase tasks, and the scope.

## Before you begin

Role required: release\_v2\_admin

## Procedure

1.  Navigate to **All** &gt; **Release** &gt; **Products**.

2.  Open the product to which you want to add a release.

    If a release belongs to no product or more than one product, you can directly navigate to **Release** &gt; **Releases** to define the release. You need not define a release in the context of a product.

3.  In the **Releases** related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_klk_nvr_pjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated unique identifier for the release.

</td></tr><tr><td>

Release Type

</td><td>

Type of the release such as Major, Minor, Upgrade, Patch, or others.

</td></tr><tr><td>

Priority

</td><td>

Priority of the release such as Critical, High, Moderate, or others.

</td></tr><tr><td>

State

</td><td>

State of the release such as Draft, Work in progress, testing, or others.If you want to customize the options in this list, reach out to your admin. Custom states can be added according to the default state categories of the release table. [Learn more about the default states of the release table.](../reference/default-state-categories-for-release-and-release-task-tables.md)

</td></tr><tr><td>

Percent complete

</td><td>

Progress of the release as a percentage of the whole.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the release. This description helps in identifying this release from a list of releases.

</td></tr><tr><td>

Description

</td><td>

Details of the release.

</td></tr><tr><td>

Planned start date

</td><td>

Tentative start date of the release.

</td></tr><tr><td>

Planned end date

</td><td>

Tentative end date of the release.

</td></tr><tr><td>

Planned duration

</td><td>

Duration of the release in days. When you submit the form, this field auto-populates based on the values of Planned start date and Planned end date.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   Attach documents such as release and deployment plans, installation manuals, and training documentation to a release.

    For more information, see Add and manage attachments.

-   Releases can have child releases. So, you can group minor releases under major releases.

    Add a child release by clicking **New** in the Releases related list in the Release form.

-   [Define a release phase in Release Management](t_DefineAReleasePhase.md).
-   [Define scope of a release in Release Management](t_ScopeARelease.md).

**Parent Topic:**[Using Release Management v2](../concept/c_Release.md)

