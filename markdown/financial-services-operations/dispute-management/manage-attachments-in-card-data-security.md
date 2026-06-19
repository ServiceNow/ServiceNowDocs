---
title: Manage attachments in Card Data Security
description: Learn how attachments in the contextual side panel are handled in Card Data Security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/manage-attachments-in-card-data-security.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [manage attachments, card data security attachments, issuer tab, merchant tab, contextual side panel attachments, download documents vault, secure attachments, dispute transaction attachments, view documents tokenizer vault]
breadcrumb: [Use, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Manage attachments in Card Data Security

Learn how attachments in the contextual side panel are handled in Card Data Security.

## Attachments in Card Data Security

When Card Data Security is installed, the Attachments view in the contextual side panel displays attachments differently at the transaction level. It displays two tabs:

-   **Issuer**, which shows files added by the dispute agent.
-   **Merchant**, which shows files received from the card network, acquirer, or merchant, stored in the tokenizer service vault.

## Transaction record attachments

In a transaction record for a card dispute case, attachments added by an agent are shown in the **Issuer** tab.

\[Omitted image "card-data-security-issuer-attachments.png"\] Alt text: Transaction review page showing the Issuer tab in Attachments.

These files can be uploaded in the Attachments view, or from the task workspace.

\[Omitted image "card-data-security-txn-attach-docs.png"\] Alt text: Transaction dispute form with document attachment area and attached customer purchase information file.

Files that are received from card networks and stored in the tokenizer service are shown in the **Merchant** tab.

The files in the **Merchant** tab aren't stored in the ServiceNow instance; they are references to files that are stored in the tokenizer service vault to maintain PCI compliance. You can download these files to your device, or preview them directly from the tokenizer service vault so that they are not stored in your instance.

\[Omitted image "card-data-security-merchant-attachments.png"\] Alt text: Transaction review page showing the Merchant tab in Attachments.

