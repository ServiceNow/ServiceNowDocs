---
title: Sourcing and Procurement Operations integration with Third-party Risk Management
description: Leverage relevant supplier risk assessment capabilities by integrating Sourcing and Procurement Operations with Third-party Risk Management.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations integration with Third-party Risk Management

Leverage relevant supplier risk assessment capabilities by integrating Sourcing and Procurement Operations with Third-party Risk Management.

The following capabilities can be leveraged by customers if they have both the Sourcing and Procurement Operations and Third-party Risk Management applications installed:

-   Connection between the Company and Supplier tables through the **Related company** field. Also, leverage properties in the tables to synchronize other fields between the two tables at your own discretion.
-   Viewing tiering assessments and risk assessments for a vendor in the Supplier table.
-   Vendor Risk Reviewer role as a procurement specialist.
-   Adding members to the Governance, Risk, and Compliance \(GRC\) group, containing the new Purchasing Task Owner role.
-   Automation of the **Valid risk assessment** field in the Supplier table.
-   Enhancements to the existing Conduct a Supplier Risk Assessment case.
-   Creating a new Conduct a Supplier Tiering Assessment case. This is automatically triggered based on its requirement specified in the **Tiering assessment needed?** field in the Supplier table.

    **Note:** This is unique to the Risk Assessments Integration for Sourcing and Procurement Operations application and is not available if the customer has Sourcing and Procurement Operations alone.


## Risk Assessments Integration for Sourcing and Procurement Operations application

Customers can use the Risk Assessments Integration for Sourcing and Procurement Operations application for leveraging certain capabilities if they have both the Sourcing and Procurement Operations and Third-party Risk Management applications installed.

With this application, the **Related company** field is defaulted from the current application. This new reference field displays under the **Global company** field as a reference to the Company table. This field is only available when the Third-party Risk Management and Sourcing and Procurement Operations applications are installed. Also, the Tiering Assessments and Risk Assessments related lists in the Supplier table are only available when the Third-party Risk Management and Sourcing and Procurement Operations applications are installed.

## Company table connection

Two new fields are added, one in the Supplier table named **Related company**, and another in the Company table named **Supplier** that references the Supplier table.

When you open any existing supplier record in the Supplier table, you can link it to an existing record in the Company table with the **Related company** field. If that record does not exist, the procurement administrator creates a record in the Company table to establish the connection.

When you create a new supplier record in the Supplier table, a new vendor record is automatically created in the Company table with read-only reference to the Supplier table.

## Valid risk assessment visibility in the Supplier table

Tiering and risk assessments on a vendor can be created on the vendor record in the Third-party Risk Management application. These assessments are made visible in the Supplier table as related lists, to validate any supplier in Sourcing and Procurement Operations. A procurement specialist, containing the Vendor Assessment Reviewer role can read any vendor risk assessment data.

For information, see [Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/third-party-risk-mgt-landing-page.md).

## Valid supplier risk assessment

To determine if a supplier has a valid risk assessment, a scheduled job is run, and the customer’s system administrator can configure its frequency. This job keeps the **Valid risk assessment** field in the Supplier table up-to-date, based on the **Risk rating valid to** field on risk assessments in the Vendor Risk Assessments table.

A risk assessment is considered valid when:

-   Today's date is on or before the date defined in the **Risk rating valid to** field.
-   The value in the **Valid risk assessment** field in the Supplier table is Yes.

A Conduct a Supplier Risk Assessment case is created if a risk assessment is invalid. Risk assessments can be triggered manually by the Vendor Risk Manager, or automatically from any change in vendor tier rating.

## Enhancing the Conduct a Supplier Risk Assessment case

A Vendor Risk Manager can be assigned the Conduct a Supplier Risk Assessment case to validate a supplier's risks and to ensure that the supplier does not pose risks to the company.

The existing Conduct a Supplier Risk Assessment case is enhanced such that:

-   The GRC group contains the Purchasing Task Owner role, with visibility and access to the case.
-   The case has a related list of the risk assessments, both valid and expired, for better visibility.

## Creating a new Conduct a Supplier Tiering Assessment case

A new Conduct a Supplier Tiering Assessment case can be created in either of these methods, and assigned to the manager of the GRC group:

-   Automatically, triggered based on its requirement specified in the **Tiering assessment needed?** field in the Supplier table. If the risk rating of the related supplier is critical, high, or empty, a Conduct a Supplier Tiering Assessment case is auto-triggered.

    **Note:** This is unique to the Risk Assessments Integration for Sourcing and Procurement Operations application and is not available if the customer has Sourcing and Procurement Operations alone.

-   Manually, by a customer.

You can customize this case through the Supplier Tiering Assessment case templates, by defining the **Sourcing decision dependent on case** field to decide if this case should stop the sourcing request from moving into the Requires Decision state. The default value of this field is **Yes**. In this scenario, if all purchase requisition lines are in the Pricing Obtained state, and there are other cases still open, the sourcing request moves to the Awaiting Task Completion state. When the open cases are closed, the sourcing request moves to the Requires decision state. When the **Sourcing decision dependent on case** field is set to **No**, and if all purchase requisition lines are in the Pricing Obtained state, then the sourcing request will be in the same Pricing Obtained state even if other cases are open.

If the sourcing request gets converted to a purchase request, the case is available to be completed in the purchase requisition.

**Note:** All tiering assessments for a supplier are displayed in related lists.

For more information on sourcing requests, purchasing tasks, and procurement cases, see [Sourcing request](../reference/sourcing-request.md) and [Purchasing tasks and procurement cases](../reference/purchasing-tasks.md).

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management](spo-itam-better-together.md)

[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Project Management](integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[SpendInt APIs](spendint-api.md)

[Procurement File Transfer Framework](procurement-file-transfer-framework.md)

