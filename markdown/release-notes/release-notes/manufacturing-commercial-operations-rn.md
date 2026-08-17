---
title: Manufacturing Commercial Operations release notes
description: The ServiceNow Manufacturing Commercial Operations enables manufacturers, agents, and dealers \(internal and channel partners\) to connect and track services and manage repair, recall, sales promotion campaigns, and quality management. Manufacturing Commercial Operations is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Manufacturing Commercial Operations release notes

The ServiceNow® Manufacturing Commercial Operations enables manufacturers, agents, and dealers \(internal and channel partners\) to connect and track services and manage repair, recall, sales promotion campaigns, and quality management. Manufacturing Commercial Operations is a new application in the Australia release.

## Manufacturing Commercial Operations highlights for the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   Starting with Zurich Patch 12, ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Now Assist for Manufacturing Commercial Operations. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   The CSM/FSM workspace landing page surfaces assigned claims, pre-authorization requests, and dashboard widgets with claims volume and value insights.
-   Anomaly-detection rules enable auto-approval or flagging of repair claim case lines for human review based on eligibility thresholds and historical claim averages.
-   Repair claim case lines display a suggested action and reason on the panel, giving claim reviewers job-level and claim-level analysis in a single view.
-   QIM playbook enables creation of remediation action plans and use of system-recommended containment actions.
-   QIM auto-triages non-conformance records, assigns owners, and generates tasks based on historical patterns.
-   QIM integrates with FSM, enabling work order creation directly from NC and QI records for on-site verification, containment, or remediation action.

See [Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-overview.md) for more information.

**Important:** Manufacturing Commercial Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Manufacturing Commercial Operations landing page \(CSM/FSM configurable workspace\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-landing-page.md)**

    The MCO core landing page surfaces role-based views of claims, pre-authorization requests, and key processing metrics for claims agents and warranty assessors.

-   **[Summarize fraudulent claim detection using agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-summarize-fraudulent-claim-detection.md)**

    Anomaly-detection rules scan claim case lines against historical patterns and thresholds to identify fraudulent claims, flagging inflated amounts, frequency anomalies, and suspicious submission patterns. Claims meeting approval thresholds auto-approve with audit trail recording. Claims exceeding thresholds or exhibiting anomalies route to designated reviewers for investigation and disposition.

-   **[Create a product non-conformance case using playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-playbook-create-non-conformance.md)**

    QIM playbook enables you to create remediation action plans and access system-recommended correction actions. It automatically triages non-conformance records, assigns owners, and creates tasks based on historical patterns.

-   **[FSM integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-fsm-integration.md)**

    QIM integrates with FSM to support quality actions that require on-site intervention. When an NC or QI record identifies a need for field verification, containment, or remediation action, you can create an FSM work order directly from within QIM.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Change in this release

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## Activation information

Install Manufacturing Commercial Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Browser requirements

ServiceNow workspace doesn’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/browser-support.md).

## Related ServiceNow applications and features

-   **[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md).**

    Optimize the lead-to-cash cycle with Order Management for Manufacturing Commercial Operations.

    The following applications are supported for Manufacturing Commercial Operations:

    -   [Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/product-catalog-managment.md) enables you to create and manage product catalogs for commercial and technical product offerings.
    -   [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md) enables you to capture and fulfill product and service orders to create a seamless ordering experience for your customers.
    -   [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-management.md) enables you to set the pricing for your products.
-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    The Customer Service Management enables you to provide the service and support that your external customers need.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)**

    The ServiceNow Field Service Management application enables you to manage work orders and related tasks, resources, skills, assets, and locations.


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/new-features-changes.md)

