---
title: Approvals hub integration with SAP Concur
description: Enable easier access to all active approvals of external business applications such as SAP Concur from Employee Center Pro. The SAP Concur spoke is built by Bristlecone, Inc.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Approvals hub integration with SAP Concur

Enable easier access to all active approvals of external business applications such as SAP Concur from Employee Center Pro. The SAP Concur spoke is built by Bristlecone, Inc.

Using Approvals hub integration with SAP Concur, you can perform the following actions from Employee Center Pro:

-   Pull SAP Concur reports and expenses metadata into a ServiceNow application.
-   View the SAP Concur expense reports, expense line items, receipts, itemizations, and comments from your ServiceNow instance.
-   Enable approvers to view, send back, and approve the tasks right from Employee Center Pro.

## Prerequisites

Remember the following information before getting started with the integration:

-   Ensure you install the following plugins:
    -   Employee Center Pro
    -   SAP Concur spoke 2.0.0 and above **\(sn\_sap\_concur\_spok\)**
    -   Approvals hub integration with SAP Concur plugin **sn\_ex\_cnc**
    -   Enterprise Service Management Integrations Framework

        **Note:** This framework is installed with Employee Center Pro.

-   Approvals hub integration with SAP Concur is supported with Employee Center Utah patch 3 as the minimum supported release for the functionality to work on Utah.
-   Understand how Enterprise Service Management Integrations Framework works, see [Using Enterprise Service Management Integrations Framework](../../human-resources/task/use-integrations-framework.md) and [View tasks of a third-party system](../../human-resources/task/display-todos.md)
-   Integrate [Approvals hub integration with SAP Concur](x-concur-sa-integration.md) with ServiceNow, create credential records, and create connection records as explained in [SAP Concur Spoke](https://www.servicenow.com/docs/access?context=sap-concur-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
-   Understand the basics of [SAP Concur](https://api.sap.com/products/SAPConcur/overview) integrations and business processes.

**Note:** The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming. To automate the RCA approvals for any record, you can run the EC bulk RCAs approval script where the source scope is one of the Employee Experience applications.

## SAP Concur approvals workflow

By using the Employee Center Pro approvals experience, you can do the following actions:

-   Sync the SAP Concur expense reports to the **My tasks** page on Employee Center Pro.
-   View and manage the expense reports, expense line items, receipts, itemizations, and comments.
-   Enable approvers to perform quick actions such as approve or send back a request with comments.
-   Leverage Concur user flows and approval flows from approvals hub.

-   **[Manage approvals from SAP Concur](../task/x-concur-approvals.md)**  
As an administrator, you can sync, view, track, and fulfill the requests from other business applications such as SAP Concur from a unified Employee Center Pro location.
-   **[Populate SAP Concur report and metadata](../task/x-concur-approvals-scheduled-job.md)**  
As an administrator, fetch the reports metadata from other business applications such as SAP Concur. View the Concur expense reports, itemizations, and receipts from your ServiceNow instance.
-   **[Use task configuration for SAP Concur approvals](../task/approval-hub-to-dos-page-concur.md)**  
Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.

**Parent Topic:**[Approval hub integrations](approvals-int-concept.md)

