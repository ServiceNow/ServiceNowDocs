---
title: Associate CIs with incident
description: Associate affected or impacted configuration items \(CIs\) with an incident record to find out how the incident affects other CIs with dependent relationships.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Associate CIs with incident

Associate affected or impacted configuration items \(CIs\) with an incident record to find out how the incident affects other CIs with dependent relationships.

## Before you begin

Role required: admin

## About this task

Use the **Configuration Item** field when there is a single, primary CI that is the cause of the incident and the **Affected CIs** or the **Impacted Services/CIs** related list when multiple CIs are affected by the incident.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open the incident record to which you want to associate CI items.

3.  Perform the following actions:

<table id="table_eh3_nlr_clb"><thead><tr><th>

Options

</th><th>

Procedures

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

1.  Click the lookup icon \(![Lookup icon](../../itsm-workspace/image/look-up-icon.png)\).
2.  Select configuration item.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality is applicable to the new customers starting the Paris release.

</td></tr><tr><td>

Affected CIs

</td><td>

1.  Click **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality is applicable to the new customers starting the Paris release.

![Filter in Affected CIs related list](../image/affected-ci-offering-filter.png)

3.  Click **Add Selected**.


</td></tr><tr><td>

Impacted Services/CIs

</td><td>

1.  Click **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out.

3.  Click **Add Selected**.


</td></tr></tbody>
</table>
