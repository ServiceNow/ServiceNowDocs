---
title: Playbook variants
description: Use one playbook for multiple scenarios.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbook variants

Use one playbook for multiple scenarios.

Create different variations on top of a base playbook for multiple use cases instead of duplicating and modifying playbooks, or relying on one-time workarounds that use complex run conditions and branching.

Consider using playbook variants if you have similar business processes that change based on specific factors. For example:

-   Processes and requirements for different locations \(regions, countries, municipalities, organizations, etc.\).
    -   Banking SLAs differ by region, USA is 30 days and EMEA is 45 days with potential for further variation by country.
    -   Card disputes with variance by network: Visa, Mastercard, Discover, etc.
-   Managing hiring flows that vary by industry, department, and job titles.
-   Business processes and requirements for different users and roles.
-   Business processes and requirements for different kinds of applications, such as licenses and permits for different kinds of businesses, etc.

To get started, see [Create a playbook variant](../task/create-playbook-variant.md).

## General Guidelines

Create, run, troubleshoot, and monitor your playbook variants more effectively. Use these guidelines to optimize the performance of your playbook variants.

-   **Evaluate your variants**

    By default, the variants are evaluated at the start of the playbook, from the top down at every level. The first variant that meets the trigger conditions will run. However, you can choose to evaluate the variants after certain activities are complete. You can leverage the output generated in the completed activities to decide which variant to run. This gives you more flexibility in designing the playbook and its variants.

-   **Pay attention to property overrides**

    As you make changes to your variants, related activity configurations that are inherited from parent variants \(such as start rules or display order\) may be overridden. The overridden link and label appear next properties that are no longer synced with the parent variant or playbook.

    ![Overridden start rule activities](../images/overridden-playbook-activity.png)

    Check all properties to ensure they are still configured as you want them. Re-sync properties to be the same as in the parent, if needed.

-   **Don't create variants if you want to change stage properties**

    Stage overrides are not currently supported in playbook variants.


-   **[Create a playbook variant](../task/create-playbook-variant.md)**  
Create variations of a playbook for different use cases.
-   **[Set variant evaluation point](../task/set-evaluation-point.md)**  
Set a point in your base playbook after which the variants are evaluated and run.
-   **[Re-order playbook variants](../task/reorder-playbook-variants.md)**  
Change the order in which playbook variants are evaluated.
-   **[Save a playbook variant as a favorite](../task/bookmark-playbook-variant.md)**  
Save a playbook variant as a favorite for quick reference.

**Parent Topic:**[Understanding the playbook components](playbook-building-blocks.md)

