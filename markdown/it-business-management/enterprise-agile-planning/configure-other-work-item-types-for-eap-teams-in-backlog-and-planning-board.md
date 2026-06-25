---
title: Configure display of other work item types in EAP Backlog and Planning board
description: Enable viewing different work item types in the Backlog and Planning board pages for EAP teams such as Portfolio, Solution Train, Agile Release Train, or Agile Team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/configure-other-work-item-types-for-eap-teams-in-backlog-and-planning-board.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure display of other work item types in EAP Backlog and Planning board

Enable viewing different work item types in the Backlog and Planning board pages for EAP teams such as Portfolio, Solution Train, Agile Release Train, or Agile Team.

## Before you begin

Ensure that you set the **Application Scope** in your instance to **Strategic Planning**.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

The Planning board for an EAP team shows only those work items that are enabled in its default configuration. For example, for a Solution Train with Full Configuration, the Backlog and Planning board show only Capabilities by default. If your product managers or team members want to switch between viewing other work item types such as Features, Epics, or Stories, you can enable it by updating the team-level configuration details.

This task provides guidance on updating the **Planning work types** or **Backlog work types** fields for your Agile teams in the Enterprise agile configuration details table \[sn\_apw\_advanced\_eap\_configuration\_detail\].

## Procedure

1.  Navigate to **All** &gt; **Enterprise Agile Planning** &gt; **EAP Configurations**.

2.  Select a configuration that you need to update the work item type selections for.

    s\[Omitted image "eap-team-level-config-01.jpg"\] Alt text: List of Enterprise agile configurations.

3.  In the Enterprise agile configuration details related list, select the team level that you want to update.

    \[Omitted image "eap-team-level-config-02.jpg"\] Alt text: Enterprise agile configuration form for Full Configuration highlighting the Enterprise agile configuration details related list.

4.  Update the work types in the following fields.

    -   **Backlog work types** to enable viewing multiple work item types in the Backlog page.
    -   **Planning work types** to enable viewing multiple work item types in the Planning board page.
    \[Omitted image "eap-team-level-config-03.jpg"\] Alt text: Enterprise agile configuration detail form highlighting the Backlog work types and Planning work types fields.

5.  Select **Update** to save your changes to the form.

6.  Repeat steps 3-5 to enable multiple work types for other team levels.


**Related topics**  


[Manage team backlog in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/using-eap.md)

[Perform PI planning in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/pi-planning-eap.md)

