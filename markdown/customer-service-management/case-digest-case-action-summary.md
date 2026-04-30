---
title: Case action summaries
description: Use a case action summary to provide updates to customers and internal stakeholders while a case is in progress.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Case action summaries

Use a case action summary to provide updates to customers and internal stakeholders while a case is in progress.

Customer service agents typically use case action summaries to communicate information about high priority cases and mass outage cases. Case action summaries can include both internal content and customer-visible information. The summaries available to customers include only the customer-visible information. The summaries available to internal users include both customer-visible information and internal content.

Customer service agents can:

-   Create case action summaries for cases that are in progress.
-   Preview summaries prior to publishing.
-   Publish summaries to customers and internal stakeholders or publish to customers and send email notifications to internal stakeholders.
-   Update and re-send summaries as needed.

Customer service agents use the **Send Case Action Summary** UI action to create a case action summary. This action creates a case action summary record and adds the record to the Related Records section on the Case form in the **Case Action Summary** field.

Customer service agents can preview a case action summary before publishing it to a case. In the preview, internal content appears after the customer-visible information and is identified with a message: **The following content is not visible to customers.**

When publishing a case action summary, agents have two options.

-   When an agent clicks **Publish to Case**, the system takes the following actions:
    -   Adds the information from the customer-visible fields to the **Additional comments** field.
    -   Adds the information from all fields to the **Work notes** field.
-   When an agent clicks **Publish to Case &amp; Notify**, the system also sends an email notification with the case action summary to the internal users included in the recipient list selected in the **Additional internal recipients** field.

    **Note:** The **Publish to Case &amp; Notify** UI action is available when a list has been selected in the **Additional internal recipients** field.


Closing a case automatically closes the corresponding case action summary.

**Related topics**  


[Create a case action summary](../task/create-case-action-summary.md)

