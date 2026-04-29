---
title: SAP USMM-based optimization
description: Optimize licensing through SAP User License Measurement \(USMM\) rules that map roles to the Named User Type for an SAP client.
locale: en-US
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

The rules in the SAP USMM map roles to a Named User Type on a system client basis. If you want to apply these rules for named user licensing, ServiceNow AI Platform pulls the USMM rules and stores all information in the SAP USMM Rules \[samp\_sap\_usmm\_rule\] table. A scheduled job, **SAM - SAP USMM Based Optimization**, runs weekly to maximize licensing according to the USMM rules of a system client for the discovered user. This optimized Named User Type is populated in the USMM Named user type column in the SAP System Users \[samp\_sap\_system\_user\] table. For more information, see [Tables installed with the SAP publisher pack](component-installed-sap-plugin.md).

If you opt in for the USMM rules by selecting the **Use USMM Role Optimization** check box in the SAP Connection record, the Software Asset Management application prefers the optimized USMM Named User Type during reconciliation. For more information about creating a connection profile to establish a connection between your SAP system and your ServiceNow instance, see [Establish an SAP connection using basic authentication](../task/add-sap-connection.md).

**Parent Topic:**[Software Asset Management publisher pack for SAP](sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)

[Establish an SAP connection using basic authentication](../task/add-sap-connection.md)

[Establish an SAP connection using OAuth 2.0](../task/add-sap-connection-oauth.md)

[Create entitlements for SAP](../task/create-entitlement-sap.md)

[Create software models for SAP](../task/add-software-model-sap.md)

[Create a custom SAP named user type](../task/create-named-user.md)

[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)

[Create custom SAP price lists](../task/create-sap-pricelist.md)

[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)

[Import custom SAP price lists](../task/import-custom-sap-price-list.md)

[User transaction activity for named user types](sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

