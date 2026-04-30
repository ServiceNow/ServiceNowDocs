---
title: Configuring calculator groups and calculators for Configuration Compliance
description: Configuration Compliance calculators are used to update record values when pre- defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Configuration Compliance, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuring calculator groups and calculators for Configuration Compliance

Configuration Compliance calculators are used to update record values when pre- defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Configuration Compliance calculators

The Configuration Compliance application includes two types of calculators, Risk Calculators and Risk Score Rollup Calculators. These calculator groups are enabled by default.

The Risk Score calculator group has been renamed to Risk Calculators.

The Risk Score Rollup Calculators includes rollup calculators for configuration tests and remediation tasks.

Configuring risk and rollup calculators for remediation of test results and remediation tasks includes the following tasks:

-   Create a risk calculator
-   Create a risk score rollup calculator

After you create a risk calculator, it is available for calculations with the next data ingestion. After you create it, you may also prefer to apply it on-demand.

For more information about calculators and calculator groups, see [Configuration Compliance calculator groups](vuln-config-compl-calc-groups.md).

**Parent Topic:**[Exploring Configuration Compliance](vuln-config-compl.md)

