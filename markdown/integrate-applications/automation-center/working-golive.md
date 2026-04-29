---
title: Working with golive checklists
description: Create a golive checklist to automatically track items that must be reviewed before publishing the automation request. Every golive checklist is associated with an automation request.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Working with golive checklists

Create a golive checklist to automatically track items that must be reviewed before publishing the automation request. Every golive checklist is associated with an automation request.

This section has the following subsections:

A checklist template is provided with the product. Here are the details.

<table id="table_xyj_ndt_zfc"><thead><tr><th>

Task name

</th><th>

Task description

</th></tr></thead><tbody><tr><td>

Business/Validation Sign-off

</td><td>

Confirm that the automation meets all business requirements and acceptance criteria. This involves a formal sign-off from the business owner or process SME, ensuring that the automation behaves as expected in staging/sub-production environments.

</td></tr><tr><td>

Development Sign-off

</td><td>

The development team must confirm that all development tasks are complete, including code review, peer review \(if applicable\), and all technical requirements have been implemented. The developer also ensures that environment-specific variables and hard-coded test values have been removed or appropriately managed through config files.

</td></tr><tr><td>

Testing/QE Sign-off

</td><td>

QA must validate that functional, regression, and negative testing is complete in sub-production \(UAT or staging\). A formal sign-off document or ticket must be attached to indicate readiness. Include validation of edge cases and exception scenarios, especially for business-critical automations.

</td></tr><tr><td>

Production Configuration Pre-check

</td><td>

Ensure that all required configuration elements are in place in the production environment:-   Application URLs, credentials, and API endpoints are updated
-   Schedules, triggers, or event rules are properly set
-   Environment variables, secrets, and certificates are configured correctly

</td></tr><tr><td>

Monitoring, Logging &amp; Alerting Setup in Production

</td><td>

Validate that all operational monitoring hooks are active in production:-   Logging destinations \(log servers, dashboards\) are correctly pointed
-   Alerts \(email/SMS/Slack/etc.\) are routed to the correct stakeholders
-   Health checks are enabled, and baseline performance is captured for comparison

</td></tr><tr><td>

Automation Enablement &amp; Final Readiness Review

</td><td>

A final checklist is completed jointly by Dev, QA, CoE, and Business SMEs. This includes:-   Setting the automation to “active/live” in production
-   Verifying all preconditions \(input data, triggers, service availability\)
-   Communicating go-live to impacted teams. This serves as the “green signal” to activate the automation in the production environment.

</td></tr></tbody>
</table>-   **[Create a checklist](../task/create-checklist.md)**  
Create a checklist to track the items for an automation request. A checklist is a list of tasks that you must track before publishing an automation request.
-   **[Edit a task](../task/edit-task.md)**  
Edit a task if you want to update the checklist.
-   **[Clear a checklist](../task/clear-checklist.md)**  
Clear a checklist if you no longer need the checklist for your automation request.
-   **[Create a template](../task/create-template.md)**  
Create a template when you think a golive checklist is useful for multiple automation requests.
-   **[Update a template](../task/update-template.md)**  
Update your template if you have changed the checklist and want those changes to reflect in your template.
-   **[Update task status](../task/update-task-status.md)**  
Update the status of a task so that it’s the latest and helps in the publishing of the automation request.

**Parent Topic:**[Working with automations](automations.md)

