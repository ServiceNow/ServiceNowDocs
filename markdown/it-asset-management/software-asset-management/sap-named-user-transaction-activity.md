---
title: User transaction activity for named user types
description: Determine license optimizations for your SAP named user types based on your SAP user transaction activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sap-named-user-transaction-activity.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# User transaction activity for named user types

Determine license optimizations for your SAP named user types based on your SAP user transaction activity.

User transaction activities are the transactions or tasks that users perform on an SAP client. These activities are based on SAP transaction codes \(t-codes\), which are the shortcuts that enable you to identify and perform these transactions or tasks. When you run scheduled jobs for SAP, the Software Asset Management application retrieves the SAP transaction codes that were actively used by your SAP users.

When you create a reclamation rule for an SAP named user type, you can specify the transaction codes and the minimum number of those transaction codes that must be active for a user to keep their assigned named user license. During reconciliation, the Software Asset Management application compares these transaction codes against the discovered user transaction codes for the named user type. You can view the resulting data in the Users for Transaction Based License Optimization report on the Software Publisher Analytics dashboard for SAP. Use this information to optimize your named user license position by downgrading licenses or reclaiming unused licenses. See [Software Publisher Analytics dashboard for SAP in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/dashboard-sap.md) for more information on this report.

-   **[View active transaction codes for your SAP users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/view-sap-transaction-activity.md)**  
View the SAP transaction codes \(t-codes\) that were actively used by your SAP users. This list is compared against your reclamation rules to determine whether the user is assigned an optimized license.

**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create entitlements for SAP]()

[Create software models for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

