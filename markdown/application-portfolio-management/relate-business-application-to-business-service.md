---
title: Relate business application to application service using CI relationship editor
description: Business applications can have multiple instances. Application instances are nothing but application services. Relate business applications to instances by relating business applications to application services. Business application and application service are two different configuration items which must be related through a CI relationship.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-portfolio-management/relate-business-application-to-business-service.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Relate business application to application service using CI relationship editor

Business applications can have multiple instances. Application instances are nothing but application services. Relate business applications to instances by relating business applications to application services. Business application and application service are two different configuration items which must be related through a CI relationship.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy business applications module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy business applications module. If you’re a new activation user, the legacy business applications module isn’t available.

You can leverage the same features by using the Enterprise Architecture Workspace. To learn more, see [Add or edit a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/eaw-create-business-app.md).

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **All Business Applications** &gt; **Business Applications**.

2.  To relate the business application with an application service, click open a business application.

3.  Click the Add CI relationship \(\[Omitted image "RelationshipEditorIcon.png"\] Alt text: CI relationship editor icon\) icon in the **Related Items** section of the business application form to launch the relationship editor and create the [CI relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateCIRelationship.md).

4.  Select one or more application services from the **Configuration Items** section.

    Integration with Service Mapping is through the CI relationship editor creating direct relationship between the configuration items.

5.  Click the \(\[Omitted image "RelationshipEditorIcon.png"\] Alt text: Create new relationships with selected configuration items\) icon in the **Relationships** section.

    By default **Consumes::Consumed by** relationship type is selected.

    You can relate two configuration items using the suggested relationship type of CMDB. It not only selects the relationship type automatically but also ensures consistency in the relationship. The suggested relationship is established between capability and application AND between application and service.

6.  Click **Save and Exit**.


## What to do next

You have created a relationship between a business application and an application service, you can now [associate the application service to a software model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/associate-business-service-to-software-model.md).

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/using-apm.md)

