---
title: App Engine Management Center user interface
description: Learn about the App Engine Management Center user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/aemc-user-interface.html
release: brazil
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AEMC user interface, App Engine Management Center UI, App Engine Management Center user interface]
breadcrumb: [Explore, App Engine Management Center, Governing app development, Building applications]
---

# App Engine Management Center user interface

Learn about the App Engine Management Center user interface.

The App Engine Management Center provides a centralized experience for all of your application development, deployment, and governance tasks.

## AEMC Overview page

The AEMC **Overview** page provides a high-level view of all intake, app, collaboration, and deployment requests for both App Engine and ReleaseOps deployments. You can also see insights into your developer and application metrics, and metrics about the releases that are in progress, upcoming, and already completed.

\[Omitted image "aemc-overview-page-bs1.png"\] Alt text: AEMC Overview page that shows requests, insights, developer, and app metrics.

## Navigating AEMC

From the AEMC **Overview** page, you can navigate to additional views: **Requests**, **Pipelines**, **Release management**, **Custom apps**, **Developers**, and **Developer Sandboxes** by selecting the view in the primary navigation bar.

<table id="table_y5k_cl3_wtb"><thead><tr><th>

Page

</th><th>

Description

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Requests

</td><td>

Complete list of each request type broken down by approval status. Requests include:-   Intake requests
-   App requests
-   Collaboration requests
-   Deployment requestsfor ReleaseOps deployments
-   Deployment requests - Legacy for App Engine deployments

</td><td>

[Managing requests using AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/manage-aemc-requests.md)

</td></tr><tr><td>

Pipelines

</td><td>

High-level view of the number of open deployment requests in each instance and within each pipeline. Selecting a pipeline or an environment in a pipeline displays all active deployment requests.**Note:** If you view deployment requests in a production instance, all **Closed - Published** deployment requests for that environment are listed.

</td><td>

[Configure Pipelines and Deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/config-p-and-d.md)

</td></tr><tr><td>

Release management

</td><td>

Available starting with version 28.2.1 of AEMC. Complete list of ReleaseOps releases and details about each release. When you select a release number, you can view the deployment requests associated with the release and monitor progress.

</td><td>

[ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/releaseops/releaseops-landing.md)

</td></tr><tr><td>

Custom apps

</td><td>

Charts and graphs illustrating the status of your active applications, and a list of all custom apps in development or production. You can view details for individual apps, including usage information, deployment history, and collaborators.

</td><td>

[Manage custom apps using AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/manage-custom-apps-using-aemc.md)

</td></tr><tr><td>

Developers

</td><td>

Charts and graphs illustrating total and active developers, and developers by department. You can view details for individual developers, including the apps for which they are collaborators and their request history.

</td><td>

[Managing developers using AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/manage-developers-using-aemc.md)

</td></tr><tr><td>

Developer Sandboxes

</td><td>

Enables the assignment of Developer Sandboxes licenses to different instances.

</td><td>



</td></tr></tbody>
</table>## Active deployment requests

The Active deployment requests in the pipeline section of the AEMC Overview page shows the number of apps at each deployment stage within each of your pipelines. You can select which pipeline is displayed or select **View all pipelines**. For the selected pipeline, you can select **Show requests** or **Show published requests** next to the corresponding sections to see an overview of each group of requests.

\[Omitted image "active-deployment-requests-in-pipeline-bs1.png"\] Alt text: The Active deployment requests in pipeline section shows the number of deployment requests currently in your pipeline and which instance they're located in.

For a full picture of all your pipeline deployment requests, access the Pipelines page in AEMC. View all of your pipelines, quickly access each deployment request record, and filter each pipeline section to see only the requests that match your criteria.

