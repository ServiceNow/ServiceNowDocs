---
title: Sourcing and Procurement Operations integration with third-party sourcing solutions
description: ServiceNow can integrate with third-party sourcing solutions to automate the sourcing process within the Sourcing and Procurement Operations product. A generic, easily configurable sourcing integration framework is provided within Source-to-Pay Integration Framework to enable you to specify the business criteria for triggering an integration. This integration framework can also integrate with multiple third-party sourcing solutions based on different criteria.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations integration with third-party sourcing solutions

ServiceNow can integrate with third-party sourcing solutions to automate the sourcing process within the Sourcing and Procurement Operations product. A generic, easily configurable sourcing integration framework is provided within Source-to-Pay Integration Framework to enable you to specify the business criteria for triggering an integration. This integration framework can also integrate with multiple third-party sourcing solutions based on different criteria.

Customers can either build the connector to that third-party tool or find one in the ServiceNow store.

For example, Fairmarkit, a third-party solution, built and certified its own ServiceNow application to the store, which leverages the integration framework to connect with the Fairmarkit system. For more information on this integration, visit [store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8bf60c3b979a3510a4ffb1511153afa2/1.0.4?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dfairmarkit&sl=sh).

For information on decision configuration, see [Decision configuration for third-party sourcing](decision-config-third-party-sourcing.md).

To learn about the integration tables, see [Integration tables for third-party sourcing](integ-tables-third-party-sourcing.md).

## Third-party sourcing integration process

-   If an integration is triggered, considering that applicable business criteria are defined in the decision table, and a request for pricing initiated by a shopper in ShoppingHub meets the criteria, one or more sourcing requests within a single purchase are automatically grouped into a single sourcing event. These are systematically created in the Sourcing and Purchasing Automation application.
-   When the negotiation setup playbook is complete, and the sourcing event is in the Work in Progress state, with the associated negotiations, sourcing requests, purchase lines, cases, and tasks in the Negotiation in Progress state, relevant data is populated in the Sourcing Outbound Queue, Sourcing Line Outbound Queue, and Sourcing Event Outbound Queue tables. This data can then be processed by the third-party solution accordingly, to initiate an RFx in their platform. Sourcing event is also created for the integrated sourcing request.

    **Note:** After a sourcing request is created and posted to the Sourcing Outbound Queue table, the third-party tool that is responsible for processing that sourcing request is identified and stored in the **Third party tool name** field.

-   A system property for the supplier responses close date \(sn\_spend\_intg.u\_bids.end.date\) sets the **Supplier responses close** field value on the sourcing event and sourcing requests to after the sourcing event has been created, plus the number of days defined. The default value is three days. The sourcing manager can override this value manually when updating this field on the sourcing event record.

    **Note:** A schedule job can be set up in the ServiceNow instance to check if the supplier responses close date has been reached \(aka today\). When done, ServiceNow stops receiving bids from suppliers and moves all individual supplier negotiations within the sourcing event to the Pricing Obtained state, and then to Requires Decision. The sourcing manager or fulfiller can then award a supplier with the business. The timestamp of the supplier responses close date is 23:59:59 of the day the bids close, in UTC date/time format. As the sourcing manager, you can also decide to close the bids now, with the date and timestamp of now, and proceed with the awarding flow without any wait time.

-   If the supplier responses close date changes on the sourcing request, then this update is sent to the Sourcing Outbound Queue table. The **Supplier responses close** field is updated. Also, if a sourcing request or purchase line is canceled, this status is also sent back to the sourcing request or purchase line outbound tables respectively.

    **Note:** The supplier responses close date is read-only on the sourcing request, but any change of the supplier responses close date on the sourcing event rolls up to the sourcing requests.

-   If there’s an error inserting new or updated records to this table, then the integration status is updated to Failed. The sourcing request at this point is in the Pending Resubmission state. The error details are captured in the **Processing Message** field and the integration error task is displayed. The procurement specialist must address the error and then resubmit both the sourcing requests and sourcing event by selecting the **Resubmit** button.

    **Note:** Currently, errors are logged only on the Sourcing Outbound Queue table.

-   Suppliers are invited to participate in a bid and engage through the third-party application platform.
-   When quotes are returned, the Sourcing Bid Stage table is populated by the third-party solution and the information is processed internally within ServiceNow using a transform map to populate the purchase lines on the sourcing request.

    **Note:** When an RFx is created or awarded in the third-party tool, shoppers and sourcing managers are notified through emails and alerts from Shopping Hub and Source-to-Pay Workspace respectively. Shoppers and sourcing managers are also notified about rejected bids, irrespective of the integration.

-   If additional supplier bids are returned from the third-party solution, an existing logic in ServiceNow determines if a new supplier, supplier product record, or both must be created.
-   After awarding is done in ServiceNow, that information is sent back to the third party using the Awarded Supplier Outbound Queue table. Awarding can also be done in the third-party tool, in which case the data is received by ServiceNow.

For information on sourcing request, negotiation, and sourcing event flows, see [Sourcing request](../reference/sourcing-request.md), [Negotiations](../reference/negotiations.md) and [Sourcing events](../reference/negotiation-events.md), respectively. For more information, see [Compare quotes and select a supplier](../task/work-compare-quotes-todos.md).

-   **[Decision configuration for third-party sourcing](decision-config-third-party-sourcing.md)**  
The Sourcing Event Generation Rule decision table in Sourcing and Procurement Operations helps the sourcing managers and procurement teams to configure the business criteria on demand, which provides them with flexibility to decide on the types of requests that should be integrated with a third-party sourcing solution.
-   **[Integration tables for third-party sourcing](integ-tables-third-party-sourcing.md)**  
Integration tables are used to interact with the third-party sourcing application. Relevant information that is required to conduct a Request for anything \(RFx\) in the third-party application is staged within ServiceNow and transferred through APIs to the third-party application.
-   **[Submit multi-product sourcing requests](../task/multi-product-sourcing-intake-with-third-party-integration.md)**  
Requesters can submit sourcing requests with multiple products in a single sourcing intake form. When a sourcing request form contains multiple products, the third-party sourcing solution automatically creates individual sourcing events for each product.
-   **[Manage third-party RFx tasks in Employee Center](../task/third-party-rfx-task-management-for-requestors.md)**  
Requesters can view and manage third-party Request for anything \(RFx\) tasks in the Employee Center and navigate to the third-party sourcing tool to review, publish, and award RFx.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management](spo-itam-better-together.md)

[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[SpendInt APIs](../../../integrate/inbound-rest/concept/spendint-api.md)

[Procurement File Transfer Framework](procurement-file-transfer-framework.md)

