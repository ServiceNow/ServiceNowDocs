---
title: Use case: Regulatory compliance in a financial services solution
description: A financial institution needs to ensure that its data is accessible only to the departments that have authorization for the indicated data.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain separation and Agent Client Collector, Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Use case: Regulatory compliance in a financial services solution

A financial institution needs to ensure that its data is accessible only to the departments that have authorization for the indicated data.

## Challenge

The financial institution must comply with regulations that require strict data separation between departments \(such as HR, IT, or Finance\).

## Solution

1.  Create separate domains for each department \(IT, Finance, HR, Compliance, and so forth\) in the Agent Client Collector \(ACC\) configuration.
2.  Apply access controls so that sensitive data \(such as employee records and financial transactions\) is accessible only to authorized departments.
3.  Use ACC health instance scans to ensure that data separation is maintained, especially when updating or troubleshooting systems.
4.  Periodically audit domain separation settings to ensure compliance with data privacy regulations such as GDPR, SOX, or PCI-DSS.

## Outcome

Compliance with legal and regulatory requirements is ensured, and sensitive data is protected from unauthorized access.

**Parent Topic:**[Domain separation and Agent Client Collector](domain-separation-agent-client-collector.md)

