---
title: Entity scoping to plan a privacy program
description: When a privacy manager plans the privacy program for an organization, the first step is to scope those business applications or processes that contain personal data. In Governance, Risk, and Compliance, these business applications or business processes are called as entities. After you identify the entities processing personal data, the processing activities are automatically created.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Entity scoping to plan a privacy program

When a privacy manager plans the privacy program for an organization, the first step is to scope those business applications or processes that contain personal data. In Governance, Risk, and Compliance, these business applications or business processes are called as entities. After you identify the entities processing personal data, the processing activities are automatically created.

A privacy manager, with the role sn\_privacy\_manager, plans various privacy programs. Some examples of the privacy programs are:

-   Identifying all the business processes and vendors that process personal data of customers.
-   Identifying business applications that process personal data of employees.

All the inventory related to business processes, applications, vendors, or business services is stored in the respective Configuration Management Database \(CMDB\) tables. The respective business owners manage this inventory.

You can identify or discover entities that process personal data by using one of the following methods.

-   Filtering the entities either by discovering the processing activities by their usage of personal information.
-   Sending initial privacy assessments.

Both these methods are explained in the following sections.

-   **Discover processing activities by their usage of personal information**

    At an inventory level, when business processes, business applications, and other inventory records are mapped with information objects of type Personal information \(PI\), the privacy manager can discover those records that process specific PI information. For details about information objects and their role in Privacy Management, see [Information objects in Privacy Management](information-object-in-privacy.md).

    The following image shows a business process with information objects associated with it. To identify such business applications or processes associated with information objects, the enhanced entity filter capability in the entity scoping functionality is used. For more information, see [Scope entities to discover processing activities with personal information](../task/scope-entities-with-pi.md).

    ![Business process with information objects associated with it.](../image/business-process-with-io.png "Business process with associated information objects")

-   **Identify potential entities and sending initial privacy assessments**

    If the information objects are not mapped to the business applications or processes, you can send initial privacy assessments to all the entities and use their responses to determine if personal data is being processed. The steps to send the assessment are as follows:

    1.  Create an Entity type. For example, `Business processes that process customer personal information` or `Business applications that store employee information`.
    2.  Identify entities using Entity Type you created.
    3.  Select the relevant entities and send privacy screening assessments to the respective entity owners.
    4.  Based on the responses, processing activities are created automatically when relevant questions are answered.
    ![Send privacy assessments to entities to determine personal data.](../image/send-privacy-asmt-entities.png "Sending privacy assessments to entities")


After the entities are scoped, then, in the applications, only those entities appear that contain personal information.

-   **[Scope entities to discover processing activities with personal information](../task/scope-entities-with-pi.md)**  
Determine which entities have and process personal information using the ServiceNow® Configuration Management Database \(CMDB\) application.

**Parent Topic:**[Using Privacy Management](using-privacy-mgmt.md)

