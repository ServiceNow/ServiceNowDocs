---
title: Understanding Employee Center plugins
description: Discover the Employee Center plugins that are included out-of-the-box on a new ServiceNow instance, as well as plugins that are installed when you upgrade to Employee Center Pro.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Employee Center, Employee Service Management]
---

# Understanding Employee Center plugins

Discover the Employee Center plugins that are included out-of-the-box on a new ServiceNow® instance, as well as plugins that are installed when you upgrade to Employee Center Pro.

## Available out-of-the-box

New ServiceNow® instances include the Employee Center and dependency plugins. Review the following table to learn more about the plugins.

|Plugin|Description|
|------|-----------|
|Employee Center \(sn\_ex\_sp\)|Installs a customizable multi-department portal and framework to help administrators build a self-service portal that provides a great self-service experience for employees.|
|Employee Center Core \(sn\_hr\_sp\)|Activates a portal framework that allows administrators to build a mobile-friendly self-service experience for users.|
|Employee experience taxonomy \(sn\_ect\)|Provides an employee content taxonomy for multi-department service delivery.|
|Employee Experience Foundation \(sn\_ex\_emp\_fd\)|Contains components such as best practice email layouts that improve employee experiences.|
|Employee Profile \(sn\_employee\)|Enhance employee experience with a unified, configurable profile, offering comprehensive work-related information, extensibility across business units, and personalized visibility settings.|

## Installed with Employee Center Pro

The following dependency plugins are installed with Employee Center Pro.

<table id="table_kc2_q2v_q1c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Center \(sn\_ex\_sp\)

</td><td>

Installs a customizable multi-department portal and framework to help administrators build a self-service portal that provides a great self-service experience for employees.

</td></tr><tr><td>

Employee Center Pro \(sn\_ex\_sp\_pro\)

</td><td>

Employee Center Pro extends the standard Employee Center capabilities and provides a platform for employees to communicate and be engaged.[Install Employee Center Pro](../task/install-ec-pro.md)

</td></tr><tr><td>

Enterprise Service Management Integrations Framework \(sn\_hr\_integ\_fw\)

</td><td>

Enables Employee Center Pro to integrate with third-party systems.[Enterprise Service Management Integrations Framework](../../human-resources/concept/hr-integrations-framework.md)

</td></tr><tr><td>

Employee Center Core \(sn\_hr\_sp\)

</td><td>

Activates a portal framework that allows administrators to build a mobile-friendly self-service experience for users.

</td></tr><tr><td>

Employee experience taxonomy \(sn\_ect\)

</td><td>

Provides an employee content taxonomy for multi-department service delivery.

</td></tr><tr><td>

Employee Experience Foundation \(sn\_ex\_emp\_fd\)

</td><td>

Contains components such as best practice email layouts that improve employee experiences.

</td></tr></tbody>
</table>To learn about the tables, roles, and widgets installed, see [Components installed with Employee Center Pro](../reference/components-installed-with-employee-center-pro-1.md)

## Plugins to extend Employee Center Pro capabilities

The following plugins are available after you install Employee Center Pro. It is not required to install all the plugins, however some plugins depend on other plugins to function.

<table id="table_yb4_2fv_q1c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Profile \(sn\_employee\)

</td><td>

Enhance employee experience with a unified, configurable profile, offering comprehensive work-related information, extensibility across business units, and personalized visibility settings.

</td></tr><tr><td>

Content Publishing \(sn\_sd\)

</td><td>

Use Content Publishing to create different types of information you want to distribute to your employees. [Activate Content Publishing](../task/activate-content-delivery-plugin.md)

</td></tr><tr><td>

Communities \(com.sn\_communities\)

</td><td>

The Communities plugin supports [Employee Forums](ecpro-employee-forum.md#), where employees can connect, engage, and collaborate with each other.Requires Content Publishing \(sn\_sd\) and Content Experiences \(sn\_ca\)

[Activate Communities plugins](https://www.servicenow.com/docs/access?context=activate-communities&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Content Experiences \(sn\_ca\)

</td><td>

Package your content into a campaign using multiple channels to deliver the right message to the right audience at the right time. Requires Content Publishing \(sn\_sd\)

[Activate Content Experiences](../task/activate-content-automation-plugin.md)

</td></tr><tr><td>

Content Analytics \(sn\_cda\)

</td><td>

Content Analytics helps you decide when content is stale, needs refreshing, and how engaged your employees are with your communication. Requires Content Publishing \(sn\_sd\) and Content Experiences \(sn\_ca\)

[Activate Content Analytics](../task/activate-content-analytics-plugin.md)

</td></tr><tr><td>

Content Governance \(sn\_cg\)

</td><td>

Content Governance provides a streamlined way for employees to request content to be created, track the progress, preview the content, and approve it before it is published.Requires Content Publishing \(sn\_sd\) and Content Experiences \(sn\_ca\)

[Activate Content Governance](../task/ec-install-content-gov.md)

</td></tr></tbody>
</table>For more information, see the [List of plugins \(Xanadu\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **[Install Employee Center Pro](../task/install-ec-pro.md)**  
Employee Center Pro extends the standard Employee Center capabilities and provides a platform for employees to communicate and be engaged.
-   **[Activate Content Experiences](../task/activate-content-automation-plugin.md)**  
You can activate the Content Experiences \[sn\_ca\] plugin if you have the admin role to deliver targeted content and campaigns to keep employees informed and engaged. This plugin includes demo data and activates related plugins if they are not already active.
-   **[Activate Content engagement](../task/installing-content-engagement.md)**  
You can activate the Content Engagement \[sn\_ce\] plugin if you have the admin role to enable employee engagement activities \(reaction icons, comments, or sharing content\) with portal and mobile content.
-   **[Activate Content Publishing](../task/activate-content-delivery-plugin.md)**  
You can activate the Content Publishing if you have the admin role to distribute meaningful content to employees through multiple channels. This plugin includes demo data and activates related plugins if they are not already active. To use the Employee Communities feature, activate the Customer Communities \[com.sn\_customer\_communities\] plugin.
-   **[Activate Content Governance](../task/ec-install-content-gov.md)**  
You can install the Content Governance application \(sn\_cg\) to provide a streamlined method for employees to request content to be created for Content Publishing.
-   **[Upgrade to Employee Center Pro from Employee Service Center \(HR\)](../task/migrate-esc-ec.md)**  
Migrate to the Employee Center Pro portal to provide employees with a unified portal and content experiences.
-   **[Migrate to Employee Center from Service Portal](../task/migrate-sp-to-ec.md)**  
Migrate to the Employee Center portal to provide employees with a unified portal experience.
-   **[Post installation troubleshooting](post-install-steps.md)**  
To  index the  curated experiences  demo data into  search and recommended content   and allow all RCA privileges, run the fix scripts.
-   **[Enhanced chat in Employee Center](nass-now-assissist-self-service.md)**  
Learn more about the theme updates and how to get started with Now Assist enhanced chat.

**Parent Topic:**[Configuring Employee Center](setup-emp-center.md)

**Related topics**  


[Employee Center users and roles](emp-center-personas.md)

[Setup browse experience features](setup-browse-experience.md)

[Setup search experience features](setup-search-experience.md)

[Setup task management and integration features](setup-task-mgmt.md)

[Setup continuous improvement features](setup-continuous-improvement.md)

[Setup employee communications](setup-employee-comms.md)

[Configure your Employee Center portal](configure-ec-portal.md)

[Moveworks for Employee Center](moveworks-for-employeecenter.md)

[Employee Center Pro Kiosk](deskless-kiosk-overview.md)

[Configuring Employee Center for mobile](ec-mobile-configrations.md)

[Quick start tests for Employee Center](../../../administer/atf-quick-start-tests/reference/quick-start-tests-employee-center.md)

