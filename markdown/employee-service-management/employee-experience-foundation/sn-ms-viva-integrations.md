---
title: Employee Center for Microsoft Viva Connections
description: The Employee Center for Microsoft Viva Connections integration extends the ServiceNow for Microsoft Teams integration, bringing the ServiceNow employee experience into the Microsoft Viva Connections dashboard.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Employee Center for Microsoft Viva Connections

The Employee Center for Microsoft Viva Connections integration extends the ServiceNow for Microsoft Teams integration, bringing the ServiceNow employee experience into the Microsoft Viva Connections dashboard.

Before installing Employee Center for Microsoft Viva Connections, ensure that the following prerequisites are met:

-   Your ServiceNow instances have been upgraded to Vancouver release.
-   You’ve installed and deployed the **IT Service Management for Microsoft 365\(sn\_now\_teams\_it\)** or **HR Service Delivery for Microsoft 365\(sn\_now\_teams\_hr\)** plugins.
-   You’ve installed and deployed Employee Center. For more information, see [Configuring Employee Center](../../employee-center/concept/setup-emp-center.md).
-   You've installed and deployed **Employee Center Core \(sn\_hr\_sp\)** August 23 store release version.

There are multiple admin roles required to deploy the Employee Center for Microsoft Viva Connections integrations application. The following table depicts the different admin roles required to perform various setup tasks in your environment.

<table id="table_m21_sy2_tqb"><thead><tr><th>

Activity

</th><th>

Role on ServiceNow

</th><th>

Role on Microsoft Azure portal

</th></tr></thead><tbody><tr><td>

[Install Employee Center for Microsoft Viva Connections application](../task/install-sn-ms-viva-connections.md)

</td><td>

External app install admin

</td><td>

NA

</td></tr><tr><td>

[Authorize Employee Center for Microsoft Viva Connections](../task/authorize-employee-experience.md)

</td><td>

External app install admin

</td><td>

Any of the following roles:

 -   [Application Administrator](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#application-administrator)
-   [Cloud Application Administrator](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#cloud-application-administrator)
-   [Global Administrator](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#global-administrator)
-   [Privileged Role Administrator](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#privileged-role-administrator)

</td></tr><tr><td>

[Update the Microsoft Teams application ID](../task/update-ms-teams-app-id.md)

</td><td>

External app install admin

</td><td>

Microsoft Teams administrator

</td></tr><tr><td>

[Download the Microsoft Viva solution package](../task/download-viva-package.md)

</td><td>

External app install admin

</td><td>

NA

</td></tr><tr><td>

[Deploy the Microsoft Viva integrations package in Microsoft SharePoint](../task/deploy-viva-sharepoint.md)

</td><td>

NA

</td><td>

Microsoft SharePoint administrator

</td></tr><tr><td>

[Enable the display of the Microsoft Viva card in Microsoft SharePoint](../task/grant-app-access-sharepoint.md)

</td><td>

NA

</td><td>

Microsoft SharePoint administrator

</td></tr></tbody>
</table>## Get started

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Integrate![Integrate](../../../common/image/icon-integrate.png)Integrate your Viva experience with Microsoft Teams and Employee Center.](integrate-viva.md)

</td><td>

[Configure![Configure](../../../common/image/icon-set-up.png)Plan and configure your implementation.](configure-viva.md)

</td></tr><tr><td>

[Manage![Manage](../../../common/image/icon-manage.png)Manage app access to deploy the Viva connections card.](manage-viva.md)

</td><td>

[Reference![Use](../../../common/image/icon-reference.png)Reference content for Viva connections.](reference-viva.md)

</td></tr></tbody>
</table>