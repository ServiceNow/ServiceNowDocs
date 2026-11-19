---
title: Image max dimension preset
description: Set the ImageMaxDimensionPreset mobile property to improve image uploads and make uploads faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/image-max-dimension-preset.html
release: brazil
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Image max dimension preset

Set the ImageMaxDimensionPreset mobile property to improve image uploads and make uploads faster.

## Before you begin

Role required: admin

**Note:** If the property is not set, the app does not resize images. The property applies to JPEG images only. Videos and other image formats are not affected.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_mobile\_properties**.

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

Name of the mobile property record. Enter `ImageMaxDimensionPreset` to resize image uploads.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(\) on the instance banner. Then select **Application scope**: *application\_scope*. For information about how mobile properties are affected by application scope, see [Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. For example: Scales JPEG images before uploading.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **String** for the `ImageMaxDimensionPreset` property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options \(not case-sensitive\). If the property isn't set or the value isn't one of these, the app does not resize images: -   To scale images to 960 px on the long side, select **low**.
-   To scale images to 1280 px on the long side, select **medium**.
-   To scale images to 1920 px on the long side, select **high**.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property is not activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the `ImageMaxDimensionPreset` property is included in the API response. Mobile properties with this check box enabled are excluded from the `/user_client` API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-properties.md)

