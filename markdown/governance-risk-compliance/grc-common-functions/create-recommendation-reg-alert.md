---
title: Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies
description: Generate recommendations to identify and mark potential impact areas, such as citations, control objectives, controls, and policies for regulatory alerts using the corresponding regulatory alert impacted skill. Recommendations simplify the process of associating impacts and creating action tasks.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies

Generate recommendations to identify and mark potential impact areas, such as citations, control objectives, controls, and policies for regulatory alerts using the corresponding regulatory alert impacted skill. Recommendations simplify the process of associating impacts and creating action tasks.

## Before you begin

Install the Now Assist for IRM application to generate recommendations. For more information, see [Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/now-assist-for-irm.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

Role required: To view your assigned regulatory alerts, you need the sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user roles.

For more information on related roles and regulatory alerts, see [Types of alerts, user roles, and states of regulatory alerts](../../grc-rcm/reference/user_roles_and_actions.md).

**Important:** Be sure to check AI-generated recommendations for accuracy. If no information is available, the generated recommendations display "No recommendations available", "None", "No records to display", and so on.

## About this task

Starting with version 19.0.x, users who have the Now Assist for IRM application installed can use the regulatory alert summarization, recommend alert impacted citations, and regulatory alert impacted control objectives skills.

To create a recommendation template, you must define a configuration using the recommendation contexts framework, which delivers AI-driven insights directly within the user interface to enhance decision-making and productivity. As part of the base system, a default context named "Suggest business operations affected by regulatory alert" powered by Now Assist for IRM" is included, which you can access from the GRC Administration menu. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).

For more information on activating the Regulatory alert impacted citations, Regulatory alert impacted control objectives, Regulatory alert impacted controls, and Regulatory alert impacted policies skills, refer to [Activate Regulatory alert recommendation skills](configure-recommendation-skill-for-a-regulatory-alert.md).

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select a regulatory alert in any state except Closed or Cancelled that you want to generate recommendations for.

3.  Generate recommendations by completing one of the following:

    -   On the Overview tab, select **Recommend**.
    -   On the Recommendations tab, select **Show recommendations**.
4.  To view the status of the recommendation request, select **View status** or reload the page.

    Recommendation requests are asynchronous enabling you to complete other tasks while the request is processed. You can select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg) to view the latest.

    On the recommendations page, a message indicates the status of your recommendations request.

    -   No data: If there’s no relevant data available, the recommendations page indicates that the request was completed and there are no recommendations currently available.
    -   In progress: If the request is in progress, try reloading the page after some time.
    -   Complete: If the request is completed successfully, the recommendations are displayed and ready for review.

## What to do next

Accept or dismiss the generated recommendations. For more information, see [Accept or dismiss recommendations for regulatory alert impacted citations](manage-recommendation-reg-alert.md), [Accept or dismiss recommendations for regulatory alert impacted control objectives](manage-recommend-co-reg-alert.md), [Accept or dismiss recommendations for regulatory alert impacted controls](manage-recos-for-controls.md), and [Accept or dismiss recommendations for regulatory alert impacted policies](manage-recos-for-policies.md).

**Note:**

You can configure UI form actions in addition to "Accept" and "Dismiss" as declarative actions for recommendations. Declarative actions help you to modify the list actions and related list actions. For more information about creating declarative actions and how to use them, see [Declarative actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/migration-form-declarative-actions.md).

When configuring declarative actions for recommendations, confirm the following:

-   For the UI Action, specify the conditions under which the UI Actions are visible such as roles.
-   For the action type UXF client action, specify the `route` and `size` values in the payload map.
-   For the page event mappings on the recommendation page, the `input` parameter is passed, which includes the following:
    -   `baseTable`
    -   `baseRecord`
    -   `relationshipData`
    -   `selectedCardInfo`

