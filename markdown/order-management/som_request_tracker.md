---
title: Inbound Request
description: Track the status of Sales CRM workflows and enable agents to track the status of any synchronous and asynchronous flows. It also supports processing dependent records sequentially to make sure that the data stays accurate and consistent.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Sales and Service API Core, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Inbound Request

Track the status of Sales CRM workflows and enable agents to track the status of any synchronous and asynchronous flows. It also supports processing dependent records sequentially to make sure that the data stays accurate and consistent.

## Inbound request table

Add a record to the modified Inbound Request table \[sn\_tmt\_core\_inbound\_queue\].

The following fields have been added to enhance the Inbound Request table:

-   Requested flow
-   Account
-   Contact
-   Consumer
-   Response payload
-   Source record ids
-   Status
-   Run in the background
-   Initiated by
-   Domain
-   Execute after
-   Request configuration
-   Job id

<table id="table_e1m_jt1_pdc"><thead><tr><th>

Fields

</th><th>

Description

</th><th>

Field type

</th></tr></thead><tbody><tr><td>

Requested flow

</td><td>

The reference to the Lead to Cash Entity mapping, for example Sold Product to Order mapping.

</td><td>

Reference: sn\_l2c\_core\_entity\_mapping

</td></tr><tr><td>

Run in background

</td><td>

Determines whether the flow is synchronous or asynchronous.

</td><td>

True/FalseDefault value: True

</td></tr><tr><td>

Resource

</td><td>

The name of the flow that creates the record in the Inbound Request table.

</td><td>

String

</td></tr><tr><td>

Source record ids

</td><td>

System-generated id of the source records.

</td><td>

List

</td></tr><tr><td>

Source table

</td><td>

Primary Lead to Cash Entity table on which the request is triggered.

</td><td>

Table name

</td></tr><tr><td>

Record id

</td><td>

System-generated id of the target record.

</td><td>

String

</td></tr><tr><td>

Reference table

</td><td>

Name of the target entity table for the request.

</td><td>

Table name

</td></tr><tr><td>

Payload

</td><td>

Request received as input to trigger the flow.

</td><td>

String

</td></tr><tr><td>

Response payload

</td><td>

Response of the request that contains the result of the flow and captures the record-level action and transaction status.

</td><td>

JSON

</td></tr><tr><td>

State

</td><td>

Current state of the transaction.

</td><td>

String \(choice\)New, In progress, Completed, Error, Pending

</td></tr><tr><td>

Status

</td><td>

The status of completion of the flow, for example success, partial success, failure

</td><td>

String \(choice\)Success, partial success, failure

</td></tr><tr><td>

Error message

</td><td>

Error message that is returned for an exception.

</td><td>

String

</td></tr><tr><td>

Account

</td><td>

The account associated with the source or target record.

</td><td>

Reference: customer\_account

</td></tr><tr><td>

Contact

</td><td>

The contact associated with the source or target record.

</td><td>

Reference: customer\_contact

</td></tr><tr><td>

Consumer

</td><td>

The consumer associated with the source or target record.

</td><td>

Reference: csm\_consumer

</td></tr><tr><td>

Initiated by

</td><td>

The user id from the current user session.

</td><td>

Reference: sys\_user

</td></tr><tr><td>

Domain

</td><td>

The current domain scope of the record, for example global

</td><td>

Domain id

</td></tr><tr><td>

Request Configuration

</td><td>

The reference to the Inbound Request Configuration table.strict\_read\_only field

</td><td>

Reference: sn\_tmt\_core\_inbound\_queue\_config

</td></tr><tr><td>

Execute After

</td><td>

Inbound request that must be processed before the current request.strict\_read\_only field

</td><td>

Reference: Inbound Request

</td></tr><tr><td>

Job id

</td><td>

Reference to Upgrade Inventory Job table.strict\_read\_only field

</td><td>

Reference: sn\_ind\_tmt\_orm\_upgrade\_inventory\_job

</td></tr></tbody>
</table>**Note:** The **requested\_flow** and **response\_payload** fields aren’t visible to agents.

Use the **Requested flow &lt;is not empty&gt;** to filter out records using the Lead to Cash core APIs. The Inbound Request table \[sn\_tmt\_core\_inbound\_queue\] provides the status and other details related to the request. For example, while creating an order through a quote record, a confirmation message with the order header number.

**Note:** The flow designer **SOM Request Processor** is deprecated. Requests are directed to the flow designer IBQ Request Processor.

## Security roles

<table id="table_uwv_tp4_ddc"><thead><tr><th>

Role

</th><th>

Permission

</th></tr></thead><tbody><tr><td>

Inbound Queue admin \[sn\_tmt\_core.inbound\_queue\_admin\]

</td><td>

Create, read, delete, and update

</td></tr><tr><td>

Inbound Queues Create User \[sn\_tmt\_core.inbound\_queue\_create\_user\]

</td><td>

Create**Note:** For Sales CRM requests, the user doesn't have access to the **response\_payload**, **payload**, or **requested\_flow** fields.

</td></tr><tr><td>

Inbound Queues Write User \[sn\_tmt\_core.inbound\_queue\_writer\]

</td><td>

Write access for non Sales CRM requestsRead only access for Sales CRM requests

**Note:** For Sales CRM requests, the user doesn't have access to the **response\_payload**, **payload**, or **requested\_flow** fields.

</td></tr><tr><td>

Inbound Queue Read User \[sn\_tmt\_core.inbound\_queue\_read\]

</td><td>

Read access to all Sales CRM requests

 **Note:** For Sales CRM requests, the user doesn't have access to the **response\_payload**, **payload**, or **requested\_flow** fields.

</td></tr></tbody>
</table>## Archival policies

Archive the records in the Inbound Request table and determine when to clean up records on the table after a certain number of days. You can implement a different retention period for successful and failed requests.

|Archival rule|Time period|
|-------------|-----------|
|Successful requests|10 days|
|Failed requests|30 days|

**Related topics**  


[Inbound Request Configuration](inbound-request-configuration-table.md)

