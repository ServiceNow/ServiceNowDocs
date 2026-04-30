---
title: Configure Needs attention panels in Digital Portfolio Management
description: Each solution page in Digital Portfolio Management \(DPM\) has a Needs attention panel with items that need attention in the context of the page. You can configure the Needs attention attributes to meet your organization's needs.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure Needs attention panels in Digital Portfolio Management

Each solution page in Digital Portfolio Management \(DPM\) has a Needs attention panel with items that need attention in the context of the page. You can configure the Needs attention attributes to meet your organization's needs.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

Configurable Needs attention panels and its attributes table were introduced in the Utah Store release, November 2023. The following are general guidelines but for more Admin configuration steps, see [KB1519343](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1519343).

Default thresholds apply to the DPM Workspace homepage. Solutions use the default attributes and thresholds from the attributes table until users decide to personalize their DPM Workspace homepage experience. See [Personalize the Digital Portfolio Management Workspace homepage](dpm-personalize-homepage.md).

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **Needs attention** &gt; **Needs attention attributes**.

    The Needs attention attributes display in a table — Critical incidents, Outages, Changes, Alerts, Risks, Audits, and Critical problems.

    **Note:** To see Critical problems in the Needs attention panel, you must be using the DPM August 2024 release or a later release.

2.  Use the Personalize List icon \(![Personalize List icon.](../../../common/image/gear.png)\) to add the following column fields to the table.

    -   Name
    -   Description
    -   Solution type
    -   Order
    -   Active
    -   Show on homepage
    -   Show on needs attention
    -   Threshold for moderate
    -   Threshold for severe
3.  Update the field settings.

<table id="table_djr_spt_d1c"><thead><tr><th>

Column field

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Order

</td><td>

-   The order of the attributes on the user's homepage solution cards.
-   The order of the attributes when the user personalizes the **Edit status conditions** on the homepage.

**Note:** When editing the status conditions, the first four attributes of each type display. You can select the drop-down list to select different status conditions.

</td></tr><tr><td>

-   Active
-   Show on homepage
-   Show on needs attention


</td><td>

Set to true or false. If set to true, then the logged-in user can choose to show the attribute on their homepage solution cards and then personalize the thresholds for that attribute.

</td></tr><tr><td>

-   Threshold for moderate
-   Threshold for severe


</td><td>

Change the number from the default threshold to the threshold that you want to set for each attribute.

 **Note:** If a threshold is set to zero \(0\), then that attribute field is empty.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Digital Portfolio Management](../concept/dpm-configure-cfw.md)

**Related topics**  


[Work with Needs attention panels in Digital Portfolio Management](../concept/dpm-needs-attn-panels.md)

