---
title: Create a clause variation
description: As a contract configurator, create a clause variation to use in a contract template for predefined condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-add-clauses-doc-tmplt.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure dynamic clauses for contract templates, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create a clause variation

As a contract configurator, create a clause variation to use in a contract template for predefined condition.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## About this task

If you want the variables related to contract request to be available in condition builder, add the contract request reference to your application table. For more information, see [Enable contract request fields in condition builders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-add-cmr-condtion-build.md)

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Clause Management**.

2.  Select a clause.

3.  In the **Clause Variations** related list, select **New**.

    \[Omitted image "cmpro-clauseV-new.png"\] Alt text: Create a clause variation to use in a contract template for predefined condition

4.  On the form, fill in the fields.

    For more information on fields, see [Clause Variation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-cv-form.md).

5.  Right-click in the form header and select **Save**.

    -   The Clause Variation Fields related list appears.
    -   The imported document is parsed, and the content controls of type Field are extracted and displayed in the Clause Variation Fields related list.
    -   If you are editing a clause variation that is associated with a published contract template and have imported a document that has additional content controls, the unmapped content controls will be listed under the Unmapped metadata related list
6.  In the Clause Variation Fields related list, select a clause variation field.

    \[Omitted image "cmpro-clause-variation-field.png"\] Alt text: Select the clause variation field to view it's information

7.  On the form, view the following details.

    |Field|Description|
    |-----|-----------|
    |Clause Variation|This field is automatically set to the clause variation name.|
    |Document field title|Title of the content control.|
    |Document field tag|Tag of the content control.|
    |Read Only|Option to prevent this field from being edited.|

8.  In the Clause Variation Field form, save the meta data by selecting **Update**.

9.  In the Clause Variation form, save the clause variation by selecting **Update**.


**Parent Topic:**[Configure dynamic clauses for contract templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-clause-and-cv.md)

