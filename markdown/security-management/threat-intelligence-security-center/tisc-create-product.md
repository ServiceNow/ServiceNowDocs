---
title: Create a Product
description: Create New Product feature allows you to record the product’s version, vendor, and classification details, to ensure products are accurately linked to vulnerabilities and related records.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Vulnerability, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a Product

Create New Product feature allows you to record the product’s version, vendor, and classification details, to ensure products are accurately linked to vulnerabilities and related records.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Library** &gt; **Vulnerability Artifacts** &gt; **Product**.

2.  Select **New**.

3.  Fill in the fields appropriately.

    |Field|Description|
    |-----|-----------|
    |ID|Unique identifier for the product record.|
    |Name|Name of the product.|
    |Product Version|Specific version of the product.|
    |Product Version Range|Range of product versions to which the record applies.|
    |Product Family|Parent product or product line to which this product belongs.|
    |Is Product Group|Indicates whether the record represents a product group instead of a single product.|
    |CPE|Common Platform Enumeration \(CPE\) string that standardizes product identification.|
    |Vendor|Organization that develops or publishes the product.|
    |Architecture|System architecture supported by the product, such as x86 or ARM.|
    |Language|Language associated with the product or release.|
    |Host Name|Host system name associated with the product, if applicable.|
    |Patch Level|Patch level applied to the product version.|
    |Service Pack|Service pack applied to the product version.|
    |Specification|Additional specifications or details relevant to the product.|
    |Created in Source|Date when the product record was originally created in the source system.|
    |Last Modified in Source|Date when the product record was last updated in the source system.|
    |Status|Current state of the product record, such as Active or Inactive.|

4.  Click **Save**.

5.  Go to the **Related Records** section.

6.  Scroll to the **Product Identifiers** related list and click **Add**.

    Clicking **Add** opens the **Product Identifier** form in a new tab. The parent context \(product\) is automatically populated in the corresponding field. Enter the required form details.

    You can use the same process to add **Related Products**, **Product Vulnerabilities**, and **Product Vulnerability Remediations** records.

7.  Click **Save**.


## Result

The product identifier record is created and appears in the **Product Identifiers** related records of the **Product**.

**Parent Topic:**[Vulnerability](../concept/vulnerability.md)

**Related topics**  


[Create a CWE record](tisc-create-cwe-record.md)

[Create a Vendor to a Vulnerability](tisc-add-vendor-to-vul.md)

[Create Remediations](tisc-create-remediation-record.md)

