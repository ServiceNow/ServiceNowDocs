---
title: Customer Service case digests
description: Use the case digests feature to provide periodic updates and resolution information about high priority customer service cases to customers and internal stakeholders.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Customer Service case digests

Use the case digests feature to provide periodic updates and resolution information about high priority customer service cases to customers and internal stakeholders.

With this feature, you can send periodic case updates while a case is in progress using a [case action summary](case-digest-case-action-summary.md). Once a case has been resolved, you can provide a [post case review](case-digest-post-case-review.md) document that captures details about the issue, root cause, resolution, and preventive measures.

The case digests feature uses a configuration for case action summaries and post case reviews. The configuration determines the information from a customer service case that is captured as part of the case action summary or the post case review document. The configuration also identifies the template that is used to create the summaries and review documents.

## Case digests workflows

Starting with the Zurich release, legacy approval workflows for the Case Digests \(com.sn\_csm\_case\_digest\) application have been migrated to low code flows in Workflow Studio. The functionality of the flows remains the same.

Post case reviews can include optional approval workflows that trigger an approval process. These workflows are selected as part of the case digest configuration.

-   New customers can select a flow from the **Approval flow** field on the Case Digest Configuration form when creating a configuration for a post case review.
-   For upgrade customers:
    -   Selecting an existing post case review configuration displays the legacy workflow in the **Approval workflow** field.
    -   When creating a new configuration for a post case review, customers can select a low code flow from the **Approval flow** field.

Upgrade users with one or more case digest configurations that use legacy workflows can continue to use the configurations. No changes have been made to existing configurations.

The **Approval flow** field appears on the configuration record and on the Case Digest Configuration list by default. However, the **Approval workflow** field remains as part of the table and is functional.

