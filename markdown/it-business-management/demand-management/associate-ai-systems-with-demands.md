---
title: Associate AI systems with demands
description: Add and manage AI system associations directly from the AI Associations tab in Demand Management.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Associate AI systems with demands

Add and manage AI system associations directly from the **AI Associations** tab in Demand Management.

## Before you begin

-   The AI Control Tower plugin must be installed. For more information, see [Activation and installation of AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/activation-and-installation-of-ai-control-tower.md).
-   The investment type of the demand is set to artificial intelligence.
-   Role required: it\_demand\_user, it\_demand\_manager

## About this task

Add and manage AI system associations directly from the AI Associations tab in a demand form.

You can select the impacted AI systems for the demand. If the required AI systems aren’t available, you can create AI systems using the **Create AI System** related link directly within the demand workflow. You’re navigated to the AI Control Tower to create the AI system. The created AI system is then available for selection in the **Impacted AI Systems** list on the demand form.

## Procedure

1.  Access the demand form in one of the following ways.

    -   Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **Create New**.
    -   Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All** and select a demand.
2.  Navigate to the **AI Associations** section of the demand form and fill in the fields.![AI Associations tab in a demand form.](../image/ai-associations-classic-dmn.png)

    |Field|Description|
    |-----|-----------|
    |Product|Product or system that the demand relates to.|
    |Impacted AI systems|Impacted AI systems associated with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.|

3.  Save the demand by selecting **Save**.

4.  Select the **Create AI System** related link to create an AI system in the AI Control Tower.

    **Note:** This related link is available for users with the sn\_ai\_steward role.

    For more information on creating AI systems, see [Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-ai-system-assets.md).


**Parent Topic:**[Use Demand Management](../reference/r_UsingDemandManagement.md)

**Related topics**  


[Assess demands](../concept/c_AssessingDemands.md)

[Create a demand](t_CreatingDemands.md)

[View demands](t_ViewDemands.md)

[Add details to demands](../concept/c_EnhancingDemands.md)

[RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records for a demand](../concept/ridac-entries-for-demand.md)

[Reset a demand to Draft state](reset-demand-to-draft-state.md)

[Delete demands](t_DeletingDemands.md)

[Move and resize a demand](t_MoveAndResizeADemand.md)

[Train the similarity solution for Demand Management to find similar demands](train-similarity-solution-dm.md)

[PPM PIWB template - Find similar demands](../../itbm-PI-workbench/task/ppm-piwb-demand.md)

[Identify similar records using Now Assist for Strategic Portfolio Management \(SPM\)](identify-similar-demands.md)

[Summarize demands with demand summarization skill](demand-summary-demand-classic.md)

