---
title: Link the coverage types and coverage options to a coverage specification
description: Link the coverage types and coverage options to a coverage specification in the Insurance claims application. This way, you associate all the available coverage types and options to the coverage specification and define the protections and risks that are covered by an insurance policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/insurance-claims/linking-coverage-types-and-coverage-options-to-a-coverage-specification.html
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Coverage specification, Setting up the policy data for Insurance claims, Configure, Insurance claims, Exploring insurance claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Link the coverage types and coverage options to a coverage specification

Link the coverage types and coverage options to a coverage specification in the Insurance claims application. This way, you associate all the available coverage types and options to the coverage specification and define the protections and risks that are covered by an insurance policy.

## Before you begin

Ensure you have created a coverage specification, coverage types, and coverage type options. For more information, see [Create a coverage specification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/insurance-claims/creating-a-coverage-specification.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Coverages** &gt; **Coverage specifications**.

2.  Search for the coverage specification record and open it.

3.  In the Product Coverage Types related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Coverage type|Coverage type that applies to this coverage specification.|

5.  Save the record.

6.  In the Product Coverage Type Options related list, select **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Coverage type option|Coverage type option that applies to this coverage type.|

8.  Select **Submit**.

9.  Repeat steps 6 through 8 for each coverage type option that you created.

    The following example shows how a coverage type is set up in the travel insurance example in this application. The coverage specification Travel guard basic coverage has a coverage type of Baggage delay, and the available coverage type option is $200 \(24 hrs\).\[Omitted image "coverage-type-setup.png"\] Alt text: Baggage delay coverage type with a coverage type option, set up for a travel coverage specification.

10. Select **Update**.


