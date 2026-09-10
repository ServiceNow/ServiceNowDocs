---
title: Software packages categorization
description: Agent Client Collector for Visibility \(ACC-VC\) classifies discovered software packages in your environment into categories. This categorization removes the need to tag software records manually and provides an accurate software inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-software-categorization.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [software categorization, software packages, ACC-VC]
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Software packages categorization

Agent Client Collector for Visibility \(ACC-VC\) classifies discovered software packages in your environment into categories. This categorization removes the need to tag software records manually and provides an accurate software inventory.

## Software categorization overview

Software packages the system has discovered in your environment are stored in two different tables:

-   If Software Asset Management \(SAM\) is installed on your instance, they are stored in the **Software Discovery Models** \(cmdb\_sam\_sw\_discovery\_model\) table.
-   If SAM is not installed, they are stored in the **CMDB CI Package** \(cmdb\_ci\_spkg\) table and the **Software package** column is populated.

ACC-VC software categorization compares each discovered software package with active, admin-defined categorization signatures. A signature is a rule that matches software to a category based on the software name or publisher. When you activate the signature, ACC-VC scans discovered software and finds matches. The system then creates entries in the Software Categorization Catalog table. Each catalog entry identifies the software package, the category assigned to it, and the signature it matched. You can filter the catalog by category to review all software in a group, such as AI tools, security-related software, or communication tools.

Software is categorized or re-categorized automatically, without creating a new signature, in the following cases:

-   An inactive signature is reactivated.
-   New software is discovered that matches an existing active signature.

-   **[Categorize discovered software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-categorize-discovered-software.md)**  
Group discovered installed software packages in your environment by business relevance.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

