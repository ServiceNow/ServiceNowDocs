---
title: Validate supplier using FedEx Dataworks supplier validation
description: Supplier validation connects a supplier's location to a FedEx Dataworks record, returning a FedEx Dataworks Supplier ID that unlocks risk assessment and performance benchmarking data for that supplier.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [supplier validation, supplier onboarding, FedEx]
breadcrumb: [FedEx Dataworks Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Validate supplier using FedEx Dataworks supplier validation

Supplier validation connects a supplier's location to a FedEx Dataworks record, returning a FedEx Dataworks Supplier ID that unlocks risk assessment and performance benchmarking data for that supplier.

## Before you begin

Role required: sn\_slm.manager

## About this task

In the supplier onboarding playbook, FedEx Dataworks supplier validation appears as additional steps in the Registration stage. A relationship manager selects the supplier's location and sends a match request to FedEx Dataworks. FedEx Dataworks searches its records for the supplier and returns a result.

**Note:** This step is optional. Relationship managers can skip supplier validation and continue the onboarding playbook without FedEx Dataworks data. If supplier validation is skipped or returns no result, FedEx Dataworks risk assessment and performance benchmarking data aren't available for that supplier.

For more information about the regular onboarding process without FedEx Dataworks, see [Use the supplier onboarding playbook to onboard suppliers](https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/use-playbooks-onboard-supp.html).

## Procedure

1.  In the supplier onboarding playbook, navigate to the **Registration** stage.

    Complete the initial steps and navigate to the **Confirm supplier information for FedEx Dataworks matching** step.

2.  Select the supplier's location from the location field.

    The location field defaults to **Headquarters**. You can select an alternate location if the supplier has multiple locations registered in the system.

3.  Select **Check supplier with FedEx Dataworks** or **Sync check supplier with FedEx Dataworks** to submit the supplier validation request to FedEx Dataworks.

    \[Omitted image "fedex-supplier-address-matching.png"\] Alt text: Select supplier info and submit request for FedEx Dataworks supplier matching

    Supplier Lifecycle Operations sends the supplier's details \(including the DUNS number\) and location to FedEx Dataworks using an outbound request table.

4.  Wait for the validation response from FedEx Dataworks.

    FedEx Dataworks app on the platform listens to the outbound request table and populates the response. This typically takes a few seconds to complete.


## Result

One of the following outcomes occur:

-   **FedEx Dataworks recognizes the supplier**: A FedEx Dataworks Supplier ID is returned and stored on the supplier record. FedEx Dataworks risk assessment and performance benchmarking is set to available.

    \[Omitted image "fedex-supplier-address-success.png"\] Alt text: FedEx Dataworks recognizes the supplier message

-   **FedEx Dataworks does not recognize the supplier**: A "no supplier found" response is returned. No FedEx Dataworks data is displayed for that supplier.

    \[Omitted image "fedex-supplier-address-failed.png"\] Alt text: Supplier validation failure message

    You can retry with the **Resync check supplier with FedEx Dataworks** button or skip the FedEx Dataworks check.

-   **Supplier validation is skipped**: No FedEx Dataworks Supplier ID is assigned.

    FedEx Dataworks risk assessment and performance benchmarking aren't available for that supplier. The message times out after one minute.


**Note:** While the supplier validation is in progress, you can still go ahead and continue with the next step of risk assessment with Third-Party Risk Management \(TPRM\). However, FedEx Dataworks risk assessment and FedEx Dataworks supplier performance benchmarking will not be activated unless supplier validation is completed.

## What to do next

After successful supplier validation, you can proceed with FedEx Dataworks risk assessment during the Qualification stage of the onboarding playbook.

**Parent Topic:**[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

**Related topics**  


[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)

[Evaluate supplier risk using FedEx Dataworks risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.md)

[View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md)

