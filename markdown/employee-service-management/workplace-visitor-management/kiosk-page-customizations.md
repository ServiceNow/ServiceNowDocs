---
title: Kiosk Page Customizations
description: The Page Configurations created for the Workplace Services Kiosk can be further customized by using their related lists.
locale: en-US
release: yokohama
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Kiosk Page Customizations

The Page Configurations created for the Workplace Services Kiosk can be further customized by using their related lists.

## Authentication Page

After creating an authentication page configuration, you can add the authentication options to the page. To add an authentication option from the Visitor authentication options list, select **New**, then fill in the Visitor authentication option form.

|Field|Description|
|-----|-----------|
|Authentication option|Option used for visitor authentication. For more information, see the following Authentication options table.|
|Page configuration|Authentication page configuration that the option is linked to.|

<table id="table_auth_options"><thead><tr><th>

Authentication option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Check-in with Qr-code

</td><td rowspan="2">

Visitor must scan the invitation QR code for authentication. The QR code is in the email invite that is sent to the visitor.**Note:** Ensure that the kiosk operator provides camera permissions on the kiosk to scan the QR code. For more information, see [Setting up a kiosk device](../../workplace-services-kiosk/concept/setting-up-kiosk-device.md#).

</td></tr><tr><td>

Check-out with Qr-code

</td></tr><tr><td>

Check-in with email address

</td><td rowspan="2">

Visitor must use their email address for authentication.

</td></tr><tr><td>

Check-out with email address

</td></tr><tr><td>

Check-in with invitation passcode

</td><td rowspan="2">

Visitor must use the invitation pass code for authentication. The pass code is in the email invite that is sent to the visitor.

</td></tr><tr><td>

Check-out with invitation passcode

</td></tr><tr><td>

Check-in with phone number

</td><td rowspan="2">

Visitor must use their phone number for authentication.

</td></tr><tr><td>

Check-out with phone number

</td></tr><tr><td>

Check-in with your name

</td><td rowspan="2">

Visitor must use their full name for authentication.

</td></tr><tr><td>

Check-out with your name

</td></tr></tbody>
</table>## End Page

After creating an end page configuration, you can add further steps for the visitor. To add a step from the Kiosk Next Steps list, select **New**, then fill in the Kiosk Next Step form.

|Field|Description|
|-----|-----------|
|Name|Name of the next step record.|
|Title|Title of the step on the kiosk end page.|
|Subtitle|Subtitle of the step on the kiosk end page.|
|Order|Order of the step. Steps with a higher order are displayed later in the page.|
|Page|End page that the record is linked to.|
|Active|Option to make the record active.|

**Parent Topic:**[Workplace Visitor Management references](../concept/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management](components-installed-with-workplace-visitor-mgmt.md)

[Properties installed with Workplace Visitor Management](properties-installed-with-workplace-visitor-mgmt.md)

[Kiosk Check-in Flow Configuration form](kiosk-check-in-config-form.md)

[Kiosk Check-out Flow Configuration form](kiosk-check-out-config-form.md)

[Kiosk Page Configuration form](kiosk-page-config-form.md)

[Location Policy form](location-policy-form.md)

