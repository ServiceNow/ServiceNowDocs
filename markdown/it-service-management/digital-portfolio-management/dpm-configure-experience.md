---
title: Configure the Digital Portfolio Management experience
description: If your organization doesn't use certain modules or life-cycle phases in Digital Portfolio Management \(DPM\), then configure the experience by hiding those elements from user views.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital Portfolio Management, IT Service Management]
---

# Configure the Digital Portfolio Management experience

If your organization doesn't use certain modules or life-cycle phases in Digital Portfolio Management \(DPM\), then configure the experience by hiding those elements from user views.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

Configure the user experience in the DPM Workspace. You can also configure it using the UI Builder application but there's so much you can do in DPM. As a DPM admin, you can:

-   Hide entire tabs, certain sections of a tab, and solutions types \(for example, business applications\) from user views. After a tab or solution type is hidden, that item is also hidden in searches and filters.
-   Hide available item types — services, technology management services, business services, service instances, service offerings, and business applications.
-   Enable system properties to show:

    -   Standard Needs attention panels.

        **Note:** Standard Needs attention panels are set to true for new customers. Existing customers must enable the system property. For more information, see [Work with Needs attention panels in Digital Portfolio Management](../concept/dpm-needs-attn-panels.md).

    -   Latest \(or last\) key performance indicator \(KPI\) scores. When enabled, KPIs no longer display as a sum or average across a date range. This feature is only available with the Utah release and later.
    -   DevOps data. For more information, see [DevOps value stream metrics in Digital Portfolio Management](../concept/dpm-devops-metrics.md).
    **Note:** You can enable and disable these configurations at any time.


See configuring DPM user views in action.

Configure DPM user views. 

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **Administration**.

2.  Select the menu item that you want to configure for users.

    -   **Service instance properties**
    -   **Business application properties**
    -   **Service and offering properties**
    -   **DevOps properties**
    -   **KPI groups properties** \(option to set the Latest score system property\)
    -   **Available item types** \(go to Step 6\)
3.  If applicable, follow the provided instructions to edit the selected record.

    For some properties, there’s a link for you to select.

4.  Follow the provided instructions to edit each configuration.

5.  Select **Save**.

6.  Hide or show available item types.

    -   Navigate to **All** &gt; **Digital Portfolio Management** &gt; **Administration** &gt; **Available item types**.
    -   Set the item type to `false` \(to hide\) or to `true` \(to show\) in the **Active** column. When a solution type is hidden, that solution is omitted from the following areas:
        -   The auto-generated solution card results.
        -   The personalization options of add and remove items.
        -   The set status conditions when updating thresholds.
        -   The page filters.

**Parent Topic:**[Configuring Digital Portfolio Management](../concept/dpm-configure-cfw.md)

**Related topics**  


[bundle-platux.open-your-configurable-workspace-experience-in-ui-builder]

[bundle-cadev.ui-builder-overview]

