---
title: Associate CIs with an incident
description: Associate affected or impacted configuration items \(CIs\) with an incident record to find out how the incident affects other CIs with dependent relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/associate-cis-with-incident.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Associate CIs with an incident

Associate affected or impacted configuration items \(CIs\) with an incident record to find out how the incident affects other CIs with dependent relationships.

## Before you begin

Role required: admin

## About this task

Use the **Configuration Item** field when a single, primary CI is the cause of the incident. Use the **Affected CIs** or **Impacted Services/CIs** related list when multiple CIs are affected.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open the incident record to which you want to associate CIs.

3.  Perform the following actions:

<table id="table_eh3_nlr_clb"><thead><tr><th>

Options

</th><th>

Procedures

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

1.  Select the lookup icon \[Omitted image "look-up-icon.png"\] Alt text:.
2.  Select a configuration item.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality applies to new customers starting with the Paris release.

</td></tr><tr><td>

Affected CIs

</td><td>

1.  Select **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality applies to new customers starting with the Paris release.

\[Omitted image "affected-ci-offering-filter.png"\] Alt text: Filter in Affected CIs related list

3.  Select **Add Selected**.


</td></tr><tr><td>

Impacted Services/CIs

</td><td>

1.  Select **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out.

3.  Select **Add Selected**.


</td></tr></tbody>
</table>
