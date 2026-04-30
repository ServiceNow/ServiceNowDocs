---
title: Relate business application to application service using CI relationship editor - Legacy
description: Business applications can have multiple instances. Application instances are nothing but application services. Relate business applications to instances by relating business applications to application services. Business application and application service are two different configuration items which must be related through a CI relationship.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Relate business application to application service using CI relationship editor - Legacy

Business applications can have multiple instances. Application instances are nothing but application services. Relate business applications to instances by relating business applications to application services. Business application and application service are two different configuration items which must be related through a CI relationship.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **All Business Applications** &gt; **Business Applications**.

2.  To relate the business application with an application service, click open a business application.

3.  Click the Add CI relationship \(\) icon in the **Related Items** section of the business application form to launch the relationship editor and create the [CI relationship](https://www.servicenow.com/docs/access?context=t_CreateCIRelationship&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

4.  Select one or more application services from the **Configuration Items** section.

    Integration with Service Mapping is through the CI relationship editor creating direct relationship between the configuration items.

5.  Click the \(\) icon in the **Relationships** section.

    By default **Consumes::Consumed by** relationship type is selected.

    You can relate two configuration items using the suggested relationship type of CMDB. It not only selects the relationship type automatically but also ensures consistency in the relationship. The suggested relationship is established between capability and application AND between application and service.

6.  Click **Save and Exit**.


## What to do next

You have created a relationship between a business application and an application service, you can now [associate the application service to a software model](associate-business-service-to-software-model.md).

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

