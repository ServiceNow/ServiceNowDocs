---
title: User transaction activity for named user types
description: Determine license optimizations for your SAP named user types based on your SAP user transaction activity.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# User transaction activity for named user types

Determine license optimizations for your SAP named user types based on your SAP user transaction activity.

User transaction activities are the transactions or tasks that users perform on an SAP client. These activities are based on SAP transaction codes \(t-codes\), which are the shortcuts that enable you to identify and perform these transactions or tasks. When you run scheduled jobs for SAP, the Software Asset Management application retrieves the SAP transaction codes that were actively used by your SAP users.

When you create a reclamation rule for an SAP named user type, you can specify the transaction codes and the minimum number of those transaction codes that must be active for a user to keep their assigned named user license. During reconciliation, the Software Asset Management application compares these transaction codes against the discovered user transaction codes for the named user type. You can view the resulting data in the Users for Transaction Based License Optimization report on the Software Publisher Analytics dashboard for SAP. Use this information to optimize your named user license position by downgrading licenses or reclaiming unused licenses. See [Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md) for more information on this report.

-   **[View active transaction codes for your SAP users](../task/view-sap-transaction-activity.md)**  
View the SAP transaction codes \(t-codes\) that were actively used by your SAP users. This list is compared against your reclamation rules to determine whether the user is assigned an optimized license.

**Parent Topic:**[Software Asset Management publisher pack for SAP](sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)

[Establish an SAP connection](../task/add-sap-connection.md)

[Create entitlements for SAP](../task/create-entitlement-sap.md)

[Create software models for SAP](../task/add-software-model-sap.md)

[Create a custom SAP named user type](../task/create-named-user.md)

[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)

[Create custom SAP price lists](../task/create-sap-pricelist.md)

[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)

[Import custom SAP price lists](../task/import-custom-sap-price-list.md)

[SAP USMM-based optimization](usmm-optimization.md)

[Self-declaring SAP engine license usage](self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

