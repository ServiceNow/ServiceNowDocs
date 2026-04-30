---
title: Security Best Practices
description: Use Security Best Practices to implement privacy and security configuration tasks on your ServiceNow instance.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Security posture console, Security Center, Platform Security]
---

# Security Best Practices

Use Security Best Practices to implement privacy and security configuration tasks on your ServiceNow instance.

Identify best practices to improve your security posture, and follow step-by-step instructions on how to implement them. Security Best Practices provide the following:

-   The home page shows an overview of your progress on implementing security best practices. You can also organize and manage lists of security best practices according to your organization's goals.
-   The overview page provides details of each security best practice, the steps to implement them, and a record of all activities and comments.
-   The task steps page provides you with instructions on how to implement security best practices.
-   The activity page tracks the history of the user and system actions related to your security best practices.

## Security Best Practices home page

![Best practices overview](../images/best-practices-1.png)

The home page displays a **Manage your best practices** section, which includes graphs provide an overview of your progress.

-   **Completed overall**

    Displays a count and trend line of best practices you have completed. Select the card to view the **Completed Overall** metric page in [Security metrics](sc-metrics.md).

-   **Completed by maturity level**

    Displays a chart of completed best practices organized by maturity level \(see a description of maturity levels in the proceeding table\). Select the card to view the **Completed by Maturity Level** metric page in [Security metrics](sc-metrics.md).

-   **Build a foundation**

    Select the **Build a foundation** button to filter the table on this page to display only best practices in the **Build a foundation** maturity level. These are lower impact changes you can make to start improving instance security.

-   **Create a task**

    Use the **+Create task** button to create a Security Task to track or delegate best practice work. For details on Security Tasks, see [Security Tasks](security-task-manager.md).


The table enables you to apply filters so that you can sort and save filtered lists, which you can use as work lists for different use cases or roles. See [save a filtered list](../task/apply-filters-to-the-security-best-practices-table.md#) for more information.

The following are explanations of the fields related to the security best practices table.

<table id="table_ktk_yh2_fbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Word used to identify a security best practice.

</td></tr><tr><td>

Maturity level

</td><td>

Applications and features that have been arranged by the order of impact to provide you measurable results. The values for maturity levels are:-   Build a foundation
-   Enhance the experience
-   Optimize the functionality
-   Add advanced features

These can also be thought of as crawl, walk, run, and fly phases.

</td></tr><tr><td>

Status

</td><td>

Current state of a best practice: -   Open
-   In progress
-   Completed

</td></tr><tr><td>

Priority

</td><td>

Order of importance for implementing a best practice in your organization: -   Immediate
-   Later
-   Not applicable

</td></tr><tr><td>

Goals

</td><td>

Security category that a best practice addresses: -   Address initial security configurations
-   Secure emails
-   Monitoring logs
-   Manage access controls
-   Protect with encryption
-   Keep instances up to date

</td></tr><tr><td>

First introduced

</td><td>

Which Security Center version the best practice was introduced.

</td></tr><tr><td>

Changed

</td><td>

Which Security Center version the best practice was changed.

</td></tr><tr><td>

Removed

</td><td>

Which Security Center version the best practice was removed.

</td></tr></tbody>
</table>## Security Best Practices details page

![Best practice details page](../images/best-practices-2.png)

Select a best practice from the table to view its page. At the top of the details page, you can view general information about the security best practice including priority, maturity level, and status. Use **Complete Best Practice** button to mark a the practice as complete, or **Reopen Best Practice** button to mark the practice complete. Use the **+Create Task** to create a Security Task to track and delegate this task. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

This page provides more information on the best practice, divided into tabs:

-   **Overview**

    This tab contains the **Priority** drop-down menu, which enables you to specify the security best practices that are important to you at this time and which are not applicable.

    The details section provides content about the features associated with the security best practice, and the documentation section provides one or more links where you can find additional information.

    The **Progress** card on the right shows the number of steps completed versus the total number of steps included. Select **go to next step** to navigate to the next incomplete step.

    The **best practice update history** card provides a snapshot of the release information for the best practice. You can track which ServiceNow Security Center version the security best practice was released in, and which versions it was subsequently last updated in.

-   **Task Steps**

    This tab provides step-by-step instructions for how to implement this security best practice. See [complete a security best practice](../task/complete-a-security-best-practice-on-your-servicenow-instance.md) for more information.

-   **Activity**

    This tabe displays timestamped activities listed from newest to oldest. Use search and filter to query for information. See [apply filters to the security best practices table](../task/apply-filters-to-the-security-best-practices-table.md#) for more information.


-   **[Complete a security best practice](../task/complete-a-security-best-practice-on-your-servicenow-instance.md)**  
Learn how to complete a security best practice on your ServiceNow instance.
-   **[View activity of a best practice](../task/view-activity-of-a-best-practice.md)**  
Track the chronological and timestamped history related to a security best practice that you're completing on your ServiceNow instance, along with the user that initiated the activity.
-   **[View data of completed best practices](../task/view-statistics-of-completed-best-practices.md)**  
See visual representations of the total amount of best practices completed, or segmented by maturity level.
-   **[Filters the security best practices table](../task/apply-filters-to-the-security-best-practices-table.md#)**  
Apply filters to return more relevant results for your security best practices.
-   **[Best Practices](../reference/best-practices.md)**  
Learn details about the Best Practices in the Security Posture Console.

**Parent Topic:**[Security posture console](sc-posture-console.md)

