---
title: Customer Actions
description: Use the Customer Actions tool to implement important security updates based on your instance and the configuration of plugins.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security configuration console, Security Center, Platform Security]
---

# Customer Actions

Use the Customer Actions tool to implement important security updates based on your instance and the configuration of plugins.

![Customer Actions app homepage](../images/critical-updates-homepage.png)

ServiceNow updates your instance with family releases and patches to keep base system platform code and functionality current and secure. However can be additional actions you can take to secure your instance that are unique to your custom instance configuration. These recommended updates are found in the Customer Actions tool.

|Feature|Customer Actions|Family releases and patches|
|-------|----------------|---------------------------|
|Definition|Manual, guided tasks for admins to implement important security changes.|System-driven updates applied automatically during family releases or patches.|
|Purpose|Address security risks that can’t be resolved by ServiceNow upgrades alone. Designed to avoid disrupting custom configurations.|Keep platform code and functionality current and secure.|
|Examples|Deprecating weak certificates, enforcing multi-factor authentication \(MFA\), disabling insecure protocols.|Platform version upgrades, patch-level fixes, backend security enhancements.|

Access this tool by navigating to **Customer Actions** within Security Center.

## Elements of the Customer Actions tool

-   **Create Task button**

    Use the **+Create task** button to create a Security Task to complete a Customer Action. For details, see [Security Tasks](security-task-manager.md).

-   **Overdue actions**

    A count of the number of Customer Actions that are part their due date. Select the overdue actions card to see a list of past due Customer Actions.

-   **Customer Actions timeline**

    A timeline of Customer Actions so that you can prioritize when to implement the steps. The timeline in the preceding image shows the Customer Actions that are overdue, and the ones that are due soon.

-   **Actions tabs**

    A tabbed interface showing Customer Actions by category:

    -   Available
    -   Overdue
    -   Due soon
    -   In progress
    -   Complete
    Select a tab to view a list of actions in each category.


For details on how to review individual Customer Actions, see [View Customer Actions](../task/view-activity-of-critical-updates.md).

For information on how to apply the changes recommended by Customer Actions, see [Implement Customer Actions](../task/implement-steps-for-critical-updates.md).

-   **[Implement Customer Actions](../task/implement-steps-for-critical-updates.md)**  
Learn how to implement Customer Actions on your instance to increase its security posture.
-   **[View Customer Actions](../task/view-activity-of-critical-updates.md)**  
See details of all of the activity related to your Customer Actions.

**Parent Topic:**[Security configuration console](homepage.md)

