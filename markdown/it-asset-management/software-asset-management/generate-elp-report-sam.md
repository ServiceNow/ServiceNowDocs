---
title: Generate an Effective License Position \(ELP\) report
description: Generate an ELP report to gain detailed insights into the consumption details of different groups within your organization.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Generate an Effective License Position \(ELP\) report

Generate an ELP report to gain detailed insights into the consumption details of different groups within your organization.

## Before you begin

Role required: sam\_user

## About this task

An ELP report groups your data on existing reconciliation groups, by consumption, without having to rerun the reconciliation process.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select **License usage**.

3.  Select **ELP Grouping**.

4.  Select **Create ELP Grouping Report**.

5.  In the Select Grouping Choices box, enter a publisher, product, and group in their respective fields.

    You can optionally also select a subgroup from the **Subgroup** field to further divide your data.

6.  Select **Confirm choices**.

    The results appear in the form of records in the ELP Grouping report results page. Every time you generate a report, a grouping result record gets created.

    At any given time, only one grouping result exists for a particular publisher and product.

7.  Select a record to view the record details page.

    You can view the results for every ELP report that you have run in the **ELP License Position Grouping Reports** tab. Among other details, each record displays the average price, total price, licenses required for each publisher and product, along with the edition and the group value.

8.  Select the display name for a report to view the related list of the consumptions that contributed to the ELP grouping record.

    The Required by device related list shows you a list of devices that require licenses, within the specific category that you selected.

    The following screenshot is an example for Microsoft Office 2016 Professional, where Sales is the selected group. You can view the 29 devices from Sales that require licenses.

    ![Required by device related list](../image/elprelatedlist.png)


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

