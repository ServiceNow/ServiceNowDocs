---
title: Update sets in ServiceNow Studio
description: Use update sets in ServiceNow Studio to group configuration changes and move them as a unit to other instances for testing or deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-21"
reading_time_minutes: 2
breadcrumb: [App deployment in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Update sets in ServiceNow Studio

Use update sets in ServiceNow Studio to group configuration changes and move them as a unit to other instances for testing or deployment.

Update sets track configuration changes made in ServiceNow Studio so that admins and delegated developers can move those changes to other instances as a single deployable unit. Access update sets from within an individual application or from the **Deployment** tab. Update set interactions in ServiceNow Studio follow the same patterns as on the ServiceNow AI Platform. For more information about tasks you can accomplish with update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

Administrators can perform the following actions with update sets to control the full deployment lifecycle.

-   Create an update set to store local changes.
-   Select the current update set to direct where new local changes are recorded.
-   Commit an update set to prepare it for distribution.
-   Report on the contents of update sets.
-   Compare update sets to determine what differences they contain.
-   Merge separate update sets into a single update set.
-   Create an external file from an update set.
-   Retrieve update sets from remote instances to pull in changes made on other instances.
-   Apply retrieved update sets to install those changes on the current instance.
-   Back out changes applied from an update set.
-   Set system properties related to update sets to configure default update set behavior.
-   Promote update sets for deployment via ReleaseOps. For more information, see [ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/releaseops-landing.md).

Delegated developers can perform the following actions with update sets in ServiceNow Studio to manage changes within their assigned applications.

-   Create an update set to store local changes.
-   Switch between update sets using the update set picker.
-   Package changes for deployment using the **Publish** button in any app.

    **Note:** If your app was created in ServiceNow IDE and converted to Fluent, you must switch from ServiceNow Studio back into the ServiceNow IDE for the publishing and deployment process.


-   **[Create an update set in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-create-update-set.md)**  
Create an update set in ServiceNow Studio to package app changes for deployment to other instances.
-   **[Mark an update set complete in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/mark-update-set-complete.md)**  
Mark an update set as **Complete** in ServiceNow Studio to make the changes available for retrieval by other instances.

**Parent Topic:**[App deployment in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/app-deployment-servicenow-studio.md)

