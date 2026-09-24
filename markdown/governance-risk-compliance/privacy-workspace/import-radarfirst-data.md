---
title: Import RadarFirst data
description: Import jurisdictions, risk factors, and data elements from RadarFirst to map them to the breach assessment data in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/import-radarfirst-data.html
release: brazil
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [RadarFirst, import, data elements, breach factors]
breadcrumb: [RadarFirst configuration, Integrate with RadarFirst, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Import RadarFirst data

Import jurisdictions, risk factors, and data elements from RadarFirst to map them to the breach assessment data in your instance.

## Before you begin

Role required: sn\_privacy.admin

Ensure that a connection with RadarFirst was established and validated. See [Set up the RadarFirst connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-workspace/set-up-radarfirst-connection.md).

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Integration Guided Setup**.

2.  On the Welcome to Guided Setup landing page, select **Continue**.

3.  Select **Start** on the **Import RadarFirst Data** step of the guided setup.

4.  Complete the Initial data setup activity.

    1.  On the **RadarFirst configuration** record, select the **Active** option.

        **Note:** Alternatively, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration**, and select **RadarFirst Configuration**. The same **RadarFirst configuration** record appears where you can complete this activity of the guided setup.

    2.  To import the RadarFirst data, select **Initiate data setup**.

        The **Observations** field displays the data collection status of the imported data. \[Omitted image "pcm-rf-import-status.png"\] Alt text: Observations field displaying the import status of risk factors, data elements, and jurisdictions-related data from RadarFirst.

    3.  Select **Mark as complete**.

5.  On the Create regions and jurisdictions activity, create regions and jurisdictions in your instance that can be mapped to the regions and jurisdictions imported from RadarFirst.

    -   To refer to the regions configured in your instance, navigate to **All** &gt; **Privacy Case Management** &gt; **Breach Assessment Configuration** &gt; **Regions**. To add a region, see [Create a region](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-workspace/create-a-region.md).
    -   To refer to the regions imported from RadarFirst, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Regions**.
    -   To refer to the jurisdictions imported from RadarFirst, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Jurisdictions**.
    1.  After the locations configured in your instance match those of RadarFirst, select **Mark as complete**.


## What to do next

After you have imported RadarFirst data into your instance, it must be mapped to the breach assessment data in Privacy Case Management.

-   To map RadarFirst regions and jurisdictions to those configured in your instance, see [Map regions and jurisdictions to RadarFirst regions and jurisdictions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-workspace/map-regions-to-rf.md).
-   To map RadarFirst data elements and risk factors to the data elements and breach factors in your instance, see [Map breach assessment data to RadarFirst data elements and risk factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/privacy-workspace/initiate-data-mapping-rf.md).

