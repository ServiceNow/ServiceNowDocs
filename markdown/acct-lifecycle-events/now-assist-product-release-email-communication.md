---
title: Product release email communication agentic workflow
description: Automatically draft, refine, and distribute product release announcement emails to designated recipients using the most recent release information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/now-assist-product-release-email-communication.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Touchpoints, Customer success, Use, Customer Success Management]
---

# Product release email communication agentic workflow

Automatically draft, refine, and distribute product release announcement emails to designated recipients using the most recent release information.

## Product release email communication agentic workflow overview

The agentic workflow automatically drafts, refines, and publishes release announcement emails to multiple customers regarding product changes and feature adoption. The agentic workflow invokes the AI agent to fetch the latest released product information and creates a draft email. With this agentic workflow a customer success manager can:

-   Timely communicate customers about product changes, enhancements, new feature releases, and feature adoption.
-   Identify the stakeholders, ensure consistent messaging, and streamline distribution.
-   Focus on driving adoption and customer value instead of repetitive communication tasks.

This agentic workflow is delivered as part of the base system and is preconfigured to operate with the Digital Product Release \(DPR\) application. This enables customers to get started quickly using the default setup. However, the workflow is designed with flexibility in mind and isn't limited to DPR. Organizations using alternative release management or related systems can adopt this capability by integrating their existing applications with minimal customization.

When the DPR record moves to the completed state, the agentic workflow triggers automatically. For more information about DPR, see [Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/dpr-landing-page.md). The customer success manager can trigger this agentic workflow manually only for assigned product releases.

The customer success manager can access this agentic workflow with these roles: `sn_acct_lc.customer_success_agent` and `sn_dpr_model.release_user`.

Agentic workflows included with the base system are read-only. To configure this workflow, see [Configure agentic workflows for Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-workflows-config.md).

**Parent Topic:**[Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-use-touchpoints.md)

