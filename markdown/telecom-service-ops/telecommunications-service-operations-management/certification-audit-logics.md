---
title: Certification Audit Logics
description: Audit Results are created for each audit executed on records that matched the selection \(see matching conditions in Initial Certification Audit Run\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/certification-audit-logics.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identify and reconcile discrepancies, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Certification Audit Logics

Audit Results are created for each audit executed on records that matched the selection \(see matching conditions in Initial Certification Audit Run\).

The result's state can be certified or failed. A Follow-On Task is created for each ‘failed’ Audit Result record.

## Initial Certification Audit Run

Validating specific CMDB tables for anomalies.

The Service Operation CMDB Compliance Audit starts to run on the CI Relationship table \(cmdb\_rel\_ci\), but only on specific records with matching conditions as follows:

-   Parent AND child CI classes are supported classes, including extended tables as follows:

    slot \(cmdb\_ci\_container\_slot\), subslot \(cmdb\_ci\_container\_subslot\), card \(cmdb\_ci\_interface\_card\), interface \(cmdb\_ci\_ni\_interface\), telco equipment \(cmdb\_ci\_ni\_telco\_equipment\), IP switch \(cmdb\_ci\_ip\_switch\), and IP router \(cmdb\_ci\_ip\_router\).

    **Note:** These properties can be configured via sn\_tsom\_core.audit.\* system properties.

-   Parent OR child is created or updated by Discovery \(discovery\_source = SG-Altiplano, ServiceNow\). Audit uses its own filter mechanism that applies on equipment Cis. Default filter is “discovery\_source CONTAINS TSOM"
-   Parent AND child life-cycle Stage is Operational.
-   The CI Relationship Type is Contains::Contained By.

    **Note:** This property can be configured in the sn\_tsom\_core.audit.relationship\_types system property.


## Subsequent Certification Audit Runs

Follows the same logic as the Initial Certification Audit Run, but with the following additional matching selection criteria:

The timestamp in the Updated field in the CI Relationship table, or the timestamp in the Updated field of a Parent CI, or the timestamp in the Updated field of child CIs is later than the timestamp in the ‘Last run date’ field in the Telecom Discrepancy Audit \(this means that there was a change since the last audit\).

