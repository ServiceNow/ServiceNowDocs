---
title: View or create software usage
description: View software usage records to track the usage of software products that you have created reclamation rules for. You can also create software usage records manually from third party integrations or Microsoft SCCM integrations.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View or create software usage

View software usage records to track the usage of software products that you have created reclamation rules for. You can also create software usage records manually from third party integrations or Microsoft SCCM integrations.

## About this task

If you’re using Software Asset Workspace, the option to view or create software usage in Core UI is inactive.

The Software Usage \[samp\_sw\_usage\] table tracks down usage to the product level and not to the version or edition level.

## Before you begin

Role required: sam\_admin or sam\_user

## About this task

Use the following steps to create software usage records manually.

## Procedure

1.  Navigate to the Create New Software Usage form.

    |Interface|Action|
    |---------|------|
    |**Core UI**|Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Software Usage**.|
    |**Software Asset Workspace**|Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Discovery** &gt; **Software usage**.|

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_w2y_w11_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Software usage

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product.

</td></tr><tr><td>

Product

</td><td>

Name of the software product.

</td></tr><tr><td>

Reclamation type

</td><td>

Type of reclamation used on the software installation. The options are **Total Usage Time** and **Last Used Date**.**Note:** If you select **Total Usage Time**, the Usage Metering Data form section appears. If you select **Last Used Date**, the Last Used Data form section appears.

</td></tr><tr><td>

Configuration Item

</td><td>

Configuration item \(CI\) that the software product is associated with. **Note:** If the CI **Status** or **Hardware Status** field changes to Retired or Stolen, installations that are related to the CI are deleted.

</td></tr><tr><td>

User

</td><td>

Name of the user who is using the software product.

</td></tr><tr><td class="sub-head" colspan="2">

Usage Metering Data**Note:** This form section appears only if the **Reclamation type** is set to **Total Usage Time**.

</td></tr><tr><td>

Month

</td><td>

Month that the software product was used.

</td></tr><tr><td>

Year

</td><td>

Year that the software product was used.

</td></tr><tr><td>

Usage count

</td><td>

Number of times that the software product was accessed.

</td></tr><tr><td>

Total seconds used

</td><td>

Amount of time \(in seconds\) that the software product was used.

</td></tr><tr><td class="sub-head" colspan="2">

Last Used Data**Note:** This form section appears only if the **Reclamation type** is set to **Last Used Date**.

</td></tr><tr><td>

Last used time

</td><td>

Date and time that the software product was last used.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

After the software usage is created, you can view it by navigating to **License operations** &gt; **Discovery** &gt; **Software usage**.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

