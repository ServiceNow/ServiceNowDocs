---
title: Download Microsoft Outlook Add-In for Legal Service Delivery manifest file
description: As an admin, download Microsoft Outlook Add-In for Legal Service Delivery manifest file.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Outlook Add-In for Legal Service Delivery, Microsoft Outlook Add-In for Legal Service Delivery, Integration with Third-party applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Download Microsoft Outlook Add-In for Legal Service Delivery manifest file

As an admin, download Microsoft Outlook Add-In for Legal Service Delivery manifest file.

## Before you begin

Role required: sn\_lg\_outlook.admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow for Legal**.

3.  Select **Download Manifest** to download the file.

4.  If your ServiceNow instance is configured with single sign-on \(SSO\) login, update the manifest file.

    1.  Open the manifest file.

    2.  Locate the `AppDomains` element.

    3.  Add a `AppDomain` element and enter the SSO URL inside it.

        Example

        ```
        <AppDomains>
        <AppDomain><Instance URl></AppDomain>
        <AppDomain><SSO URl></AppDomain>
        </AppDomains>
        ```

    4.  Save the manifest file.


## What to do next

[Deploy Microsoft Outlook Add-In for Legal Service Delivery](lsd-enable-outllook-addin.md).

**Parent Topic:**[Configure Microsoft Outlook Add-In for Legal Service Delivery](../concept/lsd-outlook-addin-configure.md)

