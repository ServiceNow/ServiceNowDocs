---
title: Manually execute flows or subflows in SAP \(Inbound\)
description: You can manually trigger flows or subflows in SAP on demand. Follow these steps to manually trigger a flow or subflow.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Manually execute flows or subflows in SAP \(Inbound\)

You can manually trigger flows or subflows in SAP on demand. Follow these steps to manually trigger a flow or subflow.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select the **SAP** ERP source to manually trigger the flows or subflows.

    For example, SAP ECC, or SAP S4 HANA Cloud, or SAP HANA OData

3.  In the Integration Services list, select the subflows that you want to manually trigger.

    ![Manually trigger flows or subflows in SAP (Inbound)](../../source-to-pay-operations/image/sap-integration-manual-trigger-flow.png "Manually trigger flows or subflows in SAP")

4.  Select **Run job** to trigger the flow or subflow.

5.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

6.  From the Workflow Studio home page, select the **Operations** tab and then select **Flows** tab.

    The list of flow executions appear. You can look up the status of the flows or subflows that you triggered. If there were any errors during execution, you can view them under the processing message column.

7.  Navigate back to the **Homepage** tab, and select **Flows** or **Subflows**.

8.  Look up the **Flow** or **Subflow** name or **SAP ECC** or **SAP S4 HANA** application name using the filter icon, and select **Apply**.

    You can view the flows or subflows that you triggered.

    ![View the list of Flows or subflows in Workflow Studio](../../source-to-pay-operations/image/sap-integration-manual-trigger-ws.png "Flows or subflows in Workflow Studio")

9.  You can use the trigger condition as a part of the base system to execute the flow or subflow.

    **Note:** Don’t modify the trigger condition.

    The flow or subflow gets executed.


**Parent Topic:**[Configure the Source-to-Pay integration with SAP](../concept/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP](../concept/erp-source-configuration-sap.md)

[Define ERP source configuration for SAP](define-erp-source-sap.md)

[Configure integration services for SAP](configure-service-maps-sap.md)

[Look up primary data in SAP](../concept/look-up-primary-data-sap.md)

[Scheduled jobs to look up primary data in SAP](../concept/scheduled-jobs-to-primary-data-sap.md)

