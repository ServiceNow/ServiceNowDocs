---
title: Restructured Invoice table
description: The invoice and invoice line tables are restructured in the Xanadu release.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Post upgrade tasks for APO, Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Restructured Invoice table

The invoice and invoice line tables are restructured in the Xanadu release.

Before Washington DC release, invoice and invoice line tables were standalone tables. With Xanadu release, the following changes are done:

-   The invoice table \[sn\_shop\_invoice\] extends the base invoice table \[sn\_fin\_base\_invoice\].
-   The invoice line table \[sn\_shop\_invoice\_line\] extends the base invoice line table \[sn\_fin\_base\_invoice\_line\].

![Invoice table structure](../image/invoice-reparenting.png "Invoice Table structure")

After you upgrade from Washington DC to Zurich release, verify that your existing invoice and invoice line data has been migrated correctly. If you notice that your invoice and invoice line tables didn’t migrate properly, use the [Now Support Portal](https://support.servicenow.com/now) to raise a case with the Technical Support team.

**Related topics**  


[Application plugin installation sequence in Accounts Payable Operations](../reference/application-plugin-installation-sequence-apo.md)

