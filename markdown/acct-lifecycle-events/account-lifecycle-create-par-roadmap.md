---
title: Create a product adoption roadmap
description: Create a product adoption roadmap that guides customers through optimal product adoption to achieve maximum business value.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer success, Customer Success Management, Customer Success Management]
---

# Create a product adoption roadmap

Create a product adoption roadmap that guides customers through optimal product adoption to achieve maximum business value.

## Before you begin

-   Product usage or capability records must already exist for the products to be included in the roadmap.
-   To create a roadmap from a template, you must first create a product adoption roadmap template.
-   Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

Use this task to create a visual roadmap that helps you communicate product adoption priorities to your customers. The roadmap organizes products into lanes that reflect their business criticality, implementation timeline, or adoption priority, making it easy to show customers which products to adopt first for maximum business value.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and navigate to the **Success portfolio overview** page.

2.  Select an engagement from the list and navigate to the **Product adoption** tab.

3.  In the Product adoption roadmaps section, select **New product adoption roadmap**.

4.  Enter a name and description from the roadmap and select **Next**.

5.  Select your product adoption implementation strategy:

    -   By product: Organize entire products to create a high-level, strategic adoption plan. Use this as a guideline on how to implement products over time.
    -   By capability: Organize specific capabilities within products for short term, tactical planning. Use this to focus on adopting features and functions.
6.  Specify how the roadmap is to be created:

    -   **From scratch**: Manually configure all roadmap settings and add products or capabilities.
    -   **Template**: Use a pre-configured template that includes lanes, items, and phase field settings. Select a template from the **Template** drop down list and select **Finish**. The roadmap is created based on the pre-configured values defined in the template. See [Create a product adoption roadmap template](account-lifecycle-create-par-roadmap-temp.md) for details.
    -   **Now Assist**: Generate a roadmap using Now Assist. See Generate a product adoption roadmap using Now Assist for Telecommunications, Media and Technology \(TMT\) for details.

        **Note:** The Now Assist option is displayed only if:

        -   The Now Assist for TMT plugin has been installed.
        -   The **Lookup similar engagements** skill has been enabled.
7.  **From scratch**: Select a value from the Phase drop down list and select **Finish** to determine the lane headings for your roadmap.

    -   The values listed in the Phase field are based on the list fields defined in the Product or Capability usage records. A list field has a pre-defined set of choices that are used to create the lane headings in the roadmap. For example, if you select the Business criticality in the Phase field, the lanes will be divided into Critical, High, Medium, Low, and Nice to have.
    -   The roadmap is displayed with lanes based on the Phase field value you selected. All products or capabilities appear in the Unmapped lane.
8.  Drag cards between lanes to organize them according to your adoption strategy and select **Finalize roadmap**.

    **Note:** The roadmap is in Draft state before it is finalized. When the roadmap is in this state, you can do the following:

    -   Select **Cancel** to discard the roadmap without saving it.
    -   Select **Edit name** to modify the name of the roadmap.
9.  After you finalize the roadmap, you can do the following:

    -   Edit: Select **Edit** to move the roadmap to the Draft state to make changes. After making changes, select **Finalize roadmap**.
    -   Sync: Select **Sync** to update the usage records with their roadmap lane values. This updates the Phase field in each product or capability usage record to match its current lane. For example, if the Phase field is **Customer priority** and an item is in the **Critical** lane, the corresponding field is updated to **Critical** in the usage record.
    -   Duplicate: Select **Duplicate map** to make a copy of the roadmap.
    -   Retire: Select **Retire** to archive the roadmap.

**Parent Topic:**[Customer success](../concept/account-lifecycle-config-cust-success.md)

**Related topics**  


[View a product adoption roadmap](../concept/account-lifecycle-view-par-roadmap.md)

[Product adoption roadmap](../concept/account-lifecycle-par-roadmap.md)

