---
title: Components created with new service categories
description: When you publish a new service category using the Service Creator application, the ServiceNow system creates components for the services in that category.
locale: en-US
release: zurich
product: Service Creator
classification: service-creator
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activate Service Creator, Service Creator, Build workflows]
---

# Components created with new service categories

When you publish a new service category using the Service Creator application, the ServiceNow system creates components for the services in that category.

These components are distinct from the components installed with the Service Creator application. The following components are added for each new service category:

|Name|Description|
|----|-----------|
|&lt;Department Name&gt; Tasks \[&lt;service category table name&gt;\]|The table that stores request task records for the service category. This table extends the Task table. The name of this table is defined by the department the service category is associated with, and the **Table name** field on the service category record. A new application menu and modules are created to allow users to access records on this table. Records on this table are numbered using a new Numbers \[sys\_numbers\] record.|

|Role|Description|
|----|-----------|
|&lt;service category table name&gt;\_user|The user role required to access request records for a service category. The Table name for the service category determines the name of the role. Users designated as the manager, editors, or service fulfillers for a service category automatically receive this role. Only users with this role can be assigned task records for the service category. ACLs are created to allow users with this role to access the relevant service task table.|

|Name|Description|
|----|-----------|
|Task commented for group|Notifies the group a service task record is assigned to when a user adds a comment.|
|Task commented for assignee|Notifies the user a service task record is assigned to when a user adds a comment.|
|Task closed for group|Notifies the group a service task record is assigned to when the record is closed.|
|Task worknoted for assignee|Notifies the user a service task record is assigned to when a user adds a work note.|
|Task assigned to group|Notifies the group a service task record is assigned to when the record is assigned to that group.|
|Task assigned to assignee|Notifies the user a service task record is assigned to when the record is assigned to that user.|
|Task worknoted for group|Notifies the group a service task record is assigned to when a user adds a work note.|
|Task closed for assignee|Notifies the user a service task record is assigned to when the record is closed.|
|Task opened for user|Notifies the user that opened a service task record when the record is created.|
|Task closed for user|Notifies the user that opened a service task record when the record is closed.|
|Task commented for user|Notifies the user that opened a service task record when a user adds a comment.|

|Name|Description|
|----|-----------|
|&lt;department name&gt; Task|The form for viewing request task records for the service category. By default, this form uses a layout that includes a formatter to display the questions for the service and the answers provided by the requesting user.|

|Name|Description|
|----|-----------|
|&lt;service category name&gt;|The default service catalog category for new services created within a service category.|

