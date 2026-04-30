---
title: Automatic case creation from emails
description: Cases are automatically created from incoming emails from shoppers based on the keywords used by them in the subject lines and bodies of the emails.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Advanced Work Assignment for Source-to-Pay Operations, Advanced Work Assignment for Source-to-Pay Operations, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Automatic case creation from emails

Cases are automatically created from incoming emails from shoppers based on the keywords used by them in the subject lines and bodies of the emails.

As an admin, you can set an email ID where all emails from shoppers are to be received. You can do this by navigating to **All** &gt; **Procurement Case Management** &gt; **Administration** &gt; **Procurement Properties**.

**Note:** The following are some examples of cases created from emails with specific keywords.

-   GL coding review cases are created from the keyword "accounting"
-   Contract review cases are created from the keyword "contract"
-   Sourcing related cases are created from the keyword "sourcing"
-   General inquiry cases are created from the keyword "information"

## Automatically create supplier case or procurement case from an inbound email

If you use the automatic case creation functionality in both Supplier Lifecycle Operations \(SLO\) and Sourcing and Procurement Operations \(SPO\), ensure that each instance is configured with a unique email address in the Automatic creation of cases from email property. This ensures the instance can correctly match incoming emails to the appropriate user and create the corresponding case.

For example:

-   In SLO, set the email address to supplierhelp@acme.com for creating supplier cases. For more information, see [Enable automatic creation of supplier cases from incoming emails](../../supplier-lifecycle-operations/task/config-email-properties.md).
-   In Sourcing and Procurement Operations, set the email address to procurementhelp@acme.com for creating procurement cases.

This approach enables seamless case creation and accurate email-to-user mapping.

**Parent Topic:**[Using Advanced Work Assignment for Source-to-Pay Operations](using-awa-spo.md)

