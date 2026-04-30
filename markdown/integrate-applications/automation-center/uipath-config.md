---
title: Configuring UiPath with Automation Center
description: Easily view and analyze UiPath data from Automation Center.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Automation Center, Automation Center, Creating integrations with applications]
---

# Configuring UiPath with Automation Center

Easily view and analyze UiPath data from Automation Center.

You can view and analyze UiPath data in Automation Center using the Automation Center API and UiPath spoke. However, using UiPath spoke is more efficient and less time-consuming.

Before configuring UiPath with Automation Center, you must install the UiPath spoke on your instance. For more details, see [UiPath spoke](../../../administer/integrationhub-store-spokes/concept/uipath-spoke.md).

After the UiPath spoke is installed, the following two options are available:

-   UiPath Webhook Registries
-   UiPath WebHook Routing Policies

If an issue occurs while processing the UiPath data, an error message along with the actual payload is inserted as a record in the Import Error Log \[sn\_ac\_import\_error\_log\] table.

**Note:** The number of days the error records will be stored in the table is defined in the Automation Center purge system property \(sn\_ac.purge\_automation\_data\_in\_days\).

-   **[Create UiPath webhook registry](../task/webhook-registry.md)**  
Create UiPath webhook registries to establish a connection between UiPath and Automation Center.
-   **[Set UiPath WebHook routing policies](../task/routing-policies.md)**  
Set the UiPath WebHook routing policies to enable the data to get populated in the ServiceNow tables, and then used by Automation Center.

**Parent Topic:**[Configuring Automation Center](automation-center-setup.md)

