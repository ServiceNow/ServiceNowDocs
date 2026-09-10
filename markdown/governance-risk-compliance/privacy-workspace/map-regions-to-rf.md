---
title: Map regions and jurisdictions to RadarFirst regions and jurisdictions
description: Map the configured breach assessment regions and jurisdictions in your instance to those imported from RadarFirst.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/map-regions-to-rf.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-07-25"
reading_time_minutes: 4
breadcrumb: [Configure, Integrate with RadarFirst, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Map regions and jurisdictions to RadarFirst regions and jurisdictions

Map the configured breach assessment regions and jurisdictions in your instance to those imported from RadarFirst.

## Before you begin

Role required: sn\_privacy.admin or sn\_privacy\_case.privacy\_case\_admin

Import data elements, risk factors, and jurisdictions from RadarFirst. For steps, see .

## About this task

In breach assessment configuration, regions are the top-level locations. Each region contains one or more levels of jurisdictions. For example, `Americas` is a region that contains `North America` as a first-level jurisdiction, which in turn contains `California` as a second-level jurisdiction. However, jurisdictions don't always require multiple levels. For example, `Europe` is a region that contains `Germany` directly as a first-level jurisdiction.

Each jurisdiction has its own set of data elements and breach factors configured for breach assessments. Because breach notification laws vary by jurisdiction, the specific data elements and breach factors that apply to a breach assessment depend on the jurisdictions involved.

To use RadarFirst for risk analysis, each region and jurisdiction in your instance must be mapped to a corresponding record in RadarFirst. This mapping ensures that the data elements and breach factors configured for a jurisdiction in your instance are correctly associated with the equivalent jurisdiction record in RadarFirst.

-   To view the regions and jurisdictions configured in your instance, navigate to **All** &gt; **Privacy Case Management** &gt; **Breach Assessment Configuration** &gt; **Regions**. Each region record lists its first-level jurisdictions in the **Locations** tab. Open a jurisdiction to view any further jurisdictions nested within it. To add a region, see [Create a region](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/create-a-region.md).
-   To view the regions imported from RadarFirst, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Regions**.
-   To view the jurisdictions imported from RadarFirst, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Jurisdictions**.

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **Breach Assessment Configuration** &gt; **Regions**.

    This opens the list of regions configured for breach assessments in your instance.

    **Note:** You may also complete this task as part of the RadarFirst integration guided setup by navigating to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Integration Guided Setup**. Select **Start** the Map RadarFirst Data to Breach Assessment step.

2.  Map the regions in your instance to their corresponding records in RadarFirst.

    1.  Select a region.

        The record displays the jurisdictions configured within it in the **Locations** tab. These jurisdictions have to be mapped to their corresponding records in RadarFirst as well.

    2.  On the Breach Assessment Payload mapping tab of the selected region, select **New**.

    3.  On the form, fill in the fields.

<table id="table_t4j_2mq_1kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Source table**

</td><td>

Location table \(cmn\_location\) that hosts the configured breach assessment regions in your ServiceNow® instance.

</td></tr><tr><td>

**Source record**

</td><td>

Region selected to map to a RadarFirst region. For example, consider`APAC`.

</td></tr><tr><td>

**Provider table**

</td><td>

RadarFirst region table \(sn\_privacy\_rf\_region\) that hosts its location records.

</td></tr><tr><td>

**Provider record**

</td><td>

Corresponding region in RadarFirst that you want to map to the source record chosen.For example, if you chose `APAC` as the source record, search for its corresponding value in the sn\_privacy\_rf\_region table, which might be listed as `APAC` or `Asia Pacific`.

</td></tr></tbody>
</table>    4.  Select the **Active** option.

    5.  Select **Submit**.

        This maps the selected region in your instance to its corresponding RadarFirst region.

3.  Map jurisdictions within the selected region to their corresponding records in RadarFirst.

    1.  Return to the **Locations** tab of the selected region.

    2.  Select a jurisdiction.

    3.  On the Breach Assessment Payload mapping tab of the selected jurisdiction, select **New**.

    4.  On the form, fill in the fields.

<table id="table_n23_vsc_dkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Source table**

</td><td>

Location table \(cmn\_location\) that hosts the configured breach assessment jurisdictions in your ServiceNow® instance.

</td></tr><tr><td>

**Source record**

</td><td>

Jurisdiction selected to map to a RadarFirst jurisdiction. For example, consider that `APAC` has `Japan` as one of its jurisdictions that need to be mapped.

</td></tr><tr><td>

**Provider table**

</td><td>

RadarFirst jurisdiction table \(sn\_privacy\_rf\_jurisdiction\) that hosts its jurisdiction records.

</td></tr><tr><td>

**Provider record**

</td><td>

Corresponding jurisdiction in RadarFirst that you want to map to the source record chosen.For example, if you chose `Japan` as the source record, search for a matching value in the sn\_privacy\_rf\_jurisdiction table.

</td></tr></tbody>
</table>    5.  Select the **Active** option.

    6.  Select **Submit**.

        This maps the selected jurisdiction in your instance to its corresponding RadarFirst jurisdiction.

        **Note:** Each jurisdiction might further have jurisdictions listed within the **Locations** tab. You can map those to their corresponding records in RadarFirst as well.

4.  To map additional regions and their jurisdictions, repeat the previous steps.


## Result

This marks the completion of the Map regions and Map jurisdictions activities of the Map RadarFirst Data to Breach Assessment step of the guided setup. All the configured mappings appear in the **Breach assessment payload mapping** table. To view this table:

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
2.  Search for **Breach assessment payload mapping** by Label.
3.  Open the record and select the **Show List** from the **Related Links** section.

## What to do next

Map the breach assessment data associated with these regions to that of RadarFirst. For steps, see [Map breach assessment data to RadarFirst data elements and risk factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/initiate-data-mapping-rf.md).

