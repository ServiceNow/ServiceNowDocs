---
title: Add outside counsel details
description: Add outside counsel details for an outside firm to enable matter creation in Legal Tracker.
locale: en-US
release: xanadu
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure data to enable matter creation in Legal Tracker, Configure Legal Matter Management to engage with outside counsel using Legal Tracker, Setting up Legal Matter Management, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Add outside counsel details

Add outside counsel details for an outside firm to enable matter creation in Legal Tracker.

## Before you begin

Verify the schedule job **Fetch Firms Data** has been executed once before you add the outside counsel details for an outside firm.

Role required: sn\_lg\_matter.matter\_config, sn\_lg\_matter.matter\_fulfiller

## About this task

To create a matter in Legal Tracker, the information related to an outside firm and its outside counsels should be present in both Legal Tracker and Legal Matter Management.

The scheduled job **Fetch Firms Data** pulls the data for outside firms from Legal Tracker into Legal Matter Management, but there is no scheduled job to pull the name and email of the outside counsels. For enabling matter creation, manually add the outside counsel name and email for the outside firm in Legal Matter Management.

## Procedure

1.  Collect the outside counsel name and email address for the outside firm from Legal Tracker.

2.  Open the outside counsels list.

<table id="choicetable_urg_zmd_jzb"><thead><tr><th align="left" id="d138803e99">

Location

</th><th align="left" id="d138803e102">

Actions

</th></tr></thead><tbody><tr><td id="d138803e108">

**From the Legal Matter module**

</td><td>

Navigate to **All** &gt; **Legal Matter** &gt; **Outside Counsel Setup** &gt; **Setup Outside Counsels**.

</td></tr><tr><td id="d138803e135">

**From Legal Counsel Center**

</td><td>

1.  Navigate to **All** &gt; **Legal Counsel Center**.
2.  Select the List icon \(![List icon](../../ohs-incident-management/image/list-icon-hs.png)\) from the primary navigation and in the Outside Counsel section of the **Lists** menu, select **All**.


</td></tr></tbody>
</table>3.  Select the outside counsel for which you want to add the details.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Outside Firm|This field is automatically set to the outside firm name.|
    |Outside Counsel Name|Name of the outside counsel.|
    |Outside Counsel Email|Email address of the outside counsel.|
    |Active|Option to make the Outside Counsel record active.|

5.  Save the Outside Counsel record.

    -   If you have added details from the Legal Matter module, select **Update**.
    -   If you have added details from the Legal Counsel Center, select **Save**.

**Parent Topic:**[Configure data to enable matter creation in Legal Tracker](lmm-config-data-mtemplates.md)

