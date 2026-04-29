---
title: Integrating Workplace Services Kiosk with Workplace Visitor Management
description: Integrate Workplace Services Kiosk with Workplace Visitor Management to create a check-in, check-out, and self-registration experience for visitors.
locale: en-US
release: australia
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Integrating Workplace Services Kiosk with Workplace Visitor Management

Integrate Workplace Services Kiosk with Workplace Visitor Management to create a check-in, check-out, and self-registration experience for visitors.

## Integration Overview

1.  Create page configurations based on the flows you want to support on the kiosk. For more information, see [Configure pages for Workplace Services Kiosk](../../workplace-visitor-mgmt/task/create-kiosk-pages.md).

    The Authentication, Summary, and End page configurations are required to support check-in and check-out flows. The Self registration page configuration is required to support the self-registration flow. Additionally, you can create an acknowledgment page to display visitor policies on the kiosk.

    You can customize the initial and additional requirements for the self-registration flow. For more information about creating visit requirements, see [Configure visit requirements](../../workplace-visitor-mgmt/task/configure-visit-requirements.md).

    **Important:** If the visitor policies for the acknowledgment page contain hyperlinks, visitors can use the links to leave the kiosk environment and they cannot return to the kiosk. The kiosk operator must reload the kiosk environment by using the kiosk URL.

2.  Create check-in and check-out flows for the kiosk by using the page configurations. For more information, see [Create a flow for Workplace Services Kiosk](../../workplace-visitor-mgmt/task/create-kiosk-flow.md).

    Alternatively, you can use the default check-in and check-out flow that is included with the Workplace Visitor Management application.

    You can create multiple check-in and check-out flows and link them to different kiosk modules.

3.  Create a kiosk module and module configuration. For more information, see [Create a kiosk module](../task/create-kiosk-module.md).

    The kiosk module is linked to the check-in or check-out table to decide the flow and pages for the kiosk.

4.  Create a homepage configuration. For more information, see [Create a kiosk homepage](../task/create-kiosk-homepage.md).
5.  Create a kiosk configuration, assign the homepage configuration, and link the kiosk module you created. For more information, see [Create a kiosk configuration](../task/create-kiosk-device-config.md).
6.  Assign the kiosk configuration to a kiosk device. For more information, see [Setting up a kiosk device](setting-up-kiosk-device.md#).

After integrating Workplace Services Kiosk with Workplace Visitor Management, visitors can use the kiosk to check-in, check-out, or self-register. For more information, see [Using Workplace Services Kiosk](use-workplace-services-kiosk.md).

If an error occurs on the kiosk at run time, a generic error page is displayed to the user. As an admin, you can find information about the errors in the system logs. For more information about error scenarios, see [Workplace Services Kiosk error scenarios](../reference/wsd-kiosk-errors.md).

**Parent Topic:**[Integrating Workplace Services Kiosk](integrating-workplace-services-kiosk.md)

