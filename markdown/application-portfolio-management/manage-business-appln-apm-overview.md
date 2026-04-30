---
title: Management of business applications
description: A business application is software used by business users to perform a business function. Classify the applications to maintain an inventory and consolidate the business applications. Analyze, assess, and evaluate the applications across various dimensions and determine the action that you can take for each application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Management of business applications

A business application is software used by business users to perform a business function. Classify the applications to maintain an inventory and consolidate the business applications. Analyze, assess, and evaluate the applications across various dimensions and determine the action that you can take for each application.

**Important:**

Starting with the Xanadu release, the legacy business applications module is moved to the Enterprise Architecture Workspace. To learn more, see [Working with an application portfolio](eaw-concept/eaw-app-portfolio.md).

You can record the details of a business application manually or import the list of applications from a spreadsheet or a third-party tool. To [import data](https://www.servicenow.com/docs/access?context=c_ImportDataUsingImportSets&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US), define a data source and transform map, and run or schedule an import.

## Assessment of Business applications

In Enterprise Architecture, add any business application that you want to assess and track for costs, usage, business value, functional fitment, and risks.

## Modeling platform applications and platforms

Use the Business Application form to create a record and capture the details of a platform application just as you create a record for a business application. Use the same form to create individual records of all business applications that run on the platform. This structure gives you a hierarchy of business applications associated with the platform host. The **Architecture type** field values help you to distinguish between the platform host and platform application data.

The architecture type values help in the following business cases:

-   Assess the performance of the platform as a whole as well as assess the performance of individual applications running on it.
-   Platform may be owned by a business owner who may not be the owner of the applications running on that platform. In such a scenario, the platform owner can assess the performance of the platform independent of the application owners, who assess the applications associated with the platform.

For example, you can create a business application record for the ServiceNow® platform. Then, create individual business application records such as Enterprise Architecture, Financial Management, and Project Portfolio Management and associate these applications to the ServiceNow® platform. The distinction between the records whether it’s a business application running on a host or a platform hosting the applications lies in the **Architecture type** values of platform application and platform host.

**Related topics**  


[Add or edit a business application](../task/manage-business-appln.md)

[Business application relationship with CIs for application information](application-relations.md)

[View business application roadmap](../task/view-business-application-roadmap.md)

[Suggestions to relate technology models to an application service](software-models-suggestions-application-service.md)

[Monitor business applications with the application landscape dashboard](../task/application-landscape-dashboard.md)

