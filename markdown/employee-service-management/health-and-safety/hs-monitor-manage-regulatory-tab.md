---
title: Monitor and manage the Regulatory list for a chemical substance
description: Use the Regulatory tab on a chemical substance record to quickly assess regulatory conformance status, review regulations, and track upcoming and overdue regulatory obligations.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 2
breadcrumb: [Chemical management, Use, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Monitor and manage the Regulatory list for a chemical substance

Use the Regulatory tab on a chemical substance record to quickly assess regulatory conformance status, review regulations, and track upcoming and overdue regulatory obligations.

## Before you begin

Role required: sn\_hs\_chm.manager

## About this task

The **Regulatory** tab provides a visual summary of a chemical substance’s regulatory conformance status. It displays a timeline of regulatory dates, compliance and overdue metrics, and a grouped list of regulations organized by regulatory list. Regulations fetched from the 3E server are read-only. Regulations created manually are editable.

The regulatory tab shows the conformance status through the regulatory list timeline, compliance, incoming, and overdue cards, and the regulations by regulatory list section.

![regulatory tab in chemical substance record](../image/hs-regulatory-tab-chem-substance.png "Regulatory tab overview")

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select **Environmental Management** \(![environmental management](../../hs-environmental-management/image/icon-hs-envt-mgmt.png)\) icon.

3.  In the **Chemical substance** list, select **All** and then open a record.

4.  Select the **Regulatory** tab.

    The tab displays cards that summarize the current regulatory compliance status.

5.  To retrieve the latest regulatory data from the 3E server, select **Sync Regulatory list**.

    For more information, see [Sync regulatory list regulations for a chemical substance](hs-sync-regulatory-list-chemical-substance.md).

6.  Review the regulatory status and metrics using the following cards:

    |Cards|Description|
    |-----|-----------|
    |Regulatory list timeline|Timeline that displays regulations organized by in-force date, spanning past and future dates. Regulation clusters appear as numbered icons on the timeline.|
    |Compliance|Chart showing the distribution of regulations by compliance status. The number inside the chart shows the total regulation count. Select a segment to drill down to a filtered list of regulations by that status.|
    |Incoming|Count of regulations with an upcoming enforce date that have not yet been reviewed.|
    |Overdue|Count of regulations whose enforce date has passed and that have not been marked as compliant.|
    |Regulations by Regulatory List|Regulations grouped by regulatory list.|

7.  Use the filter and sort controls to refine the regulations displayed.

    |Controls|Description|
    |--------|-----------|
    |Condition filter|One or more conditions to filter the regulations list. It displays the number of active conditions.|
    |Sort by|Regulations list is sorted by the selected field.|
    |Regulatory list|Regulations are grouped or filtered by regulatory list name.|
    |New|Manually add a regulation record.|
    |Refresh|Regulations list is re-queried to display the latest data.|

8.  Select a regulatory list group to expand it and view the individual regulation records it contains.

    The expanded view displays columns like regulatory list, topic, numeric value, phrase text, text value, date value, UOM \(Unit of measurement\), parameter, sub-parameter, scope, country, and region.

9.  Select a regulation record to open it and review the details fetched from 3E.

    A regulation record displays the parameters, thresholds, in-force dates, and authoring information.

10. In the Regulatory list record, set the compliance status in the **Compliance** field.

    When the regulatory list is retrieved from 3E, the **Compliance** field is set to **Non-compliant** by default.


**Parent Topic:**[Chemical management](../../hs-environmental-management/concept/hs-using-chemical-management.md)

