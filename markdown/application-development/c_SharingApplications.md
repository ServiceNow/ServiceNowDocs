---
title: Application sharing
description: Administrators can share applications that are complete and are ready for use on other instances.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer your apps, Deploying applications, Building applications]
---

# Application sharing

Administrators can share applications that are complete and are ready for use on other instances.

Application developers can share applications using one of the following methods.

|Sharing method|Makes available to|Typical use case|
|--------------|------------------|----------------|
|Publish to the application repository|All instances assigned to the same company|Transfer an application to a test or production environment.|
|Publish to the ServiceNow Store|All ServiceNow customers|Share or sell applications to other companies.|
|Publish to an Update Set|Any instance with access to the Update Set file|Save a version of an application for compliance or backup reasons.|
|Push to team development instances|Other instances in the team development environment|Push developer changes to the parent instance.|

**Note:**

“Tracking schema”: Deleting a table or a column in a scoped application is enabled by default for freshly zBooted instances. This is done by having the system property `com.glide.apps.include_my_schema` set to “true”.

For upgraded instances, if you have no custom applications installed or in development, “tracking schema deletes” is enabled by default. Otherwise the property is set to “false” so that customers get the same experience for schema deletes in their applications as in previous releases before Paris. To learn more see the [New York and Scoped Applications New Features](https://community.servicenow.com/community?id=community_blog&sys_id=ef21c1d21bf04c507a5933f2cd4bcb34) article on the ServiceNow Community site.

## Custom licensing for ISV applications

For applications that you are sharing, you can create a definition to track usage metrics on your application. For more information, see [Custom licensing for ISV applications](custom-licensing-isv-apps.md).

-   **[ServiceNow application repository](app-repo.md)**  
After you develop and test a custom application, you can make the application available to company instances by publishing it to the ServiceNow application repository.
-   **[Publish an application to the ServiceNow Store](../task/t_PublishAppsToTheServiceNowStore.md)**  
Publishing an application to the ServiceNow Store makes it available to everyone.
-   **[Create application files to include sample data](../task/t_IncludeApplicationData.md)**  
Include sample records from an application data table when sharing a custom application.
-   **[Publish an application to an Update Set](../task/t_PublishApplicationsToAnUpdateSet.md)**  
Publishing an application creates an update set containing the current version of all application configuration records.
-   **[Queued Application Operations](../task/queued-app-operations.md)**  
CICD APIs that must obtain the update **instance wide lock / mutex** to perform the requested operations are queued instead of being rejected when the update **instance wide lock / mutex** is occupied by the other operations.
-   **[Custom licensing for ISV applications](custom-licensing-isv-apps.md)**  
Monitor the usage of ISV applications with Subscription Management. Create a definition for your store application with the metadata you want collected. After publishing the application with the definition to the store, Usage Analytics runs and aggregates your defined metrics.

**Parent Topic:**[Administer your apps](../reference/r_ManagingApplications.md)

