---
title: Workplace Services Kiosk error scenarios
description: Find the cause and related information of kiosk errors in the system logs.
locale: en-US
release: zurich
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Workplace Services Kiosk error scenarios

Find the cause and related information of kiosk errors in the system logs.

The Workplace Services Kiosk displays a generic error page to the user when an error occurs. As an admin, you can find information about the errors in the system logs. An error can occur in the following scenarios:

-   The kiosk doesn’t provide the required parameters.
-   The flow configuration record isn’t found in the Kiosk module configuration \[sn\_wsd\_kiosk\_module\_configuration\] table.
-   The indoor map configuration record isn’t found in the Kiosk indoor mapping configuration \[sn\_wsd\_indoor\_map\_kiosk\_configuration\] table.
-   The configured view type isn’t accessible by the kiosk viewer \[sn\_wsd\_kiosk.kiosk\_viewer\] role.
-   The configured campus isn’t part of the configured view type.
-   The floor where the kiosk camera is set isn’t part of the configured view type.
-   The floor where the kiosk is positioned isn’t part of the configured view type.

**Parent Topic:**[Workplace Services Kiosk reference](workplace-services-kiosk-reference.md)

