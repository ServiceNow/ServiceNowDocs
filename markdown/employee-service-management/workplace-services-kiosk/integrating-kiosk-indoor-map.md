---
title: Integrating Workplace Services Kiosk with Workplace Indoor Mapping
description: Integrate Workplace Services Kiosk with Workplace Indoor Mapping to provide options to kiosk users to search for a space, get directions, and raise cases.
locale: en-US
release: zurich
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Integrating Workplace Services Kiosk with Workplace Indoor Mapping

Integrate Workplace Services Kiosk with Workplace Indoor Mapping to provide options to kiosk users to search for a space, get directions, and raise cases.

## Integration Overview

1.  Create a kiosk configuration that you want to use for indoor mapping. For more information, see [Create a kiosk configuration](../task/create-kiosk-device-config.md).

    You can also use existing kiosk configurations if they fit your requirement.

    **Note:** You can create a custom homepage for the kiosk configuration or use the default one. For more information about creating a homepage, see [Create a kiosk homepage](../task/create-kiosk-homepage.md).

2.  Create a map feature configuration from Workplace Central. For more information, see [Configure map features for kiosk](../../workplace-central/task/config-map-features.md).
3.  Set up the kiosk position and map settings. For more information, see [Configure the kiosk position and map settings](../../workplace-central/task/config-kiosk-map.md).
4.  Configure a module for the kiosk indoor map. For more information, see [Configure a module for kiosk indoor mapping](../../workplace-central/task/config-kiosk-ind-map-module.md).
5.  Assign the kiosk configuration to a kiosk device. For more information, see [Setting up a kiosk device](setting-up-kiosk-device.md#).

After integrating Workplace Services Kiosk with Workplace Indoor Mapping, kiosk users browse the workplace, search for spaces, get directions, and raise cases. For more information, see [Using Kiosk Indoor Mapping](using-kiosk-indoor-map.md).

If an error occurs on the kiosk at run time, a generic error page is displayed to the user. As an admin, you can find information about the errors in the system logs. For more information about error scenarios, see [Workplace Services Kiosk error scenarios](../reference/wsd-kiosk-errors.md).

The kiosk uses the **Kiosk general request** record producer to create a case from the **Raise an issue** modal. You can configure the record producer by navigating to **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Record producers**.

**Parent Topic:**[Integrating Workplace Services Kiosk](integrating-workplace-services-kiosk.md)

