---
title: Create a Vendor to a Vulnerability
description: Use this feature to create a vendor. Once created, you can associate the vendor to a product or link them to a vendor comment.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-02-25"
reading_time_minutes: 1
breadcrumb: [Vulnerability Artifacts, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a Vendor to a Vulnerability

Use this feature to create a vendor. Once created, you can associate the vendor to a product or link them to a vendor comment.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Library** &gt; **Vulnerability Artifacts** &gt; **Vendor**.

2.  Select **New**.

3.  Fill in the fields appropriately.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the vendor or supplying organization.|
    |Organization|The full legal or organizational name associated with the vendor.|
    |Description|A brief summary describing the vendor, their products, or their role in the context of the vulnerability.|
    |Website URL|The official website address of the vendor or organization.|
    |Contact Details|Contact information for the vendor, such as an email address, phone number, or support portal URL.|

4.  Click **Save**.

5.  To also add **Vendor Comments**, navigate to **Threat Intel Library** &gt; **Vulnerability Artifacts** and open any vendor record to which you want to add a comment.

6.  Go to the **Related Records** section.

7.  Scroll to the **Vendor Comments** related list and click **Add**.

    Clicking **Add** opens the Vulnerability Vendor Comment form in a new tab. The parent context \(vendor\) is automatically populated in the corresponding field. Enter the required form details as explained in the previous steps.

8.  Scroll to the **Vulnerability Vendor Comments** related list and click **Add**.

    The **Vendor** field is automatically populated with the current vendor record.

9.  Select the **Vulnerability** to which the comment applies.

10. Enter the vendor **Comment**.

11. Modify the **Comment Date**.

    The field defaults to current date.

12. Click **Save**.


## Result

The vendor comment is created and appears in the **Vulnerability Vendor Comments** related list of the vendor record.

**Parent Topic:**[Vulnerability Artifacts](../concept/vulnerability.md)

