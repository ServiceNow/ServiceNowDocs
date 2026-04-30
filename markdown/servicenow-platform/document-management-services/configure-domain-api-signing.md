---
title: Assign a custom signing domain for CAC/PIV digital signatures
description: Improve signing traffic management by assigning a custom domain for CAC/PIV digital signatures by setting an optional system property to override the default glide.servlet.uri setting.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [Set up a document template for signing documents, Digital signature for PDF documents using CAC or PIV smart cards, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assign a custom signing domain for CAC/PIV digital signatures

Improve signing traffic management by assigning a custom domain for CAC/PIV digital signatures by setting an optional system property to override the default **glide.servlet.uri** setting.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select **New** on the form header.

3.  In the **Name** field, enter `com.snc.pdfsigning.uri`.

4.  In the **Value** field, enter the custom domain URL.

5.  Select and hold \(or right-click\) the form header and select **Save**.


**Parent Topic:**[Set up a document template for signing documents using a CAC or PIV smart card](create-document-template.md)

