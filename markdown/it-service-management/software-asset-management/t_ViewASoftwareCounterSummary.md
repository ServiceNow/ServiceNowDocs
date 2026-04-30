---
title: View software counter summaries for the legacy Software Asset Management plugin
description: Software counter summaries provide information about each software counter type that is supported by the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View software counter summaries for the legacy Software Asset Management plugin

Software counter summaries provide information about each software counter type that is supported by the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## Procedure

1.  On the Software Counter Result form, click a type in the **Summary** related list.

2.  View the Software Counter Summary form \(see table\).

    All fields on the form are read-only.

    ![SAM software counter results](../image/SAMSoftwareCounterResults.png "SAM software counter results")

<table id="table_zrz_xcd_zq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software counter result

</td><td>

Name of the software counter result for which the summary is displayed.

</td></tr><tr><td>

Count as

</td><td>

The software model being counted.

</td></tr><tr><td>

Rights

</td><td>

Number of rights that have been used.

</td></tr><tr><td>

Valuation

</td><td>

How software is counted during the reconciliation process.

</td></tr><tr><td>

Software counter

</td><td>

Name of the software counter.

</td></tr><tr><td>

Summary

</td><td>

Check box that indicates whether the form displays summary information \(selected\) or detailed information \(cleared\).

</td></tr><tr><td>

Type

</td><td>

Type of license counted.

</td></tr><tr><td class="sub-head" colspan="2">

Usage Section

</td></tr><tr><td>

Foreground

</td><td>

Total duration of foreground usage of the software, based on all the installations for the grouping.

</td></tr><tr><td>

Background

</td><td>

Total duration of background usage of the software, based on all the installations for the grouping.

</td></tr><tr><td>

Times used

</td><td>

Total number of times the software was used, based on software usage records for the grouping.

</td></tr><tr><td>

Duration

</td><td>

Total duration of software usage, based on software usage records for the group. \(Not the sum of Foreground and Background.\)

</td></tr><tr><td class="sub-head" colspan="2">

Related List

</td></tr><tr><td>

Software Counter Details

</td><td>

Shows every entitlement, software install, and software usage for the software. The related list also shows the Workstation and User, if applicable, for each software counter detail. A software asset manager can, for example, identify people who are using the license but are not entitled. The software can then be uninstalled from machines that are not in compliance or people can be entitled a license to meet compliance rules.

 Click a type to view the [software counter detail](t_ViewSoftwareCounterDetail.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

