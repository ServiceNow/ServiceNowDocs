---
title: Manage continuous monitoring for risks between Risk Management and Vulnerability Response
description: Continuous monitoring for risks is a feature integration between the GRC: Risk Management and the Security Operations Vulnerability Response products, which uses indicators to quickly identify high impact vulnerabilities based on business impact.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Manage continuous monitoring for risks between Risk Management and Vulnerability Response

Continuous monitoring for risks is a feature integration between the GRC: Risk Management and the Security Operations Vulnerability Response products, which uses indicators to quickly identify high impact vulnerabilities based on business impact.

Risk administrators, managers, or users can monitor critical vulnerabilities by viewing the direct effect on risk posture. A new **Business Services** entity type and indicator templates automatically identify impacted services that are critical, represent a loss of availability, and are greater than two weeks old. These high-risk vulnerabilities can result in a breach and possible loss of intellectual property.

**Note:** The Entity type called 'Critical Business Services' is set to inactive by default and must be turned on.

## Continuous monitoring for risk workflow

1.  The system admin activates the Risk Management and Vulnerability Response plugins.
2.  The risk administrator creates risk statements and indicator templates.
3.  The risk manager associates the **Critical Business Services** entity type to the risk statements and indicator templates.
4.  The Vulnerability Response application ingests vulnerability data from scanners related to impacted services.
5.  As risks are identified, issues are generated and assigned to the appropriate business service owners.
6.  Dashboards provide an up-to-date view for business stakeholders as risks are identified and remediated.

**Parent Topic:**[Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md)

