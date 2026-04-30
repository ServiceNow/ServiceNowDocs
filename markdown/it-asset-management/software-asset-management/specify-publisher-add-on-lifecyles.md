---
title: Use publisher add-on lifecycles in the Software Lifecycle Report
description: If you purchase an add-on or optional support for a software product, enable the Software Asset Management application to automatically update the life-cycle dates of that product with the extended life-cycle dates of the add-on or optional support. These updated life-cycle dates are populated in the Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Use publisher add-on lifecycles in the Software Lifecycle Report

If you purchase an add-on or optional support for a software product, enable the Software Asset Management application to automatically update the life-cycle dates of that product with the extended life-cycle dates of the add-on or optional support. These updated life-cycle dates are populated in the Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\] table.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  From the Software Asset Workspace, open the License operations view.

3.  From the navigation menu of the License operations view, navigate to **Licensing** &gt; **Publisher Add-On Lifecycles**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_ptp_ttr_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option that indicates if the Software Asset Management application can update the life-cycles dates of the specified software product with the extended life-cycles dates of the add-on or optional support that you have purchased.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the life-cycles dates are updated.

</td></tr><tr><td>

Product

</td><td>

Software product that you want to update the life-cycle dates for.**Note:** If you leave this field empty, the Software Asset Management application updates the life-cycle dates of every product with an add-on or optional support under the specified software publisher.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product that you want to update the life-cycle dates for.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

When the next SAM - Generate Software Lifecycle Report scheduled job runs, the Software Asset Management application uses life-cycle information from the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table to automatically update the life-cycle dates of the specified software product with the extended life-cycle dates of the add-on or optional support that you have purchased.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

