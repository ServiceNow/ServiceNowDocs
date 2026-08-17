---
title: Set up the HAM advisor dashboard manually
description: If the HAM advisor dashboard was not configured automatically, set it up manually by selecting the model categories that define the HAM scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-manual-setup.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 2
keywords: [manual dashboard setup, select model categories, HAM scope configuration, Select model categories dialog box, opt in resource categories]
breadcrumb: [Get started with dashboard setup, Set up advisor, Use HAM advisor, Asset and CI management, Explore, Hardware Asset Management, IT Asset Management]
---

# Set up the HAM advisor dashboard manually

If the HAM advisor dashboard was not configured automatically, set it up manually by selecting the model categories that define the HAM scope.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  On the CMDB success advisor landing page, select **Select model categories** within the HAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/cmdb-sa-landing-page.md).

2.  On the Select model categories dialog box, select a resource category to choose all its model categories or expand a resource category to select individual categories, then move them from the **Available resource and model categories** column to the **Selected** column.

    **Note:** If the Select model categories dialog box shows **No model categories available**, select **Opt in categories** to opt in at least one HAM license resource category, then return to this step.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add an available resource category|Select the check box for the resource category to include all its model categories.|Includes all model categories associated with the selected resource category.|
    |Expand model category selection|Select **&gt;** to expand a resource category, then select check boxes for specific model categories.|Includes only the selected model categories associated with a resource category.|
    |Narrow down model category selection|Select **&gt;** to expand a resource category, then clear check boxes for specific model categories.|Excludes only the model categories cleared from a resource category.|
    |Remove an opted-out or available resource category|Clear the check box for the resource category.|Excludes all model categories associated with the removed resource category.|
    |Remove a selected model category|Select the X icon next to the category in the **Selected** column or clear the check box for the category|Model category is removed from scope.|

    **Tip:** You can use the **Search** field to find specific categories. You can select up to 200 model categories.

3.  Select **Done** to build the CMDB success advisor for HAM dashboard.


## Result

The HAM data collection begins immediately via the **CMDB Advisor - HAM Daily Data Collection** scheduled job. The HAM advisor dashboard is populated after data collection completes. The scheduled job then continues running on a daily basis.

Until this initial data collection completes, dashboard cards indicate that no data is available and let you refresh to check again.

After manual setup, once initial data collection completes, you receive a notification indicating that insights for the selected model categories are ready for review.

To update the scope after initial setup, select **Edit dashboard scope** on the HAM advisor dashboard.

