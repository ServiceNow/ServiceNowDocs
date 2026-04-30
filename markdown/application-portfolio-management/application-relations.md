---
title: Business application relationship with CIs for application information
description: Business application is a new CMDB CI class. You can create relationships between the business application and other CIs. Functionally, two applications can be integrated or connected to each other to establish a relationship between them. You can relate your business applications to other infrastructural CIs like database and webservers.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Management of business applications, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business application relationship with CIs for application information

Business application is a new CMDB CI class. You can create relationships between the business application and other CIs. Functionally, two applications can be integrated or connected to each other to establish a relationship between them. You can relate your business applications to other infrastructural CIs like database and webservers.

To get reports about a business application, there must be an association between the application and the CIs that make up the application. Hence, business applications have to be integrated with the other CIs to examine the CI and its relationship from a [CI relation formatter](https://www.servicenow.com/docs/access?context=c_CIRelationsFormatterNG&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## CMDB dependency views

Dependency view graphically displays an infrastructure view for a configuration item \(CI\) and the business application or business services that it is part of and that it supports.

In Enterprise Architecture, you can see the dependency views by clicking the show dependency views icon \(![Show dependency icon](../image/ShowDependencyIcon.png)\) in the related items of the Business Application form.

In addition to the existing Enterprise Architecture specific configuration items based on references versus relationships, a relationship is established between the Business Capability configuration item and the Business Application configuration item. A reference is also created between the **Parent** related field attribute of the Business Capability table \[cmdb\_ci\_business\_capability\] and the **Platform Host** related field attribute of the Business Application table \[cmdb\_ci\_business\_app\].

To view the mapping of the related items, navigate to **Dependency Views** &gt; **Map Related Items**. The table provides a list of configuration items that are related to each other by a referenced related field, because of which the dependency view is rendered.

**Related topics**  


[Add or edit a business application](../task/manage-business-appln.md)

[View business application roadmap](../task/view-business-application-roadmap.md)

[Monitor business applications with the application landscape dashboard](../task/application-landscape-dashboard.md)

