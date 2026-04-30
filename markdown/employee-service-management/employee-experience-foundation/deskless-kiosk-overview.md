---
title: Employee Center Pro Kiosk
description: Enable the field workers and shift workers with the in-context information for operational efficiency.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Employee Center Pro Kiosk

Enable the field workers and shift workers with the in-context information for operational efficiency.

A deskless worker is an employee who typically doesn’t sit behind a desk or use a computer to perform the job. Empowering deskless workers with resources is crucial for enhancing productivity, engagement, and overall organizational success.

A new plugin Employee Center Pro Kiosk enables all such deskless workers with simplified access to information and services for self-serve and improved productivity.

## Kiosk overview

Using the Kiosk application, deskless employees can manage their time off, schedule, and requests.

![Kiosk home page](../images/deskless-homepage-eck.png "Employee Center Pro Kiosk home page")

-   **One-stop source**: Meet employees where they’re and how they want to receive information and request services​.
-   **Guided experiences**: Empower the deskless employee workforce with relevant services and actions.
-   **Personalized self-service experience**: Access relevant information and services that help with day-to-day work.
-   **Feedback drawer widget**: Organizations can easily capture feedback on the Kiosk experience using the experience feedback drawer widget on the home page. For more information, see [Integrated experience and service feedback](ex-fdback-ovrvw.md).

**Note:** Employee Center Pro Kiosk \(sn\_ex\_sp\_pro\_kiosk\) home page is available with Employee Center Pro \(com.snc.employee\_center\_pro\) license.

Access all your information and services from a unified location from external applications such as Ultimate Kronos Group. Installation of the HR Service Delivery with the UKG plugin \(com.sn\_hr\_ukg\) provides a default setup of the UKG spoke. For more information, see [Integrate with the UKG spoke](../task/integrate-kiosk-kronos.md).

## Prerequisites

This portal supports displaying timeoff balance, employee schedule, my requests, and get support for deskless workers. Employee Center Pro Kiosk has a dependency on the following applications.

**Note:** Ensure you activate these applications first before installing the Employee Center Pro Kiosk app from ServiceNow Store.

-   Employee Center Pro \(sn\_ex\_sp\_pro\)
-   Employee Center \(sn\_ex\_sp\)
-   Employee Experience Foundation \(sn\_ex\_emp\_fd\)
-   Employee Profile \(sn\_employee\)
-   HR Service Delivery Integration with Ultimate Kronos Group \(sn\_hr\_ukg\)
-   UKG Spoke \(sn\_kronos\_spoke\)

    **Note:** Installation of the com.sn\_hr\_ukg plugin provides a default setup of the UKG spoke.

-   \(Optional\) Health and Safety Incident Management

    **Note:** To report health and safety, activate the plugin and apply the `sn_ohs_im.reporter` role.


## Kiosk users and roles

|User roles|Required role|
|----------|-------------|
|Kiosk admin|sn\_hr\_sp.esc\_admin|
|Kiosk user|sn\_ex\_sp\_pro\_kiosk.user|
|Employee profile admin|sn\_employee.admin|

**Note:** Ensure that the users have the `sn_ex_sp_pro_kiosk.user` role to access the Kiosk portal.

-   **[Employee Center Pro Kiosk benefits](deskless-kiosk-eck-benefits.md)**  
Enable the field workers and shift workers with the in-context information for operational efficiency.
-   **[Configure Employee Center Pro Kiosk](../task/deskless-kiosk-config.md)**  
Configure and use the default Kiosk for better deskless experience.
-   **[Customize Employee Center Pro Kiosk widgets](emp-center-topic-inst-options.md)**  
You can configure the widget instance options to control how data is displayed within the widget.
-   **[Configure the mail and SMS send to self](../task/deskless-kiosk-sendtoself-sms-email.md)**  
Help employees access information easily by sending required information as an SMS or email.
-   **[Integrate with the UKG spoke](../task/integrate-kiosk-kronos.md)**  
Integrate with the UKG spoke to use the Employee Center Pro Kiosk in your organization.
-   **[Use Employee Center Pro Kiosk](deskless-eck-homepage.md)**  
Use the Kiosk experience to self-serve, leading to improved productivity, and operational efficiencies for the organization.​

**Parent Topic:**[Employee Center Integrations](integrate-ec.md)

**Related topics**  


[Use Employee Center Pro Kiosk](deskless-eck-homepage.md)

[Integrated experience and service feedback](ex-fdback-ovrvw.md)

