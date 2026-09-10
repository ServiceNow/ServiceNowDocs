---
title: Create a Product
description: Create New Product feature allows you to record the product’s version, vendor, and classification details, to ensure products are accurately linked to vulnerabilities and related records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-create-product.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Vulnerability Artifacts, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
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

4.  Select **Save**.

5.  Select **Related Records** to perform one of the following actions.

    1.  Select an option to view the associated records.

    2.  Select **Link** and follow the modal to link a record.

    3.  Select **New** to create a product and link it to a related product or vulnerability.

    The **Link** and **New** buttons may not apply to all the record types.

6.  Scroll to the **Product Identifiers** related list and select **Add**.

    Clicking **Add** opens the **Product Identifier** form in a new tab. The parent context \(product\) is automatically populated in the corresponding field. Enter the required form details.

    You can use the same process to add **Related Products**, **Product Vulnerabilities**, and **Product Vulnerability Remediations** records.

7.  Select **Save**.


## Result

The product identifier record is created and appears in the **Product Identifiers** related records of the **Product**.

**Parent Topic:**[Vulnerability Artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/vulnerability.md)

**Related topics**  


[Create a CWE record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-cwe-record.md)

[Create a Vendor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-vendor-to-vul.md)

[Create Remediations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-remediation-record.md)

