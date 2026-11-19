---
title: ServiceNow Otto for Software Asset Management \(SAM\) release notes
description: The ServiceNow Otto for Software Asset Management \(SAM\) application brings agentic AI to Software Asset Management. See the following sections for release notes by version.This release adds five AI-powered skills that automatically resolve unmatched publisher and product values in entitlement imports.This version includes support for Gemma, a third-party LLM model and enhancements to the Software removal candidate evaluation AI agent.This release adds AI-powered analysis of software spend transactions and software spend detection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/servicenow-otto-sam-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# ServiceNow Otto for Software Asset Management \(SAM\) release notes

The ServiceNow Otto for Software Asset Management \(SAM\) application brings agentic AI to Software Asset Management. See the following sections for release notes by version.

## About ServiceNow Otto for Software Asset Management \(SAM\)

-   Automatically match software entitlements to installations and usage data, and flag over-deployment and unused licenses so asset managers aren’t reconciling spreadsheets by hand.
-   Route license requests, installs, and upgrades to the right approvers and fulfillment steps, cutting response and provisioning time for employees.
-   Link publishers, contracts, entitlements, and install records into one view, then use AI analysis to flag renewal risks, shelfware, and reclaim opportunities.

See [ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam.md) for more information.

**Important:** For Now LLM Service model updates for each release, see [Model provider updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-llm-model-updates.md).

## Activation and other requirements

-   **Activation information**

    Install ServiceNow Otto for Software Asset Management \(SAM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/it-asset-management-rn-landing.md)

## Version 13.0.0

This release adds five AI-powered skills that automatically resolve unmatched publisher and product values in entitlement imports.

### What's new

-   **[Resolve entitlement import errors by using ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/resolve-entitlement-import-error.md)**

    Resolve unmatched publisher and product data that blocks bulk entitlement imports in Software Asset Workspace by using five new AI-powered skills that normalize publisher and product values:

    -   Publisher Search Tags Generation
    -   Product Search Tags Generation
    -   Publisher Match Review
    -   Product Match Review
    -   Product Resolution

## Version 12.0.0

This version includes support for Gemma, a third-party LLM model and enhancements to the Software removal candidate evaluation AI agent.

### What's new

-   **[Evaluate software subscription removal candidates at integration profile and software model levels with the enhanced Evaluate Software Reclamation AI Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam-evaluate-removal-candidate-workflow.md)**

    Launch the Evaluate Software Reclamation AI Agent directly from the **Reclamation** tab of the License usage view in the Software Asset Workspace. The AI agent enables you to evaluate software subscription removal candidates at both the integration profile and software model levels, using reclamation summary data, without leaving your workflow.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the October 2026 release, Gemma 4 26B A4B IT and Gemini 3.5 flash models joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


## Version 11.0.0

This release adds AI-powered analysis of software spend transactions and software spend detection.

### What's new

-   **[Analyze software spend transactions with AI in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/spend-detection-ai-enhancements.md)**

    Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


