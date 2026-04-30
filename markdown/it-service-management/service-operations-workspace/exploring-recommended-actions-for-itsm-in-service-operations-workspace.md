---
title: Exploring Recommended Actions for ITSM in Service Operations Workspace
description: Recommended Actions for ITSM lets you set up and apply real-time actionable recommendations for speeding up the triaging process. You can resolve issues quickly across various records in the Service Operations Workspace, including Incident, Incident task, Problem, Problem task, Change request, Change task, Interaction, and Request.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-04-22"
reading_time_minutes: 5
breadcrumb: [Explore, Service Operations Workspace for ITSM, IT Service Management]
---

# Exploring Recommended Actions for ITSM in Service Operations Workspace

Recommended Actions for ITSM lets you set up and apply real-time actionable recommendations for speeding up the triaging process. You can resolve issues quickly across various records in the Service Operations Workspace, including Incident, Incident task, Problem, Problem task, Change request, Change task, Interaction, and Request.

## Recommended Actions for ITSM overview

Recommended Actions for ITSM overview 

There are two ways in which recommendations appear: as actionable real-time recommendations in the side panel or as field-level recommendations while updating or creating the records in Service Operations Workspace.

**Note:** Field level recommendations are available only for Incidents in Service Operations Workspace.

Agents can access recommended actions in Service Operations Workspace by selecting the Recommendations icon \(![Recommended Actions icon.](../image/recommended-actions-icon.png)\) in the side panel. They can also manually search for AI-powered recommendations to quickly find solutions. These search results are available in the following records:

-   Incident
-   Incident task
-   Problem
-   Problem task
-   Change request
-   Change task
-   Interaction
-   Request

For incident records, selecting the Recommendations icon \(![Recommended Actions icon.](../image/recommended-actions-icon.png)\) displays the **Recommended actions** and **Search** sub-tabs, as shown in the following diagram.

![Guided based recommendations for incidents](../image/Guidance_based_recommendations_for_incident.png)

**Note:** The **Search** sub-tab enables you to manually search for AI-powered recommendations.

For other records, selecting the Recommendations icon \(![Recommended Actions icon.](../image/recommended-actions-icon.png)\) displays only the AI-powered search results, as shown in the following diagram.![AI-powered search results](../image/AI-search_powered_recommendations.png)

For more information, see [Get Guidance based recommendations](../task/get-guidance-based-recommendations.md).

Agents can view field-level recommendations in the fields of an incident form in Service Operations Workspace. If you're on version prior to 4.2, the recommendations appeared as messages below the field.

**Note:** Starting from version 4.2, field-level recommendations appearing as messages below the field will no longer be supported to help prevent performance issues.

![Field-level recommendations.](../image/ra-field-recommendation.png)

Starting from the version 4.2, field recommendations appear in a drop-down when you select the field. For more information, see [Get field recommendations](../task/get-field-recommendations.md).

![Field_recommendations_in_drop-down](../image/ra_get_field_recommendations_drop-down.png)

## Request apps on the Store

Visit the  [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do)  website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the  [https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Recommended Actions for ITSM application details

There are two versions of Recommended Actions: Standard and Advanced. For information about installing either, see [Setting up Recommended Actions for ITSM](set-up-ra-itsm.md).

## Recommended Actions for ITSM workflow

The workflow for Recommended Actions for ITSM includes the following:

1.  Use Context: Use any of the following contexts to find and use the recommendations in Service Operations Workspace.

    -   Incident
    -   Incident task
    -   Problem
    -   Problem task
    -   Change request
    -   Change task
    -   Interaction
    -   Request
    **Note:**

    -   For incidents, you can use guidance-based recommendations in the **Recommended actions** sub- tab or manually search for AI-driven recommendations in the **Search** sub-tab.
    -   AI-powered search results are available in the following eight record types: Incident, Incident task, Problem, Problem task, Change request, Change task, Interaction, and Request.
2.  Set Rule: Configure the recommendations for required roles and conditions.
3.  Create Recommendations: Create recommendations where you select a resource generator and action types.

    -   Create Resource Generator: Resource generators provide information that you can use as inputs to actions such as recommendation guidance and field recommendations. The trained machine learning solution models configured in Predictive Intelligence or Task Intelligence for ITSM are used as solutions in the generator type to get the required recommendations for the incident forms in Service Operations Workspace.

        **Note:**

        -   The **Incident Fields value prediction \(TI\)** and **Similar Incidents \(TI\)** are the only recommendations where the trained models come from Task Intelligence for ITSM. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md).

        -   All remaining recommendations use the trained model from Predictive Intelligence. For more information, see [Predictive Intelligence for Incident Management](../../incident-management/concept/predictive-intelligence-for-incident.md).

    -   Create Action type: Configure the actions that an agent can perform for Recommended Actions guidance. Update the following:
        -   Input: Select the input fields.
        -   Output: Select the options to decide how the recommendations should look in the input fields.
        -   Action: Select the actions that are presented to the agent to perform the guidance.
    **Note:** For more information, see [Configuring Recommended Actions for ITSM in Service Operations Workspace](configuring-recommended-actions-for-itsm-in-service-operations-workspace.md).

4.  Get guidance-based or field-level recommendations for records in Service Operations Workspace. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md).

**Parent Topic:**[Exploring Service Operations Workspace for ITSM](explore-sow.md)

**Related topics**  


[Access Service Operations Workspace for ITSM](../task/access-sow-itsm.md)

[Service Operations Workspace for ITSM user interface](service-operations-workspace-ui.md)

[Service Operations Workspace for ITSM for ITSM landing page](sow-ui-landing-page.md)

[Exploring On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)

