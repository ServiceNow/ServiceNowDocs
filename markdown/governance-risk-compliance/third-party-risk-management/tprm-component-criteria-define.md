---
title: Define component criteria
description: Components are the entities for which you can assess risk \(for example, subsidiaries or engagements\). A component criteria is a group of components that should apply to a particular type of third party or engagement.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Define component criteria

Components are the entities for which you can assess risk \(for example, subsidiaries or engagements\). A component criteria is a group of components that should apply to a particular type of third party or engagement.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

Components are the entities for which you can assess risk. The base system comes with the following types of components:

-   Third-party components
    -   Third-party risk assessments \(External risk assessments\)
    -   Subsidiaries
    -   Engagements
    -   Risk intelligence rating
-   Engagement components
    -   Engagement risk assessments
    -   Product
    -   Principal
    -   Facility
    -   Other

You can view the third party or engagement components by navigating to **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Third-party Components** or **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Engagement Components**.

**Note:** You can’t add new components or modify existing ones. You can, however, define the criteria \(in terms of scoring method and weight\) to be used to assess the components. You can update the **Default scoring method** to specify how multiple scores for each risk area are calculated. You can use the **Default weight** to adjust the weight of third-party provider scores in the third party's overall risk rating.

## Procedure

1.  Navigate to **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Third-party Component Criteria** or **Third-party Risk Management** &gt; **Scoring Setup** &gt; **Engagement Component Criteria**.

2.  Select the **Default** entry to open the default criteria.

    ![Component criteria — default record.](../image/component-criteria-default.png)

3.  Based on the amount of emphasis your company places on each of the component types, open each component and assign a weight.

    For example, you could create component criteria for all IT third parties that care most about third-party risk assessments, as follows:

    |Component|Weight|
    |---------|------|
    |Subsidiaries|5|
    |Engagements|5|
    |External Risk Assessments|90|

4.  When you have finished assigning weights, select **Update**.


