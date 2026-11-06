---
title: Configure impact ratings
description: Configure an impact rating to assess an impact category as low, moderate, high, or critical. Use the Impact Ratings module in the Business Continuity Management application navigator to help you measure the intensity of the loss when a business downtime occurs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/configure-impact-rating-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure impact ratings

Configure an impact rating to assess an impact category as low, moderate, high, or critical. Use the **Impact Ratings** module in the Business Continuity Management application navigator to help you measure the intensity of the loss when a business downtime occurs.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Impact Ratings**.

2.  Select **New**.

    The impact rating template is shown in the example.

    \[Omitted image "impact-rating-new.png"\] Alt text: Impact rating template.

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [Impact Rating record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/impact-rating-new-record-form.md).

    The example shows an impact rating from the demo data.

    \[Omitted image "impact-rating-example.png"\] Alt text: Impact rating example.

    For example, create ratings for `Customer impact`, each with a description:

    -   `Low` \(Value `1`; `Tolerable`\)
    -   `Medium` \(Value `2`; `Not tolerable`\)
    -   `High` \(Value `3`; `Tolerable`\)
    -   `Critical` \(Value `4`; `Not tolerable`\)
    Similarly, create ratings for `Operational impact` the same way:

    -   `Low` \(Value `1`; `Not tolerable`\)
    -   `Medium` \(Value `2`; `Tolerable`\)
    -   `High` \(Value `3`; `Not tolerable`\)
    -   `Critical` \(Value `4`; `Tolerable`\)
4.  Select **Submit**.


-   **[Impact Rating record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/impact-rating-new-record-form.md)**  
Use the Impact Rating record form to assess an impact category such as low, moderate, high, or critical by using BCM UIB Workspace.

**Parent Topic:**[General administration setup for BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/set-up-bcm-bcmadmin-tasks.md)

