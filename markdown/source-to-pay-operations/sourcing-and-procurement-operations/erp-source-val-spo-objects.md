---
title: ERP source validation on Sourcing and Procurement Operations objects
description: Sourcing and Procurement Operations supports multi-ERP integration that enables you to use different ERP systems for different regions or lines of business, as required.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# ERP source validation on Sourcing and Procurement Operations objects

Sourcing and Procurement Operations supports multi-ERP integration that enables you to use different ERP systems for different regions or lines of business, as required.

Whenever Sourcing and Procurement Operations integrates with multiple ERPs, it validates the ERP from where the primary data is being fetched. It also ensures that the transaction data is routed to the right ERP with the right set of attributes. To validate ERP source to select correct attributes for Sourcing and Procurement Operations objects, and to support multi-ERP integration, these updates are enabled.

## Fx currency and conversion rates

Conversion rates from the Finance Exchange Rates \(sn\_fin\_fx\_rate\) table are used. This table has an ERP Source column, and records like purchase requisition and purchase order are also tied to the ERP Source column. By taking the legal entity and getting an ERP source from the legal entity, the right conversion rate is derived.

Fx2 currency amount is converted into your legal entity local currency amount and legal entity reporting currency amount by using the conversion rate from the Finance Exchange Rates table. All these converted values are stored in the PSM FX Currencies \(sn\_shop\_fx\_currency\_instance\)​ table.

## Shopping Hub

Foreign currency transactions are supported. A foreign currency transaction is one where the contract currency, also known as the transaction currency, is different from the local currency of the legal entity. For example, if an employee whose legal entity has a local currency of USD, purchases something which is in the contract currency of EUR, then it becomes a foreign currency transaction. In such cases,the contract amount is converted into the legal entity local currency in the shopping cart by using the exchange rate from the Finance Exchange Rates \(sn\_fin\_fx\_rate\) table, where the ERP source in the Finance Exchange Rates table matches with the ERP source or legal entity of the employee.

Also, purchase requisitions are split based on currency of the purchase requisition lines. Legal entity local currency is used to do the conversions during checkout.

## Cost center and GL account

Cost center and GL account values are restricted by the ERP source on the object. The legal entity from the object is considered, and the ERP source is fetched. When a user updates the record, only those cost centers that have matching ERP sources are displayed in the Source-to-Pay Workspace.

**Note:** These validations are enforced only when a legal entity has been set up for integration with ERPs. If you've set up integration with an ERP, then you’ll see the data having the same ERP source, thereby preventing downstream errors during integration.

If there’s any record with different ERP sources, then an integration error task is raised. This is an indicator for your fulfiller to correct the record before processing it further.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](../concept/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management](../concept/spo-itam-better-together.md)

[Sourcing and Procurement Operations integration with Employee Center](../concept/employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](../concept/psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](../concept/better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](../concept/integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](../concept/integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](../concept/integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](../concept/integration-spo-cmpro.md)

[SpendInt APIs](../concept/spendint-api.md)

[Procurement File Transfer Framework](../concept/procurement-file-transfer-framework.md)

