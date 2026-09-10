---
title: Map breach assessment data to RadarFirst data elements and risk factors
description: Map the data elements and breach factors linked to the breach assessment regions in your instance to RadarFirst.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/initiate-data-mapping-rf.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 2
breadcrumb: [Configure, Integrate with RadarFirst, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Map breach assessment data to RadarFirst data elements and risk factors

Map the data elements and breach factors linked to the breach assessment regions in your instance to RadarFirst.

## Before you begin

Role required: sn\_privacy.admin or sn\_privacy\_case.privacy\_case\_admin

Map the regions in your instance with those of RadarFirst to proceed. For steps, see [Map regions and jurisdictions to RadarFirst regions and jurisdictions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/map-regions-to-rf.md).

## About this task

RadarFirst data import brings in data elements and risk factors that you must map to the data elements and breach factors in your instance. During a breach assessment, when a business user creates a PI artifact, they only see the data elements and jurisdictions for the selected region.

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Integration Guided Setup**.

2.  On the Welcome to Guided Setup landing page, select **Continue**.

3.  On the Map RadarFirst Data to Breach Assessment step, navigate to the Initiate and Validate data mapping activity.

    This displays the **RadarFirst configuration** record where the RadarFirst data was imported.

    **Note:** You can also navigate to this record directly from **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Configuration**.

4.  On the RadarFirst configuration record, select **Initiate data mapping**.

    The system automatically maps your breach assessment data to RadarFirst data elements and risk factors. The Observations field displays the mapping status. \[Omitted image "pcm-rf-data-map-stat.png"\] Alt text: Data mapping status showing successfully mapped data elements and breach factors.

    -   The Status changes from **Initiate data mapping** to **Data set up completed**.
    -   No records remain in the **Data Elements** and **Breach Factors** tabs if each record successfully maps to RadarFirst data.

        **Note:** You might have to refresh the list on both tabs for the changes to reflect. Orphaned records that can't be mapped to a corresponding RadarFirst record remain listed in these tabs. You must deactivate these records to successfully complete the RadarFirst integration.

5.  On the Initiate and Validate data mapping activity, select **Mark as complete**.

    This marks the completion of the RadarFirst integration guided setup.

6.  Select **Close**, then select **Complete**.


## Result

With integration complete, a privacy analyst can initiate a RadarFirst analysis on a breach assessment to get a detailed report comprising regional regulatory guidance. For details, see [Perform RadarFirst analysis on a privacy breach assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/submit-breach-review.md).

