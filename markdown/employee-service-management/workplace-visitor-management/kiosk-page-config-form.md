---
title: Kiosk Page Configuration form
description: Use the Kiosk Page Configuration form to create pages for the Workplace Services Kiosk.
locale: en-US
release: yokohama
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Kiosk Page Configuration form

Use the Kiosk Page Configuration form to create pages for the Workplace Services Kiosk.

<table id="table_tks_nnv_tbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the page configuration.

</td></tr><tr><td>

Title

</td><td>

Title that is displayed when the page is displayed on a kiosk.

</td></tr><tr><td>

Page type

</td><td>

Type of page that you want to create for the kiosk flow. For more information, see [Kiosk Check-in Flow Configuration form](kiosk-check-in-config-form.md).

</td></tr><tr><td>

Subtitle

</td><td>

Subtitle that is displayed when the page is displayed on a kiosk.

</td></tr><tr><td>

Application

</td><td>

Application scope of the page configuration record. This field is automatically filled based on the application scope of your instance.

</td></tr><tr><td>

Optional step

</td><td>

Option to allow kiosk users to skip taking a picture. This field appears only if the page type is **Picture**.

</td></tr><tr><td>

Always display policies

</td><td>

Option to always display the policies page, even if the visitor has accepted the policies earlier.

</td></tr><tr><td>

Record producer

</td><td>

Record producer that contains the self-registration logic. This field appears only if the page type is **Self-registration**.You can use the default **WSD VM Self registration** record producer that is included with the Workplace Visitor Management application.

</td></tr><tr><td>

Primary authentication option

</td><td>

Authentication option that opens by default on the authentication page. This field appears only if the page type is **Authentication**.**Note:** If the **Primary authentication option** field is not visible on the form, you must add it to the form layout. For more information about form layouts, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>## Self-registration record producer configuration

As an admin, you can configure the default record producer by navigating to **All** &gt; **Workplace Visitor Management** &gt; **Administration** &gt; **Record Producers**, then selecting the **WSD VM Self registration** record producer.

The Variables related list contains the variables that are included with the record producer. The following variables are not displayed on the kiosk:

-   **Location**: The location of the kiosk device determines the company policies and the list of hosts for the kiosk device.

    The location value is automatically filled at run time based on the kiosk configuration. For more information, see [Create a kiosk configuration](../../workplace-services-kiosk/task/create-kiosk-device-config.md).

-   **Duration**: The duration of the visit is used to determine the expected departure time of the visitor.

    The default value of the duration is **1h**, which specifies one hour. You can enter a combination of numbers with `h` to specify hours or `m` to specify minutes. For example, `5h` is five hours, `30m` is thirty minutes, `1h30m` is one hour and thirty minutes.


**Parent Topic:**[Workplace Visitor Management references](../concept/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management](components-installed-with-workplace-visitor-mgmt.md)

[Properties installed with Workplace Visitor Management](properties-installed-with-workplace-visitor-mgmt.md)

[Kiosk Check-in Flow Configuration form](kiosk-check-in-config-form.md)

[Kiosk Check-out Flow Configuration form](kiosk-check-out-config-form.md)

[Kiosk Page Customizations](kiosk-page-customizations.md)

[Location Policy form](location-policy-form.md)

