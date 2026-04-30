---
title: Tagging records with functional domain
description: Functional domain tagging is a mechanism that allows you to classify risk records based on the specific business function, process, or use case they support. A functional domain represents a logical grouping, such as Cybersecurity and risk, IT risk and compliance, Compliance, Third-Party Risk, or Operational Risk.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Tagging records with functional domain

Functional domain tagging is a mechanism that allows you to classify risk records based on the specific business function, process, or use case they support. A functional domain represents a logical grouping, such as Cybersecurity and risk, IT risk and compliance, Compliance, Third-Party Risk, or Operational Risk.

To understand feature adoption across diverse business functions, you can apply functional domain tags to records, either manually or through automation. This tagging allows organizations to identify how Integrated Risk Management capabilities are used across different teams, departments, and use cases.

Functional domain tagging provides a mechanism to capture structured metadata that reflects actual business usage across domains. This record tagging is critical for understanding adoption trends, identifying gaps in utilization, and informing targeted enablement efforts. By aggregating domain-specific usage data, organizations can generate metrics for reporting, continuous improvement, and stakeholder alignment.

## Key benefits

The following benefits highlight the value of implementing functional domain tagging.

-   Facilitates targeted analysis of risk feature adoption across business units.
-   Enables more informed decision-making for product planning and enablement.
-   Supports domain-specific guidance and best practice recommendations.
-   Contributes to the development of adoption metrics and reporting frameworks.

## Tagging records

A scheduled job named `Populate Functional domain metrics table weekly` has been implemented to maintain accurate and up-to-date adoption metrics. This job systematically queries key Risk-related tables such as **sn\_risk**, **sn\_control**, and **sn\_citation**, identifies and counts records tagged with functional domains. It then calculates the count of tagged records, aggregates the data, and inserts the results into the `Functional domain metrics` \(sn\_grc\_functional\_domain\_metrics\) table. This automated process ensures reliable visibility into domain-level usage and supports informed reporting for adoption tracking and analysis.

The scheduled job is configured to run every Monday at 1:00 AM. Upon successful execution, the `Functional domain metrics` table is updated with the latest aggregated data. Users with the `usage_admin` role can see the data in this table.

The `Functional domain metrics` table includes the following columns: Count, Functional Domain, Domain, and Type.

![Functional domain metrics table with data populated after the Populate Functional domain metrics table weekly job has been executed successfully.](../image/functional-domain-metrics-table.png "Functional domain metrics table")

## Supported record types

The following is a list of supported record types:

-   Risk
-   Control
-   Issue
-   Authority Document
-   Audit tasks
-   Engagement
-   Citation
-   Policy
-   Control objective
-   Entity
-   Entity Class
-   Entity Type
-   Risk Statement

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

