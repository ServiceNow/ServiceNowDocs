---
title: Asynchronous attachment uploads
description: Set the AsyncAttachmentsUploadEnabled mobile property to true to turn on background file uploads in the ServiceNow mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/asynchronous-attachment-uploads.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Asynchronous attachment uploads

Set the `AsyncAttachmentsUploadEnabled` mobile property to true to turn on background file uploads in the ServiceNow mobile app.

## Before you begin

Role required: **admin**

**Note:** The asynchronous attachment property is only supported on Input form and activity stream screens.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

3.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `AsyncAttachmentsUploadEnabled` to turn on asynchronous attachment uploads.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the **Overflows Menu** on the instance banner, then select **Scope selectors** &gt; **Application scope**: *application\_scope*.

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. For example: `Turns on background file uploads in the mobile app.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the `AsyncAttachmentsUploadEnabled` property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options: -   To turn on asynchronous attachment uploads, enter `true`.
-   To turn off asynchronous attachment uploads, enter `false`.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property is not activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the `AsyncAttachmentsUploadEnabled` property is included in the API response. Mobile properties with this check box enabled are excluded from the `/user_client` API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app.

</td></tr></tbody>
</table>4.  To configure the number of automatic retry attempts before an upload is marked as failed, create a second mobile property named `AsyncAttachmentsUploadNumRetriesBeforeFailure` using the same procedure, using type **Integer** and setting the value to the number of retries you want.

5.  Select **Submit**.


**Parent Topic:**[Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-properties.md)

