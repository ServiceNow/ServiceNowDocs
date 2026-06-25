---
title: Use a flow or subflow in SAP Ariba \(Outbound\)
description: Execute a flow or subflow in SAP Ariba using the Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/use-subflow-sap-ariba.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use flows in SAP Ariba, Use, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use a flow or subflow in SAP Ariba \(Outbound\)

Execute a flow or subflow in SAP Ariba using the Workflow Studio.

## Before you begin

Role required: sn\_fcms\_intg.admin, sn\_shop.procurement\_specialist, connection\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **Flows**.

3.  Select the More icon \[Omitted image "more\_vertical\_icon.png"\] Alt text: More icon corresponding to the flow, subflow, or application name, use the filter condition, and select **Apply**.

4.  Select the required flow from the list.

    For example, select the **Create or Update Sourcing Event in SAP Ariba** flow.

    \[Omitted image "sap-ariba-trigger.png"\] Alt text: Overview of the Create or Update Sourcing Event in SAP Ariba flow

5.  In the Trigger field, specify the condition for the flow to run.

    This flow subsequently triggers subflows. To customize the sample flow, copy it to the desired application scope.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Use flows in SAP Ariba](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/use-flows-sap-ariba.md)

**Related topics**  


[Manually trigger flows or subflows in SAP Ariba \(Inbound\)]()

[Copy a flow or subflow in SAP Ariba]()

