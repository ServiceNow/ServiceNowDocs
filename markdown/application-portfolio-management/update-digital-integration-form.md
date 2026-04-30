---
title: Update digital integration form
description: Use the digital integration form to update the digital integration between two business applications.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update digital integration form

Use the digital integration form to update the digital integration between two business applications.

<table id="table_hnb_rrh_bwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name of the digital integration.

</td></tr><tr><td>

Number

</td><td>

Number of the digital integration. This field is automatically generated with the DINTG prefix and can’t be edited.

</td></tr><tr><td>

Provider Digital Interface

</td><td>

Name of the digital interface. As a digital integration between two business applications or services uses a digital interface \(API\), you must select an interface related to the provider business application or service. This field is automatically generated and can’t be edited.

</td></tr><tr><td>

Provider Business Application

</td><td>

Name of the business application that provides the digital interface and enables to consume or ingest data. Changes, ownership, and responsibilities of the interface are often connected to the provider.**Note:** Being a provider or subscriber business application, it doesn’t refer to the data flow direction \(incoming, outgoing, bidirectional\). It’s managed by the Data Flow Direction attribute.

This field is automatically generated and can’t be edited.

</td></tr><tr><td>

Subscriber Digital Interface

</td><td>

Name of the r digital interface that subscribes for the integration.

</td></tr><tr><td>

Subscriber Business Application

</td><td>

Name of the business application that uses the provided interface to consume, exchange, or ingest data to support a business capability. Therefore it’s affected by the changes or an outage face connection or data loss.**Note:** Being a provider or subscriber business application, it doesn’t refer to the data flow direction \(incoming, outgoing, bidirectional\). It’s managed by the Data Flow Direction attribute.

</td></tr><tr><td>

Type

</td><td>

Type of the integration. Use the following options:

-   Data Integration – use this option when the integration must mainly focus on the exchange of data such as users, groups, locations, configuration items, and departments.
-   Process Integration – use this option when the integration is about an interaction of transactional data to support a specific process.
-   User interface Integration – use this option when the integration opens a connection with another application and sends app data via a URL to query the application.

</td></tr><tr><td>

Subtype

</td><td>

Subtype of the integration.This field appears only when **Data Integration** is selected from the **Type** field. Use the following options:

-   Process configuration
-   Foundation data
-   Configuration items
-   Events
-   Reporting
-   Sys log

</td></tr><tr><td>

Version

</td><td>

Version of the integration. You can apply a practice of designing, planning, and managing changes to an Integration. You can describe the different changes and capabilities according to version in the **Description** field. It helps Application Owners and Architects to look up which version of an Integration is in use or should change the life cycle.

</td></tr><tr><td>

Life Cycle Stage

</td><td>

Life cycle stage of the integration. Helps to track the life cycles for products, assets, contracts, CIs, locations, and other objects. Using the standard CSDM life-cycle values helps you to track objects through their transitions over time. Reporting can therefore accurately reflect the actual states of CIs: usage, availability, end of support, and so on.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Life cycle stage status of the integration. The state transition of a Digital Integration guides you through the different stages of its life cycle. A life-cycle state is the combination life-cycle stage and life-cycle status of a Digital Integration during the life cycle.

</td></tr><tr><td>

Business Unit

</td><td>

Name of the business unit that the integration belongs to.

</td></tr><tr><td>

Description

</td><td>

Description of the digital integration. Describe in detail why the integration is being created between two business applications or between an external service provided interface and a business application and what business value it adds.

</td></tr></tbody>
</table><table id="table_qkg_gny_ncc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Data flow direction

</td><td>

Direction of the data flow in the integration. Use the following options:

-   Outgoing - Data flow from the Provider business application to the Subscriber business application.
-   Incoming - Data flow from the Subscriber business application to the Provider business application.
-   Bidirectional - Data flow in both the directions between the Provider and Subscriber business applications.

</td></tr><tr><td>

Trigger

</td><td>

How to trigger the integration.Use the following options:

-   Manual
-   Scheduled
-   Process Driven
-   Event

</td></tr><tr><td>

Interval

</td><td>

Frequency to trigger the integration.Options for the interval are as follows:

-   Seconds
-   Minutes
-   Hours
-   Days
-   Weeks
-   Months
-   Quarters
-   Years
-   On Demand
-   Real Time.

</td></tr><tr><td>

Response

</td><td>

Type of the response received by the subscriber. Use the following options:

-   Synchronous
-   Asynchronous

</td></tr><tr><td>

Interaction type

</td><td>

Type of the interaction between the provider business application and the subscriber business application. Use the following options:

-   Guaranteed Message
-   Pub-Sub
-   Pull
-   Push

</td></tr><tr><td>

Middleware

</td><td>

Name of the middleware used in the integration.

</td></tr></tbody>
</table><table id="table_b52_bny_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Criticality

</td><td>

Level of the business impact criticality. Use the following options:-   Low
-   Medium
-   High
-   Critical

</td></tr><tr><td>

Confidentiality

</td><td>

Confidentiality level of the integration. Use the following options:-   Low
-   Medium
-   High
-   Critical

</td></tr><tr><td>

Integrity

</td><td>

Integrity level of the integration. Use the following options:-   Low
-   Medium
-   High
-   Critical

</td></tr><tr><td>

Availability

</td><td>

Availability of the integration. Use the following options:-   Low
-   Medium
-   High
-   Critical

</td></tr></tbody>
</table>| | |
|---|---|
|Business owner|The owner of the business function who owns the digital integration. It can be the same person who owns the parent subscriber business application.|
|IT owner|The owner within the IT organization who owns the digital integration. It can be the same person who owns the parent subscriber business application.|
|Supported by|Name of the Subject Matter Expert \(SME\) or individual who provides support to the digital interface.|
|Support group|Name of the group that provides support to the digital interface.|

|Field|Description|
|-----|-----------|
|Work notes|Comments about the integration.|

**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Update a digital integration](../task/edit-digital-integration.md)

