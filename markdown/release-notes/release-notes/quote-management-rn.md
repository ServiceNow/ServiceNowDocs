---
title: Quote Management release notes
description: The ServiceNow Quote Management enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Quote Management release notes

The ServiceNow® Quote Management enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Australia release.

## Quote Management highlights for the Australia release

-   Quickly understand the financial outcome of quote changes, making it easier to review, approve, and act on updated quotes with visibility into exact amounts owed.
-   Enable sales agents to set a target outcome for a quote and let automated adjustments handle header-level discounting, removing manual trial-and-error and speeding up quote approvals.
-   Improve quote data consistency by validating contract start and end dates across quote headers, parent lines, and child lines, preventing date conflicts during updates.
-   Enable greater flexibility in managing amendment quotes by splitting active ramp segments into shorter intervals, adjusting quantities, and maintaining accurate line types throughout the quote life cycle.
-   Enhance quote approval workflows with automated reminders, escalations, override capabilities, and ad-hoc approvals for greater control and accountability throughout the approval process.
-   [Australia Patch 1](../quality/australia-patch-1.md)Summarize a quote with Now Assist for immediate, comprehensive insights into quote details \(product, pricing, and terms\) to improve quote accuracy, help teams align, reduce manual review, catch issues early, and accelerate quote turnaround.

See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=australia&pubname=australia-order-management&ft:locale=en-US) for more information.

**Important:** Quote Management is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

## New in the Australia release

-   **[Consolidate quotes](https://www.servicenow.com/docs/access?context=consolidate-quotes&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Maintain traceability from orders to all originating contract lines when creating orders from consolidated quotes. Additional calculated fields on order lines provide visibility into uplift values derived from consolidation rules.

-   **[Add price ramps on a quote line item](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Enable agents to create and manage custom ramp structures with flexible segment durations. Make ramp changes across the quote life cycle, including amendments and renewals, while maintaining pricing and quantity consistency across ramp segments.

-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Use the Advanced Approval Management to create approval workflows for end-to-end visibility and control of quote approvals.

    -   Track approval status, steps, sequencing, approvers, and comments in real time
    -   Manage quote states and edit permissions automatically as quotes move through Draft, In Review, Approved, and Rejected states
    -   Receive email notifications for approvers and requesters as approval actions are taken
    -   Configure approval conditions and sequencing across quotes, quote lines, and related entities using serial, parallel, or hybrid flows driven by business and compliance rules
    -   Preserve approval history across submissions and quote versions for a complete audit trail

-   **[Customer entities on Quote](https://www.servicenow.com/docs/access?context=quote-detail-form-fields&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Capture the deal type \(Direct or Indirect deals\) and align it with different routes to market for consistency, compliance, and operational efficiency across systems and teams.


-   **[Australia Patch 1](../quality/australia-patch-1.md)[Summarize a quote using quote summarization with Now Assist](https://www.servicenow.com/docs/access?context=summarize-quote&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Generate a summary of a quote to:

    -   Summarize key quote components during early customer discussions or pre‑discovery.
    -   Provide an updated view of the quote after revisions, without requiring review of multiple records.
    -   Provide a single, consolidated snapshot of all actions, tasks, and notes derived from a quote in one place.
    -   Highlight custom pricing, discounts, and negotiated changes made during the quoting process.
    -   Review the quote prior to sending it to the customer to confirm accuracy and completeness.
    -   Support internal handoffs by summarizing the quoted offer for internal teams.

## Changed in this release

-   **[Enhancements to price ramps on quote lines](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Modify active ramp segments on amendment quotes to better manage pricing changes over time.

    -   Split an active ramp segment into multiple shorter segments within the original term, with the system automatically assigning the correct line types and effective dates for each resulting segment.
    -   Merge split segments back into the original ramp while the quote is in draft state.
    -   Remove segments that are no longer needed.
    -   Edit the quantity in the product configurator. The quantity field for the last ramp segment of configurable and bundled products is read-only.
-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Build on existing quote approval workflows with greater control and flexibility

    -   Receive automated reminder notifications for pending approvals steps based on reminder schedules configured by your administrator.
    -   View the escalated approver on the approval step card when an approval step is escalated, so you can clearly identify who is responsible for the next action.
    -   Add ad-hoc approvers to an approval request outside the configured approval workflow when additional review is needed.
    -   Override an approval to advance a quote when permitted by your organization's approval configuration.

See [Advanced Approval Management release notes](advanced-approval-management-for-sales-rn.md) for more information.

## Activation information

Install Quote Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Advanced Approval Management](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Submit customer quotes for approval and track approval status using approval workflows created in Advanced Approval Management.

-   **[CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The CPQ Configurator interface streamlines the process of configuring and pricing customizable products in Sales Customer Relationship Management transactions, such as quotes and orders.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=australia&pubname=australia-order-management&ft:locale=en-US) application enables your pricing organization to set, manage, and optimize pricing strategies for any Sales Customer Relationship Management solution. These pricing strategies enable your sales teams to generate opportunities, quotes, and orders with accurate and competitive pricing quickly.

-   **[Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The Sales Agreement application captures the scope and conditions from a quote for future sales transactions, over a specified period between a buyer and a seller.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

