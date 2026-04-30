---
title: Kiosk Check-in Flow Configuration form
description: Use the Kiosk Check-in Flow Configuration form to create a check-in flow for the Workplace Services Kiosk.
locale: en-US
release: zurich
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Kiosk Check-in Flow Configuration form

Use the Kiosk Check-in Flow Configuration form to create a check-in flow for the Workplace Services Kiosk.

|Field|Description|
|-----|-----------|
|Name|Name of the check-in flow configuration.|
|Authentication page configuration|Page configuration that contains the check-in authentication.|
|Self-registration page configuration|Page configuration that contains the self-registration flow.|
|Acknowledgment page configuration|Page configuration that contains the check-in policies for the visitor to acknowledge. For more information about policies, see [Create a visitor policy](../task/create-visitor-policy.md).|
|Picture page configuration|Page configuration that uses the camera to take a picture of the visitor.|
|Summary page configuration|Page configuration that contains the summary of the visit.|
|End page configuration|Page configuration that displays the next steps for the visitor to follow.|
|Active|Option to make the page configuration active.|

**Note:** The Acknowledgment, Summary,Picture, and Self-registration pages are optional. If an optional page is not configured, it is skipped in the check-in flow.

|Scenario|Flow|
|--------|----|
|Authentication is successful|**Authentication page** &gt; **Summary page** &gt; **Picture Page** &gt; **Acknowledgement page** &gt; **End page** &gt; **Kiosk home page**|
|Authentication fails and self-registration is not configured|**Authentication page** &gt; **Authentication error** &gt; **Kiosk home page**|
|Authentication fails, self-registration is configured, and the visitor opts out of self-registration|**Authentication page** &gt; **Authentication error** &gt; **Self-registration page** &gt; **Kiosk home page**|
|Authentication fails, self-registration is configured, and the visitor opts to self-register|**Authentication page** &gt; **Authentication error** &gt; **Self-registration page** &gt; **Picture Page** &gt; **Acknowledgement page** &gt; **End page** &gt; **Kiosk home page**|

**Parent Topic:**[Workplace Visitor Management references](../concept/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management](components-installed-with-workplace-visitor-mgmt.md)

[Properties installed with Workplace Visitor Management](properties-installed-with-workplace-visitor-mgmt.md)

[Kiosk Check-out Flow Configuration form](kiosk-check-out-config-form.md)

[Kiosk Page Configuration form](kiosk-page-config-form.md)

[Kiosk Page Customizations](kiosk-page-customizations.md)

[Location Policy form](location-policy-form.md)

