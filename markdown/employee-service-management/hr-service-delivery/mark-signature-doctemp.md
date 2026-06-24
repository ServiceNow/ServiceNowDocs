---
title: Mark a signature block
description: Specify the area in the PDF document where you want to collect the signatures of participants.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/mark-signature-doctemp.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Templates of type PDF \(Advanced forms\), Configuring Document Templates, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Mark a signature block

Specify the area in the PDF document where you want to collect the signatures of participants.

## Before you begin

Role required: sn\_doc.admin

**Important:** You can mark signatures only if you have defined participants and mapped users to those participants.

## Procedure

1.  Navigate to **All** &gt; **Document Template** &gt; **All Document Templates**.

2.  Select the PDF document template you want to use.

3.  [Configure a PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/configure-editable-pdf.md).

4.  [Create participants for a PDF document template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/create-participant.md).

5.  Click **Mark Signatures**.

6.  In the Mark Signature Blocks window:

    1.  Click **Add Field** and select the area where you want to collect the signature of a participant.
    2.  In the **Name** field, specify a name for the signature mapping record.
    3.  In the **Mapping** list, select a user from the mapped participants.
    4.  Click **Save**.
    \[Omitted image "mark-signature-blocks-dt.png"\] Alt text: How to mark signature blocks.

7.  Click **Submit**.

    The signature mapping is added to the PDF Template Mappings section.


