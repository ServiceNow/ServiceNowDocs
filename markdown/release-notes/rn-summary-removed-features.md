---
title: Removed features and products in Xanadu
description: Cumulative release notes summary on features that were removed from Xanadu features and products.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 5
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Removed features and products in Xanadu

Cumulative release notes summary on features that were removed from Xanadu features and products.

Some features were removed as part of Xanadu product updates.

<table id="rn-summary-removed-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Application Vulnerability Response

</td><td>

The **Close** button has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

</td></tr><tr><td>

Configuration Compliance

</td><td>

-   The **Reason** field in the Resolve modal has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.
-   The **Close** button has been removed for a remediation task, in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   CMDB Health:
    -   The CMDB Health Dashboard on Core UI isn't included in new Xanadu instances. On upgraded instances, this dashboard is available but no longer supported.
    -   The CI dashboard isn't included in new Xanadu instances. On upgraded instances, this dashboard is available but no longer supported.
    -   The following widgets have been removed from the CI Health tile in the CMDB Workspace: Incomplete Attributes vs Total Attributes, Non-compliant relationships vs Total Relationships, and Stale relationships vs Total Relationships widgets.
    -   The concept of the overall health score has been removed and no longer appears in any of the CMDB Health dashboards or views.
    -   The concept of weighted averages and scorecards thresholds, which specify the ranges of health states, has been removed.
    -   The bar charts for metrics in the main CMDB Health Dashboard have been removed, as well as the tiles for top 10 incident, alert, and change generators.
    -   The **CMDB Health Dashboard - Top Task Generating CIs Calculation** scheduled job has been removed.
-   CSDM and the CMDB Data Foundations Dashboards:
    -   When drilling down into the CIs Not Processed Via IRE in the Data Management Practices metric group, the **Show Records** button isn't supported.
    -   When drilling down into the Orphan CIs metric, only a list view of orphan CIs appears without any Performance Analytics details.

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

The **Close** button has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   The Authorization Official \(AO\) \(sn\_irm\_cont\_auth.authorization\_official\) role no longer contains the sn\_audit.user and sn\_compliance.user roles. The AO role can only read and approve an authorization package.
-   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role no longer contains the sn\_audit.user role.
-   The Reader \(sn\_irm\_cont\_auth.reader\) role no longer contains the sn\_audit.user role.

</td></tr><tr><td>

Document Intelligence

</td><td>

Starting in the Xanadu release, the Platform Document Intelligence Usage dashboard is no longer supported or available through the Document Intelligence application. Performance metrics are available in the Document Intelligence Admin experience. For more information, see [Document Intelligence monitoring dashboard](https://www.servicenow.com/docs/access?context=document-intelligence-monitoring-dashboard&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Employee Center

</td><td>

The Content Publishing and Content Experiences demo portals have been removed.

</td></tr><tr><td>

Event Management

</td><td>

The Event Management Mobile application is no longer available.

</td></tr><tr><td>

Field Service Management

</td><td>

The Field Service dashboard is removed from the Emergency Exposure Management application.

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   Moved the reason code for Late Presentment from the processing error decision question to the authorization category.
-   Updated the 12.1 chargeback rules to 11.3, aligning with VROL’s latest release revision 24.2.
-   Removed the **is\_parcelado** column from the dispute intake table, in alignment with VROL’s latest release revision 24.2.

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   Removed the system property com.snc.process\_flow.reporting.iteration.lastn that was used to specify the number of loop iterations that a flow would generate execution details for. To report on all iterations of a loop, create a flow execution settings record for the flow instead. For more information about flow execution settings, see [Flow execution settings](https://www.servicenow.com/docs/access?context=flow-execution-settings&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   The user preference for flow authors to include draft actions in the list of available actions has been removed. To see a custom action during flow design, publish the action. For more information, see [Create an action in Workflow Studio](https://www.servicenow.com/docs/access?context=create-action&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Integration Hub

</td><td>

-   The Legacy Usage Overview dashboard is deprecated. This feature is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   The Actions tab has been removed from the Next Experience Inspector.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   Starting with version 2.0.1 of AI Agents for Observability, the sn\_obs\_aia.admin role, previously required to configure AI agents in the Analyze alert impact agentic workflow, has been removed. Users must now have the credential\_admin and connection\_admin roles instead.
-   Starting with version 2.0.1 of AI Agents for Observability, the prompt `How severe is this alert?` no longer appears in the Analyze alert impact agentic workflow.

</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

The **Opened** column was removed from the lists under the OT Incident module in the Industrial Workspace list view.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   The **New** button has been removed from the **All OT Devices** list view and its corresponding list views.
-   The **New** button has been removed from the Equipment Model Entities related list in the Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] form.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

Use the Questionnaire activity instead of the Collect User Data activity.

</td></tr><tr><td>

RPA Hub

</td><td>

The credential set related list was removed from the bot process form in RPA Hub.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   The `scopeId` parameter was removed from the `now-sdk convert` command, which supported converting global applications. Only scoped applications can be converted.
-   The `mode` parameter was removed from the `now-sdk fetch` and `now-sdk deploy` commands. A complete fetch or deploy are always executed.

</td></tr><tr><td>

Skills Intelligence

</td><td>

The Skills onboarding feature is removed and is replaced with Skill imports playbook experience. For customers who already have their data in Skills onboarding, download all the skills in the Ready for review state and re-upload them using the new import process. For more information, see .

</td></tr><tr><td>

Software Asset Management

</td><td>

The following legacy dashboards are no longer available for new Xanadu users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Xanadu without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu.

-   Office 365 and Adobe Cloud dashboard
-   Software Asset Analytics dashboard
-   Software Publisher Analytics dashboard
-   SaaS Overview dashboard
-   Software Asset Management dashboard
-   Engineering License Overview dashboard
-   Normalization and Content Service dashboard
-   Software Asset Management Foundation dashboard
-   Overlapping Software dashboard

**Note:** If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to the legacy dashboards. If you activate the Workspace plugin, you aren't able to access the legacy dashboards from the **Software Asset** navigation menu in your instance. You can, however, access the legacy dashboards from the **Dashboards** navigation menu.

</td></tr><tr><td>

Subscription Management

</td><td>

-   The Custom tables chart has been removed from the subscription details page.

</td></tr><tr><td>

Theme Builder

</td><td>

-   Removed the **Apply** button used to apply your theme to web and mobile instances. To publish your theme, use the **Publish** option from the theme card overflow menu. For more information about publishing themes, see [Publish your themes with Theme Builder](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Vulnerability Response

</td><td>

The **Close** button has been removed for a remediation task in the Classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](../release-notes-summaries.md)

