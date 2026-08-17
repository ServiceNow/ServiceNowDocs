---
title: Removed features and products in Australia
description: Cumulative release notes summary on features that were removed from Australia features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-removed-features.html
release: australia
topic_type: reference
last_updated: "2026-08-10"
reading_time_minutes: 3
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Removed features and products in Australia

Cumulative release notes summary on features that were removed from Australia features and products.

Some features were removed as part of Australia product updates.

<table id="rn-summary-removed-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   AI Control Tower removed in [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md):

The Number of clients connecting to MCP servers metrics in Overview tab have been removed. Also, you can't create security incidents from dormant agents using conversational prompts.

-   AI Control Tower \(legacy\) removed in [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md):

The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.

-   AI Control Tower \(legacy\) removed in [Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md):

Adding legacy AI connections via Service Graph Connectors \(SGC\) is deprecated. In AI connections, under Legacy connections, the **New** button has been removed to block users from creating new connections using SGC.


</td></tr><tr><td>

API

</td><td>

-   GlideElementDynamicAttribute has been removed. Use other GlideElement instances corresponding to an attribute's type instead.
-   NowAnalyticsService and NowAnalyticsServiceDelegate have been removed from Mobile SDK - iOS.
-   NowAnalyticsSDK has been removed from Mobile SDK - Android.

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   Roll up logic applies only to system tax, not to supplier-declared tax. Supplier tax roll up is removed. This replaces the previous approach, which lacked independent validation of supplier-provided tax amounts.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see [CMDB 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multisource-cmdb.md).

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

</td></tr><tr><td>

Flows, subflows, and actions

</td><td>

The now.assist.creator role is no longer a required role to use generative AI features with Now Assist.

</td></tr><tr><td>

Impact

</td><td>

On-demand value report and Value potential accelerators have been removed.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

Australia Early Availability

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

</td></tr><tr><td>

Opportunity Management

</td><td>

-   Removed the **New** Opportunity Line button from the platform and workspace view.

</td></tr><tr><td>

Playbook

</td><td>

The now.assist.creator role is no longer a required role to generate a playbook or playbook recommendation when using Now Assist.

</td></tr><tr><td>

Process Mining

</td><td>

You no longer require the now.assist.creator role to access Now Assist features in the Creator Pro Plus package. However, you must enable the relevant Process Mining skill, which serves as the necessary prerequisite. Additionally, you should have appropriate access to the project.

</td></tr><tr><td>

Product Support for Technology

</td><td>

Australia Early Availability

-   The **Analytics** tab is removed from the customer account view.
-   The **Notify Customers** UI action is removed from the case record.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   For Demand Management:
    -   The permission to edit the value of the **dmn\_stakeholder\_register.number** field in the Stakeholder Register \[dmn\_stakeholder\_register\] table has been removed for the admin role.
    -   The admin role ACL has been removed for the bubble chart workbench.
    -   The duplicate app module that was created for the admin role has been removed.

</td></tr><tr><td>

ServiceNow Otto for Creator

</td><td>

Spoke generation has been removed from ServiceNow Otto for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

</td></tr><tr><td>

ServiceNow Otto for Zero Copy Connector

</td><td>

The Ask AI button has been removed from the Model Manager.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   Assessments using entities are no longer supported.
-   The `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles.
-   The `scoring_rule` and `scoring_rule_ref` fields are removed from assessment forms and UI sections. Custom scripts or integrations that reference these fields must be updated.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/release-notes-summaries.md)

