---
title: Create a coverage specification
description: Create a coverage specification in the Insurance claims application so that you can outline the scope and limits of the protection that is provided by an insurance policy.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Coverage specification, Setting up the policy data for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Create a coverage specification

Create a coverage specification in the Insurance claims application so that you can outline the scope and limits of the protection that is provided by an insurance policy.

## Before you begin

Role required: admin

## About this task

When creating the coverage specification, you also create the coverage types that act as the primary data for the coverage specification and the coverage type options for each coverage type.

For example, if the coverage specification is travel coverage, then you can select the following options:

-   A coverage type may be Baggage delay.
-   The coverage type options may be \(in U.S. dollars\) $200 \(24 hours\), $300 \(12 hours\), or $500 \(12 hours\).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Coverages** &gt; **Coverage specifications**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the coverage specification.|
    |Description|Brief description of the coverage specification.|

4.  Save the record.

5.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Coverages** &gt; **Coverage types**.

6.  Select **New**.

7.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Name|&lt;name of the coverage type&gt;|
    |Input type|Choice|
    |Type|Limit|
    |Scope|Policy|
    |Description|&lt;brief description of the coverage type&gt;|

8.  Select **Save**.

9.  In the Coverage Type Options related list, select **New**.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Option|Name of the coverage type option. For example, the option could be $200 \(24 hours\), $300 \(12 hours\), or $500 \(12 hours\).|
    |Coverage type|Coverage type that you created earlier.|
    |Order|Order in which this option is displayed for the coverage type.|

11. Repeat steps 9 and 10 for each coverage type option that is available.


## What to do next

Link the coverage types and coverage type options to the coverage specification that you created. For more information, see [Link the coverage types and coverage options to a coverage specification](linking-coverage-types-and-coverage-options-to-a-coverage-specification.md).

