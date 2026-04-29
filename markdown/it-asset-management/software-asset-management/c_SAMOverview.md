---
title: Software Asset Management overview
description: An overview of the functionality of the Software Asset Management application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software Asset Management overview

An overview of the functionality of the Software Asset Management application.

Software Asset Management functionality consists of these main features.

<table id="table_fxn_2mt_1bb"><thead><tr><th>

Feature area

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dashboards

</td><td>

These dashboards show software installation results for your environment in the form of statistics and charts. -   Software Asset Analytics: Overview, License Summary, Compliance Summary, and Removal Summary
-   Normalization and Content Service: Normalization trend charts
-   Software Publisher Analytics: Citrix, IBM, Microsoft, Oracle, SAP, and VMware.

**Note:** The publisher pack add-on must be activated to see the Software Publisher Analytics dashboard.

-   Office 365 and Adobe Cloud

**Note:** The publisher pack add-on must be activated to see the Office 365 and Adobe Cloud dashboard.

-   Software Asset Management: Overview, Optimization, Compliance Analysis

</td></tr><tr><td>

Licensing

</td><td>

Software models created for all installed software products are used to tie software installations \(software being used\) with entitlements \(software owned\). Entitlements define license details and are assigned to software models.Features include publisher part number lookup, common per core and per processor license metrics, entitlement discovery maps, exclusion listing, client access, license change projection, entitlement import, and entitlement import error results list.

</td></tr><tr><td>

Discovery and normalization

</td><td>

A discovery process, such as ServiceNow Discovery or Microsoft SCCM \(2012 v2 or 2016\), can be used to discover the software installed in your environment. The normalization process compares the discovered publisher, discovered product, and discovered version values against the ServiceNow repository of normalized equivalents

 An OOB Normalization library contains all content except publisher and product. Custom products can be created if a software product does not exist in the Software Library. Discovered software can also be manually normalized for reconciliation. A software discovery model is then matched to discovered software installations.

 Features include partial, full, and publisher normalization, License Workbench, License Position report, custom pattern normalization rules, normalization suggestions, on-premise customer support, and an optional Software Asset Management content service to update the Normalization Library with pattern normalization rules.

 The Integration — Microsoft SCCM 2016 plugin is compatible with SCCM version 1606, 1906, 1910, and 2002.

 **Note:** Legacy SCCM plugins, SCCM 2012 and SCCM 2016, will be deprecated in the upcoming releases.If you are creating the integration for the very first time, then begin with Microsoft SCCM Service Graph Connector SG Connector. If you are already using one of these plugins then use the application titled Migration Readiness Tool for Service Graph Connector for SCCM in the ServiceNow Store to prepare for migration to the Service Graph Connector.

</td></tr><tr><td>

Reconciliation

</td><td>

The reconciliation process calculates the compliance status of software products regarding discovery and entitlements.Removal candidates are generated for unused software that can be used to reclaim software rights.

 Features include reconciliation grouping, and remediation actions for resolving compliance issues.

</td></tr><tr><td>

Optimization

</td><td>

The reclamation process remediates non-compliance by uninstalling software from devices and reclaiming those software rights. The reclamation process can be automated using Client Software Distribution \(CSD\).Features include removal candidate and workflows, reclamation rule creation, software usage listing, and support for creating a purchase order directly using Procurement integration. For more information, see the [Procurement overview](https://www.servicenow.com/docs/access?context=c_Procurement&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Downgrade Rights

</td><td>

The concept of downgrading licenses is built into the Software Asset Management plugin feature. Downgrade rights is the process of having acquired the rights to the latest version of software but using the rights to license earlier versions of the same software. For more information, see [Downgrade Rights](downgrade-rights.md).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

