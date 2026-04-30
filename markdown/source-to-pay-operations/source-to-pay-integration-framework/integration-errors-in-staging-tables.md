---
title: Integration errors in staging tables
description: Integration errors caused by the target ERP sources are recorded in the form of system-generated integration error tasks \(outbound integration error\). You can view the integration tasks associated with Procurement and Sourcing Operations, Supplier Lifecycle Operations and Accounts Payable Operations in the Tasks area of the Source-to-Pay workspace.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Integration errors in staging tables

Integration errors caused by the target ERP sources are recorded in the form of system-generated integration error tasks \(outbound integration error\). You can view the integration tasks associated with Procurement and Sourcing Operations, Supplier Lifecycle Operations and Accounts Payable Operations in the **Tasks** area of the Source-to-Pay workspace.

The integration errors are categorized as:

-   Outbound integration Error-occurs when the outbound staging record is run and the sub flows in the target ERP source fails due to an error. Example: Connection error. The sub flow auto-updates the error message in the **Processing message** field of the outbound staging table and sets the **Integration status** to error. The system auto-creates error task for erroneous record and auto-assigns to a specialist.
-   Inbound integration error- Occurs when the inbound flow fails to fetch the primary data from the target ERP sources due to error in the master flow or ERP subflow. The **Error** field in the inbound staging table is auto-updated with the appropriate error message.

A specialist can reinitiate the integration activity after fixing the integration errors. Bulk records are integrated through scheduled jobs.

