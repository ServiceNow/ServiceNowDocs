---
title: Evaluate supplier risk using FedEx Dataworks risk assessment
description: FedEx Dataworks risk assessment returns logistics-based risk factor ratings for a matched supplier, helping relationship managers evaluate supplier risk during onboarding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/fedex-risk-assessment.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [FedEx risk assessment, supplier risk assessment, supplier onboarding, FedEx]
breadcrumb: [FedEx Dataworks Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Evaluate supplier risk using FedEx Dataworks risk assessment

FedEx Dataworks risk assessment returns logistics-based risk factor ratings for a matched supplier, helping relationship managers evaluate supplier risk during onboarding.

## Before you begin

Role required: sn\_slm.manager

FedEx Dataworks risk assessment is available only for suppliers that have a FedEx Dataworks Supplier ID. If supplier validation was not completed or returned no result, the risk assessment option is read-only and can't be selected.

## About this task

In the supplier onboarding playbook, FedEx Dataworks risk assessment is available as additional steps in the Qualification stage, after successful supplier validation. A relationship manager opts in to the assessment and submits a request. FedEx Dataworks evaluates the supplier and returns risk factor ratings within seconds.

**Risk factors**: Risk factors and their definitions are owned and maintained by FedEx Dataworks. FedEx Dataworks can add or remove risk factors at any monthly cycle.

**Risk assessment states**: The risk assessment flow in the onboarding playbook progresses through three states: Select, Run, and Results.

**FedEx Dataworks risk factor ratings**: Each risk factor is rated High, Medium, or Low. Ratings are color-coded: High is displayed in red, Medium in yellow, and Low in green.

**Risk assessment template**: A scheduled job runs on a monthly cycle to retrieve the latest risk assessment template from FedEx Dataworks. The template defines which risk factors are returned for any supplier assessment that month. The template applies to all suppliers globally for that month and is not supplier-specific.

## Procedure

1.  In the supplier onboarding playbook, when you reach the **Select risk assessments** step in the **Qualification** stage, select the **FedEx Dataworks Risk Assessment** check box to opt in.

    \[Omitted image "fedex-risk-assessment-select.png"\] Alt text: Select FedEx Risk Assessment

2.  Select **Run selected Assessments**.

    \[Omitted image "fedex-risk-assessment-run.png"\] Alt text: Running selected risk Assessment message

    An outbound request is sent to FedEx Dataworks for risk evaluation. Results are returned and displayed in the playbook within seconds.

3.  View the risk evaluation results.

    \[Omitted image "fedex-risk-assessment-result.png"\] Alt text: Risk evaluation results

<table id="table_mxr_fqd_rjc"><thead><tr><th>

Risk factor

</th><th>

Description

</th><th>

Measurement scale

</th></tr></thead><tbody><tr><td>

Origin country risk

</td><td>

Indicates if the given supplier address is in a restricted or sanctioned country, which may prevent shipping or require additional compliance steps.

</td><td>

Boolean \( Restricted=1, Unrestricted=0\)

</td></tr><tr><td>

Customs risk

</td><td>

Indicates the risk of customs delays or issues that may affect the shipment.

</td><td>

Percentile

</td></tr><tr><td>

Dangerous goods risk

</td><td>

Indicates the risk associated with the shipment of dangerous goods.

</td><td>

Percentile

</td></tr></tbody>
</table>
**Parent Topic:**[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

**Related topics**  


[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-dataworks-overview.md)

[Install the S2P Integration FedEx Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-fedex-connector.md)

[Validate supplier using FedEx Dataworks supplier validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-validation.md)

[View supplier metrics using FedEx Dataworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/fedex-supplier-performance-benchmarking.md)

