---
title: Activate the business rule for the Triage legal requests agentic workflow
description: Activate the business rules for the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application.
locale: en-US
release: xanadu
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Configuring the Triage legal requests agentic workflow, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Activate the business rule for the Triage legal requests agentic workflow

Activate the business rules for the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application.

## Before you begin

Role required: admin

## About this task

The Triage legal requests agentic workflow is shipped in an inactive state in the base system. To activate it, you must enable the business rule named the Trigger Triage Legal Request use case.

By default, the script include in this business rule contains the sys\_id of the Trigger Triage Legal Request use case. If you have a customized use case, you must update the script include in the business rule with the sys\_id of your customized use case.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    The Business Rules table appears.

2.  In the Name column, search for `Trigger Triage Legal Request use case`.

3.  Open the **Trigger Triage Legal Request use case** rule.

4.  Select the **Active** check box.

5.  For a customized agentic workflow, update **usecaseId** in the script with the sys\_id of the customized agentic workflow.

    1.  Navigate to the Advanced related list.

    2.  In the script, update the value for **usecaseId** with the sys\_id of the customized agentic workflow.

        ![Update the usecaseId with the sys_id of the customized agentic workflow.](../image/lsd-agentic-add-sys-id.png)

        To get the sys\_id of a customized use case, navigate to the use cases list, right-click the customized use case record, and select  **Copy sys\_id**.

6.  Select **Update**.


## Result

The Triage legal requests agentic workflow is activated for Now Assist for Legal Service Delivery \(LSD\).

