---
title: Scan Engine definitions
description: The Scan Engine uses a large set of definitions to correct coding and workflow findings in real-time and perform scans across your entire instance to detect existing findings.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine definitions

The Scan Engine uses a large set of definitions to correct coding and workflow findings in real-time and perform scans across your entire instance to detect existing findings.

## Pre-defined definitions

There are various types of definitions available as a baseline in the Impact Scan Engine.

<table id="table_zby_my2_m2c"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security

</td><td>

Measures implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.See [Scan Engine definitions: Security](../reference/scan-engine-definitions-security.md) for additional information.

</td></tr><tr><td>

Performance

</td><td>

Measures the efficiency of a ServiceNow instance, encompassing aspects such as speed, responsiveness, resource utilization, and overall dependability.See [Scan Engine definitions: Performance](../reference/scan-engine-definitions-performance.md) for additional information.

</td></tr><tr><td>

Manageability

</td><td>

Measures the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.See [Scan Engine definitions: Manageability](../reference/scan-engine-definitions-manageability.md) for additional information.

</td></tr><tr><td>

Upgradeability

</td><td>

Assesses the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.See [Scan Engine definitions: Upgradeability](../reference/scan-engine-definitions-upgradeability.md) for additional information.

</td></tr><tr><td>

User Experience

</td><td>

Evaluates the quality of user interactions with applications. Considers the ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.See [Scan Engine definitions: User Experience](../reference/scan-engine-definitions-user-experience.md) for additional information.

</td></tr></tbody>
</table>For more information, see [Configure Scan Engine properties](../task/configure-scan-engine-properties.md).

## Custom definitions

Users can create their own custom definitions. For more information, see [Create custom Scan Engine definitions](../task/create-scan-engine-definitions.md#).

**Note:** The number of custom definitions that is permitted varies based on your Impact package. For more information, see [Impact packages](../reference/impact-packages.md).

## Scan Engine definition suites

Definition suites are groupings of similar definitions that allow administrators to target specific areas or functions of code during scans. This is useful as it allows scanning of the entire instance or all definitions. Admins can focus on a suite that represents a logical category \(for example, JavaScript naming conventions, ITOM workflows, security hardening, and so on\). This improves efficiency and precision in code quality checks.

By default, the following suites are available:

-   Scan Engine
-   JavaScript Naming Conventions
-   Scoped Application
-   ITOM
-   Workflow Engine
-   Security and Instance Hardening
-   IL4 \(Impact Level 4\)
-   HR Scoped Applications
-   Artificial Intelligence Readiness

**Note:** Only users with the `sn_se.scan_engine_admin_role` role can modify existing suites and their relationship with their definitions.

For more information, see [Create Scan Engine definition suites](../task/create-scan-engine-definition-suites.md#).

