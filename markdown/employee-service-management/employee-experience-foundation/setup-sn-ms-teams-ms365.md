---
title: Integrating ServiceNow with Microsoft 365 applications for Employee Experience
description: Set up your ServiceNow Employee Center instance to integrate Microsoft 365 applications.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Integrating ServiceNow with Microsoft 365 applications for Employee Experience

Set up your ServiceNow Employee Center instance to integrate Microsoft 365 applications.

**Important:**

-   From [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08/2.6.7?referer=%2Fstore%2Fproduct%2F9389b69edbb8e810d27e581adc9619ca) \(version 2.6.7\), ServiceNow for Microsoft Teams is upgraded to ServiceNow for Microsoft 365.
-   From [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2/3.3.6?referer=%2Fstore%2Fproduct%2F9389b69edbb8e810d27e581adc9619ca) \(version 3.3.6\), ServiceNow for Microsoft Teams is upgraded to ServiceNow for Microsoft 365.

For upgrading existing Microsoft Teams capabilities to Microsoft 365 applications, follow the steps given here.

The ServiceNow Employee Center integration with Microsoft Teams extends its capability to enable integration with other Microsoft 365 applications, bringing the ServiceNow employee experience to Microsoft Outlook, Microsoft Office 365, and Microsoft Teams together.

## Prerequisites

Before integrating Employee Center with your Microsoft 365 tenant, ensure that the following prerequisites are met:

-   You have the external app install admin \(external\_app\_install\_admin\) permissions on ServiceNow.
-   You have installed and deployed one of the following:

    -   IT Service Management for Microsoft 365
    -   HR Service Delivery for Microsoft 365
    For more information on how to install IT Service Management with Microsoft 365 or HR Service Delivery with Microsoft 365, see [Integrating ServiceNow with Microsoft Teams and Microsoft 365](setup-sn-ms-teams.md).


## Integration process for pre-published apps

1.  Upgrade to IT Service Management for Microsoft 365 / HR Service Delivery with Microsoft 365 by installing the latest IT Service Management for Microsoft 365 / HR Service Delivery with Microsoft 365 plugin.

    **Note:** For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

2.  Regenerate and download a new manifest file for Microsoft 365.

    For more information on how to generate and download the manifest file, see [Create and download manifest file for Employee Center and Microsoft 365 integration](../task/download-manifest-ms365.md).

3.  [Upload manifest file in Microsoft Teams for Microsoft 365](../task/upload-manifest-ms-teams-ms365.md).

## Integration process for self-configured apps

1.  Upgrade to IT Service Management for Microsoft 365 / HR Service Delivery with Microsoft 365 by installing the latest IT Service Management for Microsoft 365 / HR Service Delivery with Microsoft 365 plugin.

    **Note:** For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

2.  Authenticate users to access Employee Center in Microsoft 365 applications by updating the client IDs in the Microsoft Azure application.

<table id="table_obn_kbn_1yb"><thead><tr><th align="left">

Application

</th><th align="left">

Client ID

</th></tr></thead><tbody><tr><td>

Microsoft Teams mobile/desktop application

</td><td>

**1fec8e78-bce4-4aaf-ab1b-5451cc387264**

</td></tr><tr><td>

Microsoft Teams web application

</td><td>

**5e3ce6c0-2b1f-4285-8d4b-75ee78787346**

</td></tr><tr><td>

Microsoft 365 web application

</td><td>

**4765445b-32c6-49b0-83e6-1d93765276ca**

</td></tr><tr><td>

Microsoft 365 desktop application

</td><td>

**0ec893e0-5785-4de6-99da-4ed124e5296c**

</td></tr><tr><td>

Microsoft Outlook desktop application

</td><td>

**d3590ed6-52b3-4102-aeff-aad2292ab01c**

</td></tr><tr><td>

Microsoft Outlook web application

</td><td>

**bc59ab01-8403-45c6-8796-ac3ef710b3e3**

</td></tr><tr><td>

Microsoft Outlook mobile application

</td><td>

**27922004-5251-4030-b22d-91ecd9a37ea4**

</td></tr></tbody>
</table>    For more information on updating the Microsoft Azure application and authenticating users, see [Create Microsoft Azure application and authenticate users to access Employee Center in Microsoft Teams](../task/authenticate-users-your-hub-ms-teams.md).

3.  Regenerate and download a new manifest file for Microsoft 365.

    For more information on how to generate and download the manifest file, see [Create and download manifest file for Employee Center and Microsoft 365 integration](../task/download-manifest-ms365.md).

4.  [Upload manifest file in Microsoft Teams for Microsoft 365](../task/upload-manifest-ms-teams-ms365.md).

