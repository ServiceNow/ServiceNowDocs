---
title: Application sharing
description: Administrators can share applications that are complete and are ready for use on other instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/c\_SharingApplications.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Administer your apps, Administering applications, Get started, Administer the ServiceNow AI Platform]
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

For applications that you are sharing, you can create a definition to track usage metrics on your application. For more information, see .

**Parent Topic:**[Administer your apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_ManagingApplications.md)

