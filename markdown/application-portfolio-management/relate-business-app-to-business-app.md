---
title: Relate a business application to another business application
description: Relate a business application to another business application using the CI relationship \[cmdb\_rel\_ci\] table of type Interfaced by::Interfaces. Use this suggested relationship to get the information of other business applications, which are interfaced with the business application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Relate a business application to another business application

Relate a business application to another business application using the CI relationship \[cmdb\_rel\_ci\] table of type Interfaced by::Interfaces. Use this suggested relationship to get the information of other business applications, which are interfaced with the business application.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications**.

2.  To create a suggested relationship between the business applications, open a business application record.

3.  In the Related Items section of the Business Application form, click the add CI relationship icon \(![CI relationship icon](../image/RelationshipEditorIcon.png)\) to launch the relationship editor and create the CI relationship.

4.  Select the Interfaced by \(Parent\) from the Suggested relationship types section.

    The filter is automatically applied on the business application.

5.  In the Configuration Items section, select the record that is of a business application.

6.  In the Relationships section, select the CI relationship icon \(![CI relationship icon](../image/RelationshipEditorIcon.png)\) to create new relationship with selected configuration items.

    The Interfaced by::Interfaces relationship is added in the Relationships section.

7.  Click **Save and Exit**.![Relationship Editor page](../image/relate-ba-to-ba.png)


## What to do next

Click the show dependency views icon \(![Show dependency views icon.](../image/ShowDependencyIcon.png)\) in the **Business Application** related items to view the dependency of this business application interfacing or interfaced by other business applications.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

