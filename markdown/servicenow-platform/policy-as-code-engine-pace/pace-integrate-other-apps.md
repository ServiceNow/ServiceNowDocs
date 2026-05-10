---
title: Integrating PaCE with other applications
description: Extend the capabilities of Policy as Code Engine \(PaCE\) by creating policies with other applications.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Integrating PaCE with other applications

Extend the capabilities of Policy as Code Engine \(PaCE\) by creating policies with other applications.

PaCE provides integrations with the applications listed in the following table:

<table id="table_ncs_lh1_vzb"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Digital Product Release \(DPR\)

</td><td>

Define policies in Digital Product Release, see the [Define policies in Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-policy-admin.md) topic.

</td></tr><tr><td>

Software Bill of Materials \(SBOM\)

</td><td>

Starting with version 4.0 of SBOM Response, an application that is part of the [Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations-landing-page.md) suite of applications, you can view components that are identified as stale or abandoned as ‘Non-compliant’ in the Policy as Code Engine \(PaCE\) interface that is available in the Software Bill of Materials Workspace.-   Determine if components are stale or abandoned with the **Run PaCE policies for SBOM Response** scheduled job. This scheduled job is deactivated by default.
-   View components that are identified as stale or abandoned as Non-compliant in the PaCE interface that is available and viewed in the SBOM Workspace.

See [Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sbom-core/vr-sbom-config-osv-deps.md) for more information.

</td></tr></tbody>
</table>