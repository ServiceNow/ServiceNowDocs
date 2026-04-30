---
title: Manually trigger flows or subflows in SAP Ariba \(Inbound\)
description: You can manually trigger flows or subflows in SAP Ariba on demand.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use flows in SAP Ariba, Use, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Manually trigger flows or subflows in SAP Ariba \(Inbound\)

You can manually trigger flows or subflows in SAP Ariba on demand.

## Before you begin

Role required: sn\_fcms\_intg.admin

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select the **SAP Ariba REST** ERP source to manually trigger the flows or subflows.

3.  In the Integration Services list, select the subflows that you want to manually trigger.

4.  Select **Run job** to trigger the flow or subflow.

    ![Select and run the subflows](../image/sap-ariba-run-job.png "Run subflows in SAP Ariba")

5.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

6.  From the Workflow Studio home page, select the **Operations** tab and then select **Flows** tab.

    ![List of executed flows in SAP Ariba](../image/sap-ariba-flow-execution.png "Flow execution in SAP Ariba")

    The list of flow executions appear. You can look up the status of the flows or subflows that you triggered. If there were any errors during execution, you can view them under the processing message column.

7.  Navigate back to the **Homepage** tab, and select **Flows** or **Subflows**.

8.  Select the More icon ![More icon](../../sourcing-procurement-operations/image/more_vertical_icon.png) corresponding to the flow, subflow, or application name, use the filter condition, and select **Apply**.

    ![Filter the subflows](../image/sap-ariba-filter-flow.png "Filter flow, subflow, or application")

    You can view the flows or subflows that you triggered.

9.  Use the trigger condition defined in the base system, to execute the flow or subflow.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Use flows in SAP Ariba](../concept/use-flows-sap-ariba.md)

**Related topics**  


[Use a flow or subflow in SAP Ariba \(Outbound\)](use-subflow-sap-ariba.md)

[Copy a flow or subflow in SAP Ariba](copy-subflow-sap-ariba.md)

