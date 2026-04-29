---
title: IBM ILMT setup success guide
description: This success guide provides information on the IBM License Metric Tool \(ILMT\) or IBM BigFix Inventory integration with the Software Asset Management application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Success Guides, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# IBM ILMT setup success guide

This success guide provides information on the IBM License Metric Tool \(ILMT\) or IBM BigFix Inventory integration with the Software Asset Management application.

This integration supports license compliance for IBM products using the following IBM license metrics:

-   Processor Value Unit \(PVU\)
-   Resource Value Unit \(RVU MAPC\)

The integration imports only the IBM product usage data that is required for these license metrics.

**Note:** This integration doesn’t import any discovery or usage data for IBM products that are licensed via other metrics.

For IBM license compliance to work with this integration, you must complete the following prerequisites:

-   Set up and run ILMT or BigFix Inventory on your instance.
-   Configure IBM ILMT agents to scan your instance in compliance with the IBM usage measurement guidelines.
-   Enable ILMT or BigFix Inventory to discover the configurations of both virtual machines \(VMs\) and physical hosts as well as the relationships between them.
-   Classify IBM components into IBM products through ILMT or BigFix Inventory.
-   Bundle IBM components into IBM products through ILMT or BigFix Inventory.
-   Install ILMT version 9.2.7 or later.

Complete the following steps for the [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md) with the Software Asset Management application:

1.  [Create a connection to ILMT or BigFix Inventory](../task/set-up-ibm-platform.md)
2.  [Validate your ILMT connection health](../task/validate-ilmt-connection-health.md)

## Alternative to ILMT or BigFix Inventory

You can track and manage IBM licenses in both VMware vSphere environments and IBM LPAR infrastructures by integrating the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program. With these integrations, you can track and manage IBM licensing directly without having to integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory. For more information, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md).

## Additional resources

-   IBM license management by the Software Asset Management application
    -   [Software Asset Management publisher pack for IBM](ibm-publisher-pack.md)
    -   [Supported IBM license types](supported-ibm-license-types.md)
-   [Fix invalid computer serial numbers](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0691430)

