---
title: Managing app development using the App Engine Management Center
description: Track and manage your App Engine Studio \(AES\) and Creator Studio requests, deployments, applications, and collaborative developers using the App Engine Management Center \(AEMC\) in your production instance. Additionally, AEMC allows admins to manage app development from intake through production.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Managing app development using the App Engine Management Center

Track and manage your App Engine Studio \(AES\) and Creator Studio requests, deployments, applications, and collaborative developers using the App Engine Management Center \(AEMC\) in your production instance. Additionally, AEMC allows admins to manage app development from intake through production.

AEMC uses Pipelines and Deployments to deploy applications through different instances. Pipelines and Deployments uses the Application Repository to manage these deployments. For more information, see [ServiceNow application repository](../../applications/concept/app-repo.md).

Each application can either be deployed using the Application Repository or System Update Sets. If you've used Update Sets in the past, but want to switch to using the Application Repository, you can do a one-time conversion to deploy the app using the Application Repository instead. All apps don't have to follow the same deployment. For more information, see [Convert custom applications to upgrade from the application repository](../../applications/task/convert-custom-app-to-update-app-repo.md) and [System update sets](../../system-update-sets/concept/system-update-sets.md).

## Additional resources for App Engine Management Center

<table id="table_h24_rr5_gwb"><thead><tr><th>

Learn more about App Engine Management Center

</th><th>

ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

Although you can use AEMC in any instance, for full functionality, you must install AEMC in the production instance. You must also set up the deployment pipelines with the controller instance in production. For more information, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).

</td><td>

![](../../../reuse/icons/brand-icons/bus-try-a-demo.svg) [Govern low-code app development at scale with App Engine Management Center](https://www.youtube.com/watch?v=G-PcrtXs6GI)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-webinar.svg) [Creator toolbox \| App Engine Management Center](https://www.youtube.com/watch?v=fDvEqAQIHzQ)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [Govern low-code app development at scale with App Management Center](https://www.servicenow.com/demo/demonow-detail.html?videoid=govern-lowcode-app-development)

</td></tr></tbody>
</table>## Navigating AEMC

From the AEMC Overview screen, you can navigate to four additional views: Requests, Pipelines, Custom apps, and Developers by selecting icons in the primary navigation bar.

<table id="table_y5k_cl3_wtb"><thead><tr><th>

Page

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

High-level view of all intake,app, collaboration, and deployment requests, with a graph showing new requests of each type over the last 90 days. You can also see a high-level view of your pipelines and application metrics.

</td></tr><tr><td>

Requests

</td><td>

Full list of each request type broken down by approval status.

</td></tr><tr><td>

Pipelines

</td><td>

High-level view of the number of open deployment requests in each instance and within each pipeline. Selecting a pipeline or an environment in a pipeline displays all active deployment requests.**Note:** If you view deployment requests in a production instance, all **Closed - Published** deployment requests for that environment are listed.

</td></tr><tr><td>

Custom apps

</td><td>

Charts and graphs illustrating the status of your active applications, and a list of all custom apps in development or production. You can view details for individual apps, including usage information, deployment history, and collaborators.

</td></tr><tr><td>

Developers

</td><td>

Charts and graphs illustrating total and active developers, as well as developers by department. You can view details for individual developers, including the apps for which they are collaborators and their request history.

</td></tr></tbody>
</table>-   **[Managing requests using AEMC](manage-aemc-requests.md)**  
You can track and approve or reject Intake, App,Collaboration, and Deployment requests using the App Engine Management Center \(AEMC\).
-   **[Managing deployments using pipelines in AEMC](manage-deployments-using-aemc.md#)**  
Manage applications at all stages of deployment, view multiple pipelines, and approve or reject deployment requests using the App Engine Management Center \(AEMC\).
-   **[Managing custom apps using AEMC](manage-custom-apps-using-aemc.md)**  
Review custom app metrics and manage apps through the development life cycle using the App Engine Management Center \(AEMC\).
-   **[Managing developers using AEMC](manage-developers-using-aemc.md)**  
View details about developers working on apps in App Engine Studio and Creator Studio using App Engine Management Center \(AEMC\).

**Parent Topic:**[Build apps using App Engine Studio](aes-overview.md)

