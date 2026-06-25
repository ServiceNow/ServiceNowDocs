---
title: SAP USMM-based optimization
description: Optimize licensing through SAP User License Measurement \(USMM\) rules that map roles to the Named User Type for an SAP client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/usmm-optimization.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# SAP USMM-based optimization

Optimize licensing through SAP User License Measurement \(USMM\) rules that map roles to the Named User Type for an SAP client.

The rules in the SAP USMM map roles to a Named User Type on a system client basis. If you want to apply these rules for named user licensing, ServiceNow AI Platform pulls the USMM rules and stores all information in the SAP USMM Rules \[samp\_sap\_usmm\_rule\] table. A scheduled job, **SAM - SAP USMM Based Optimization**, runs weekly to maximize licensing according to the USMM rules of a system client for the discovered user. This optimized Named User Type is populated in the USMM Named user type column in the SAP System Users \[samp\_sap\_system\_user\] table. For more information, see [Tables installed with the SAP publisher pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/component-installed-sap-plugin.md).

If you opt in for the USMM rules by selecting the **Use USMM Role Optimization** check box in the SAP Connection record, the Software Asset Management application prefers the optimized USMM Named User Type during reconciliation. For more information about creating a connection profile to establish a connection between your SAP system and your ServiceNow instance, see [Establish an SAP connection using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/add-sap-connection.md).

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

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

