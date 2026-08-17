---
title: Set up the environment to manage approvals
description: Complete the setup tasks before creating approval configurations and workflows. These prerequisites enable the approval system for a CPQ implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/setup-approvals-prerequisites.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 4
keywords: [approvals, setup, prerequisites, configuration]
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up the environment to manage approvals

Complete the setup tasks before creating approval configurations and workflows. These prerequisites enable the approval system for a CPQ implementation.

## Before you begin

Role required: admin or sn\_adv\_appr\_mgmt.approval\_rule\_admin

## About this task

Set up the environment to administer and manage approvals.

## Procedure

1.  Install the required plugins.

    1.  Navigate to **All** &gt; **System Definitions** &gt; **Plugins**.

    2.  Search for and install the following plugins, if not already installed:

        -   Advanced Approvals Plugin: Provides the core approval management framework. For more information, see [Install Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-advanced-approval-management.md)
        -   Quote Management - Advanced \(App id: sn\_quote\_mgmt\_adv\): Required for approving transactions.
    3.  Confirm that all plugins show as active in the Plugins list.

    All required plugins are installed and active in your system.

2.  Enable the approval tenant setting in your microservices instance.

    1.  Contact ServiceNow Customer Support to enable the approval tenant setting for your microservices instance.

    2.  When contacting support, provide the following information:

        -   Your ServiceNow instance name
        -   Request to enable: "Microservices Approval Tenant Setting"
        -   Confirmation that Advanced Approvals and Advanced Code plugins are installed
    3.  Wait for the support team to confirm the setting is active.

    4.  After the setting is enabled, verify that the approval interface and approval-related UI components are visible by navigating to the approval configuration areas.

    The approval tenant setting is enabled in your microservices instance, and the approval system is ready for configuration.

3.  Export and re-import the blueprint to seed approval system fields, events, and integrations.

    1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Blueprint**.

    2.  Select **Export**.

        The export process creates a backup of your current blueprint configuration.

    3.  Navigate to **All** &gt; **CPQ Administration** &gt; **Utilities** &gt; **Matrix Loader**.

    4.  Import the blueprint.

        The components such as system events \(Preview, Request, Approve, Cancel/Reject, View\), integrations \(Data flow integration between your microservices and the approval system\), rules \(Validate Approval Submission, Validate Approval Completion, Validate Approval Revision\), rule groups \(Approval Submission, Approval Completion, and Approval Revision\), and field \(Approval state\) are added.

    5.  Verify that approval events and integration rules are now available in the UI by navigating to **All** &gt; **CPQ Administration** &gt; **Transaction**.

    The blueprint import completes, and all approval system events and integrations are seeded in your instance. These system events and integrations are now available for use in approval rules and configurations.

4.  Configure UI effects and layout for the approval experience.

    For more information, see [Configure approval events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-approval-events.md).

5.  Set up stage transitions for the approval workflow.

    For more information, see [Configure stages and entry criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-stages-entry-criteria.md).

6.  Create the web embeddable module for the approval interface.

    1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Home Page**.

    2.  Create a web embeddable module.

        Web embeddables are reusable UI components that can be embedded in multiple places. For approvals, this creates a reusable approval interface component.

    3.  Name the module \(for example, "Advanced Approvals" or "Approval Interface"\).

    4.  Select **Advanced Approvals** as the component type.

    5.  Configure the component properties and save.

        The web embeddable is created, and a SYS ID is generated for the module.

    6.  Copy the SYS ID of the created embeddable module.

    7.  Navigate to **All** &gt; **UI Builder** &gt; **CSM/FSM Configurable Workspace**.

    8.  Select **Quote Transaction Default** component.

    9.  Locate the seismic\_components\_property\_list field.

    10. Add an entry with the embeddable SYS ID for approvals.

    The web embeddable module for approvals is created and configured. The approval interface is now embedded in your microservices instance and ready for use.

7.  Verify all prerequisites are complete.

    1.  Confirm all plugins are active and installed.

    2.  Verify that the approval tenant setting is enabled in your instance.

    3.  Check approval system events and integrations are visible in the Advanced Approvals configuration area.

    4.  Confirm UI buttons and approval interface components are visible in your quote or order forms.

    5.  Verify stage transitions are correctly configured and appear in the configuration UI.

    All prerequisites are verified and complete. Your instance is now ready for approval rule configuration.


## What to do next

Proceed with the following tasks:

-   [Create an approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-configuration.md)
-   [Create conditions that trigger approval workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-approval-trigger-conditions.md)
-   [Create approval rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-rules.md)
-   [Create approval chains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-chain.md)
-   [Define an approval user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-users.md)
-   [Define an approval group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-groups.md)

After approvals are configured, end users can submit approval requests using the approval interface. For user-facing tasks, see [Review and approve a submitted quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/review-and-approve-quote.md).

