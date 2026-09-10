---
title: Recommended Actions for ITSM Workflow
description: Configure AI-driven recommendations for ITSM records by creating contexts, setting rules, and defining resource generators with action types. Use this workflow to enable guidance-based and field-level recommendations in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-operations-workspace/sow-itsm-ra-workflow.html
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 2
keywords: [Recommended Actions for ITSM, Service Operations Workspace, resource generator, action types, guidance-based recommendations, field recommendations, Predictive Intelligence, Task Intelligence for ITSM, incident recommendations, problem recommendations, change request recommendations, machine learning solutions, recommendation workflow]
breadcrumb: [Configuring Recommended Actions for ITSM, Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Recommended Actions for ITSM Workflow

Configure AI-driven recommendations for ITSM records by creating contexts, setting rules, and defining resource generators with action types. Use this workflow to enable guidance-based and field-level recommendations in Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

The workflow for Recommended Actions for ITSM includes the following:

## Procedure

1.  Create or use a context.

    1.  Use any of the following contexts to find and use the recommendations in Service Operations Workspace.

        -   Incident
        -   Incident task
        -   Problem
        -   Problem task
        -   Change request
        -   Change task
        -   Interaction
        -   Request
        **Note:**

        -   For more information about contexts, see [Contexts in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/contexts-in-recommended-actions-for-itsm.md).
        -   For incidents, you can use guidance-based recommendations in the **Recommended actions** sub- tab or manually search for AI-driven recommendations in the **Search** sub-tab. For more information about guidance-based recommendations, see [Guidance based recommendations in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/guidance-based-recommendations-in-recommended-actions-for-itsm.md).
2.  Set rules.

    1.  Configure the recommendations for required roles and conditions.

3.  Create recommendations where you select a resource generator and action types.

    1.  Create Resource Generator.

        Resource generators provide information that you can use as inputs to actions such as recommendation guidance and field recommendations. The trained machine learning solution models configured in Predictive Intelligence or Task Intelligence for ITSM are used as solutions in the generator type to get the required recommendations for the incident forms in Service Operations Workspace.

        **Note:**

        -   The **Incident Fields value prediction \(TI\)** and **Similar Incidents \(TI\)** are the only recommendations where the trained models come from Task Intelligence for ITSM. For more information, see [Task Intelligence for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-intelligence-for-itsm/c-itsm-task-intelligence.md).

        -   All remaining recommendations use the trained model from Predictive Intelligence. For more information, see [Predictive Intelligence for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/predictive-intelligence-for-incident.md).

    2.  Create Action type.

        Configure the actions that an agent can perform for Recommended Actions guidance. Update the following:

        -   Input: Select the input fields.
        -   Output: Select the options to decide how the recommendations should look in the input fields.
        -   Action: Select the actions that are presented to the agent to perform the guidance.
        **Note:** For more information, see [Configuring Recommended Actions for ITSM in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/configuring-recommended-actions-for-itsm-in-service-operations-workspace.md).


## Result

Get guidance-based or field-level recommendations for records in Service Operations Workspace. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/recommended-actions-for-itsm-in-service-operations-workspace.md).

**Parent Topic:**[Configuring Recommended Actions for ITSM in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/configuring-recommended-actions-for-itsm-in-service-operations-workspace.md)

