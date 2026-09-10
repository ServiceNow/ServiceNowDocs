---
title: Create a Vendor
description: Create a vendor record to track organizations that supply products affected by vulnerabilities. Associate vendors with products or add vendor comments to document their responses and remediation guidance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-add-vendor-to-vul.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Vulnerability Artifacts, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a Vendor

Create a vendor record to track organizations that supply products affected by vulnerabilities. Associate vendors with products or add vendor comments to document their responses and remediation guidance.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Threat Intel Library**.

3.  **Vulnerability Artifacts** &gt; **Vendor**.

4.  Select **New**.

5.  Fill in the fields appropriately.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the vendor or supplying organization.|
    |Organization|The full legal or organizational name associated with the vendor.|
    |Description|A brief summary describing the vendor, their products, or their role in the context of the vulnerability.|
    |Website URL|The official website address of the vendor or organization.|
    |Contact Details|Contact information for the vendor, such as an email address, phone number, or support portal URL.|

6.  Select **Save**.

7.  To also add **Vendor Comments**, navigate to **Threat Intel Library** &gt; **Vulnerability Artifacts** and open any vendor record to which you want to add a comment.

8.  Go to the **Related Records** section.

9.  Scroll to the **Vendor Comments** related list and select **Add**.

    Clicking **Add** opens the Vulnerability Vendor Comment form in a new tab. The parent context \(vendor\) is automatically populated in the corresponding field. Enter the required form details as explained in the previous steps.

10. Scroll to the **Vulnerability Vendor Comments** related list and select **Add**.

    The **Vendor** field is automatically populated with the current vendor record.

11. Select the **Vulnerability** to which the comment applies.

12. Enter the vendor **Comment**.

13. Modify the **Comment Date**.

    The field defaults to current date.

14. Select **Save**.

15. Select **Related Records** to perform one of the following actions.

    1.  Select an option to view the associated records.

    2.  Select **Link** and follow the modal to link a record.

    3.  Select **New** to create a product and link it to the vendor.

    The **Link** and **New** buttons may not apply to all the record types.


**Parent Topic:**[Vulnerability Artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/vulnerability.md)

