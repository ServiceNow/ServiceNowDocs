---
title: Activate ServiceNow Otto for Employee Experience skills
description: Activate ServiceNow Otto for Employee Experience skills to enable AI-powered summarization and assistance capabilities for employee requests, cases, and approval workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/activate-now-assist-skills-uex.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 2
keywords: [generative AI for Employee Center, generative AI for UEX, configuration]
breadcrumb: [Explore, ServiceNow Otto for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Activate ServiceNow Otto for Employee Experience skills

Activate ServiceNow Otto for Employee Experience skills to enable AI-powered summarization and assistance capabilities for employee requests, cases, and approval workflows.

## Before you begin

Before activating the ServiceNow Otto for Employee Experience skills, you must install the following plugins:

-   ServiceNow Otto for Employee Experience
-   ServiceNow Otto for HR Service Delivery \(HRSD\) — required for the Case summarization for approvals skill
-   ServiceNow Otto for IT Service Management \(ITSM\) — required for the Request summarization for approvals and Requested Item summarization for approvals skills

Role required: admin

## About this task

Activate the ServiceNow Otto for Employee Experience plugin to enable generative AI on your instance.

-   Admins can select the roles for whom the skill is available.
-   When you don't have the required role to read the record, you can't see the skill summary.
-   When you activate the skill, you can see the skill or summary.
-   The OOB Applicability record includes a filter for the Employee Center portal. To display a summary on any portal, add an applicability record for that portal. The filter format is `{"URL Suffix of portal" + table : <tableName>}`.
-   By default, the availability filter isn't available. Any changes or customization can affect the availability of the summary widget.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

    If you're already in the AI Admin Hub console, select the **AI Skills** tab.

2.  On the navigation panel, select **Employee** &gt; ****Employee Center to review the skill set.

    Toggle between the list and grid layouts for optimum viewing experience.

    **Note:** All three approval summarization skills appear only if ServiceNow Otto for HR Service Delivery \(HRSD\) and ServiceNow Otto for Employee Experience are installed. If either plugin is missing, the corresponding skills will not be present in the list.

3.  Verify and use the out-of-box settings in **General details**, **Choose input**, and so on.

    Use the options in the default setup for the most common use cases.

    -   Select the step in the guided setup navigation.
    -   Return to a previous step by selecting **Back**.
    -   Select **Save and continue** to go to the next step.
4.  [Clone a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-and-edit-servicenow-skill.md).

5.  Go to **Define Trigger** and select one of the following triggers.

    -   Automatic \(Default\) - Generates auto-summarization for the request, requested item, or case for approval task.
    -   Manual - Requires user to trigger summarization for the request, requested item, or case for approval task.
6.  Choose where to display generative AI skills.

    For ServiceNow Otto for Employee Experience, use **In-product desktop**.

7.  Review your choices and complete the configuration by selecting **Activate**.

8.  Select **Activate skill**.

    On activation of the skill, the skill state changes to active.


## Result

On successful configuration, approval users can see summarization for approvals. For more information, see [View summarization for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/view-summarization-approvals.md).

**Note:** After installing ServiceNow Otto for Employee Experience \[sn\_ex\_gen\_ai\] plugin and activating the skills in the AI Admin Center, the Summary appears in Approvals on Employee Center and service portals. To enable the summary on the custom portals, follow the instructions available in [KB2739995](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2739995) and update the `sn_nowassist_skill_config` table.

**Parent Topic:**[Explore ServiceNow Otto for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/explore-now-assist-for-emp-exp.md)

**Related topics**  


[Supporting information for ServiceNow Otto for Employee Experience]()

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

