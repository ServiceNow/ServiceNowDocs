---
title: Digital interface information object form
description: A digital interface is related to a business application, and the business application will have related information objects. You can use this relationship to get the logical data of the information object.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital interface information object form

A digital interface is related to a business application, and the business application will have related information objects. You can use this relationship to get the logical data of the information object.

## Digital Interface Information Object form fields

**Note:** The Supported CRUD Operations section helps you to define how you can interact with the information objects used, consumed or exposed by an Interface.

|Field|Description|
|-----|-----------|
|Information Object|Select the information object associated with provider business application of the digital interface. For a digital interface provided by a company, you can select any available information object.|
|Digital Interface|Name of the digital interface. This field is auto-populated with the name of the interface that you’re editing. If you want to create the relationship to a different digital interface, use the Lookup icon to select a digital interface.|
|Active From|Select the date from when the information object will be active.|
|Active Until|Select the date by when the information object will be inactive.|
|Number|Unique identifier of the digital interface information object record. This field is automatically generated and can’t be edited. The number starts with the prefix DINTFIO. For example: DINTFIO01234.|
|Description|Description about the connection between the digital interface and the information object.|

|Field|Description|
|-----|-----------|
|Can create the object?|Select Yes or No.|
|Can update the object?|Select Yes or No.|
|Can retrieve the object?|Select Yes or No.|
|Can delete the object?|Select Yes or No.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Relate an information object to a digital interface](../../task/eaw-task/eaw-dig-interface-add-info-object.md)

