---
title: By Software Model view
description: The By Software Model view displays the Software Models Business Applications Application Services .
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multiple views in TPM, View technology risks in timeline, Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# By Software Model view

The By Software Model view displays the **Software Models** &gt; **Business Applications** &gt; **Application Services**.

By this view you can view the list of all software models along with the full version. When you click to expand the software model, you can view all the business applications that run on that software model. On further expansion of the business application, you can view all the application services that the business applications support.

There is no direct cmdb CI relationship between a business application and a software model. Whereas a business application and an application service are related by cmdb relationship. For the application service, there are related software models that are stored and retrieved from the Application Service Software Models \[sn\_apm\_tpm\_service\_software\_model\] table. Hence, the advantage of the By Software Model view is that you can directly view all the business applications that run on that software model and its full version.

By this view, you can only view the software models that have at least one or more business applications running on it.

![By Software Model view](../image/BySoftwareModelView_v2.png "By Software Model view")

You can also do the following:

-   Search the software models.
-   Set conditions to filter the software models.
-   Display a selected number of software model records using the incremental pagination option.
-   Add a demand or project to the software model. Point to the software model and click the ![add demand or project](../image/AddDemandProject.png) icon that appears next to the software model name. The demand or the project form that opens has the names of the business applications that run on the selected software model, populated in the **Business Application** field.

    **Note:** You can add a project to the software model only when you activate PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.


**Parent Topic:**[Multiple views in TPM](tpm-timeline-views.md)

