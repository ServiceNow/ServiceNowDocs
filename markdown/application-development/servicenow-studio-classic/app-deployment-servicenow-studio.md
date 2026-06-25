---
title: App deployment in ServiceNow Studio
description: Deploy applications from ServiceNow Studio using several methods, including using deployment requests to move application and global file changes across instances. Deployment options depend on organizational preference and standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/app-deployment-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# App deployment in ServiceNow Studio

Deploy applications from ServiceNow Studio using several methods, including using deployment requests to move application and global file changes across instances. Deployment options depend on organizational preference and standards.

View and manage your deployment pipeline from within ServiceNow Studio, without switching to another application or environment.

## How are deployment requests created?

When a developer selects **Publish** in an application, a deployment request is created and displays on the **Deployment** section of the ServiceNow Studio homepage, on the **Deployment requests** tab.

Select a deployment record number to open it in a new tab, or select **New** to create a deployment request and attach update sets to it.

\[Omitted image "sn-studio-new-deployment-req.png"\] Alt text: Access, edit, or create deployment requests from the Deployment section on the home page.

## What options are available for app deployment?

Available deployment methods vary depending on if you're on the core UI or the Next Experience.

-   **Next Experience**

    **App Engine Management Center \(AEMC\)**: Deploy custom applications built in App Engine Studio, Creator Studio, and ServiceNow Studio across instances. AEMC uses Pipelines and Deployments to move applications between instances as they progress toward release. From AEMC, admins can customize pipelines, review and approve or reject deployment requests, and schedule deployments. For more information, see [App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/app-engine-management-center.md).

-   **Core UI \(lists and forms\)**

    **ReleaseOps**: Automates the deployment process using update sets and customizable pipelines. ReleaseOps orchestrates the entire process of deployment, including moving changes between instances, running scans and tests, and releasing changes, while providing transparency into the process for release managers and teams.

    **Application Repository**: Central location for all scoped applications that are published by all ServiceNow customers. After you develop and test a custom application, you can make the application available to company instances by publishing it to this repository.

    **Update sets**: Group of configuration changes that can be moved from one instance to another. Admins can group a series of changes into a named set and then move them as a unit to other systems for testing or deployment.


-   **[Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md)**  
Use update sets in ServiceNow Studio to group configuration changes and move them as a unit to other instances for testing or deployment.
-   **[Application Repository in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-the-app-repo-in-servicenow-studio.md)**  
Publish custom applications from ServiceNow Studio to the ServiceNow Application Repository to distribute them to other instances in the organization.
-   **[Pipelines in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-pipelines-servicenow-studio.md)**  
Use pipelines in ServiceNow Studio to automate the propagation and installation of applications from one instance to another. Admins manage deployment requests in the App Engine Management Center \(AEMC\).

**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/using-servicenow-studio.md)

