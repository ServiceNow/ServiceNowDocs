---
title: Integrate Workday professional worker profiles
description: Bring-in professional worker profile data from Workday into ServiceNow. View professional worker profile details from Workday in ServiceNow HR Service Delivery.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Integrate Workday professional worker profiles

Bring-in professional worker profile data from Workday into ServiceNow. View professional worker profile details from Workday in ServiceNow HR Service Delivery.

**Note:**

-   Professional worker profiles data is additional to the existing employee profile data. So, make sure you have the employee data available in your ServiceNow instance.
-   You need an active Employee definition to generate employee profiles. For more information, see [Create an active employee definition](../../employee-center/task/generate-profile-definition.md).

The following steps show how the professional worker profile data is imported into ServiceNow:

-   Activating and running the schedule flow **Run Workday Integration Flow** which contains the professional worker profile flow. For more information, see [Activating schedule flows](../task/activate-w-schedule-flow.md).
-   Selecting the **Professional worker profile** check box that activates the **Get Professional Worker Profile** subflow.
-   Activating **Get Professional Worker Profile Service**.
-   Initiates the **Look up Professional Profiles Stream** action.
-   Pulling data into the staging tables, and transform maps move data into target tables. For more information, see [Use transform maps](../reference/transform-maps-w.md).
-   Controlling access to the HR profile table with six Restricted caller access privileges \(RCAs\).

