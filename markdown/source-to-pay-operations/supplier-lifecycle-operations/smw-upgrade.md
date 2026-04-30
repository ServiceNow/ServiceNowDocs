---
title: Prerequisites for upgrading Supplier Lifecycle Operations to Washington DC or later releases
description: Starting with the Washington DC release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden from the navigation and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Prerequisites for upgrading Supplier Lifecycle Operations to Washington DC or later releases

Starting with the Washington DC release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden from the navigation and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.

**Important:** The Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management in the Yokohama December 2025 \(v 5.2.0\) release.

Supplier managers are often part of procurement, which involves sourcing products and selecting the supplier that best fits the needs. As a result, the supplier manager had to switch between two different workspaces, which affected the user experience.

The Source-to-Pay \(S2P\) product suite utilizes the Source-to-Pay Workspace for various activities such as procuring goods, onboarding suppliers, and processing invoices. This unified workspace is designed to streamline tasks for Procurement Specialists, Supplier Managers, and Accounts Payable Specialists by providing a consistent interface for Source-to-Pay Operations. For more information, see [Source-to-Pay Workspace](../../source-to-pay-operations/concept/source-to-pay-ws-overview.md).

Before upgrading to Washington DC or later releases, ensure that you have installed the Vancouver version 2.4.2 of both Supplier Common Architecture and Supplier Lifecycle Operations. This step is mandatory if you plan to continue using the deprecated Supplier Manager Workspace. For more information, see the KB article [KB1651502](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651502).

If you have upgraded to Washington DC or later releases and want to use the Supplier Manager Workspace, ensure that you run the fixscript\_migrate\_workspace\_to\_smw.xml fix script. For more information, see [Run fix script to migrate existing data from the deprecated Action type column after upgrade](../task/fix-script-deprecated-column.md).

**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

