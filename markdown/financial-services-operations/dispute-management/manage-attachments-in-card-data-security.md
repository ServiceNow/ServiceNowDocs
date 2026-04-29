---
title: Manage attachments in Card Data Security
description: Learn how attachments in the contextual side panel are handled in Card Data Security.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
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

![Transaction review page showing the Issuer tab in Attachments.](../image/card-data-security-issuer-attachments.png)

These files can be uploaded in the Attachments view, or from the task workspace.

![Transaction dispute form with document attachment area and attached customer purchase information file.](../image/card-data-security-txn-attach-docs.png)

Files that are received from card networks and stored in the tokenizer service are shown in the **Merchant** tab.

The files in the **Merchant** tab aren't stored in the ServiceNow instance; they are references to files that are stored in the tokenizer service vault to maintain PCI compliance. You can download these files to your device, or preview them directly from the tokenizer service vault so that they are not stored in your instance.

![Transaction review page showing the Merchant tab in Attachments.](../image/card-data-security-merchant-attachments.png)

