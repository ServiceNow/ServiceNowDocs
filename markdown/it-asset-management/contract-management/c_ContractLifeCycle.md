---
title: Contract life cycle
description: From creation until closure, contracts follow a life cycle that determines which fields can be edited.
locale: en-US
release: xanadu
product: Contract Management
classification: contract-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Contract Management use, Contract Management, IT Asset Management]
---

# Contract life cycle

From creation until closure, contracts follow a life cycle that determines which fields can be edited.

When a contract is in **Draft** state, almost all fields on the contract record can be edited. After a contract moves past the **Draft** state, certain date, renewal, extension, and financial fields become read-only. The **State** field and **Substate** field are read-only.

The **Contract Compliance Checks** schedule job runs on the Contract \[ast\_contract\] table automatically each night. For more information about the scheduled job, see [Use Condition Check Definitions](c_UseConditionCheckDefinitions.md). The scheduled job performs the following actions:

-   Changes the contract state to **Active** if the contract is approved and reaches the specified start date.
-   Renews the contract if the contract is approved for renewal and reaches the specified start date.
-   Changes the contract state to **Expired** if the contract state is **Active** and reaches the end date.

The system property **contract\_compliance\_check\_job.enable\_override** enables the Contract Compliance Checks job to override checks in a hierarchy. By default, this system property is set to **True**. When checks are defined on the same field of the parent and child tables, the Contract Compliance Checks job performs the following:

-   For the records on the parent table, the condition check on the table sets the field with the value specified in the condition.
-   For the records on the child table, the condition check on the child table overrides the parent table condition and sets the field value on the child table accordingly.

For example, when a check is defined on the Description field of the Contract \(parent\) and Lease \(child\) tables, the field on the Lease table is set to the value specified in the child table condition. To disable the contract compliance check override functionality, set the system property contract\_compliance\_check\_job.enable\_override to **False**.

Expense lines are only generated from contracts that are active or expired.

|State|Description|
|-----|-----------|
|Draft|User adds information about the contract and specifies an approver.|
|Active|Contract was approved and has reached the specified start date.|
|Expired|Contract reached the specified end date. Expired contracts with an active renewal workflow that are waiting for approval have a substate of **Awaiting Review**. Expired contracts with an active renewal workflow where the renewal was approved, but the renewal date hasn’t yet passed, have a substate of **Renewal Approved**. Expired contracts with no active renewal or extension pending workflow have an empty substate.|
|Canceled|Contract was discontinued and is no longer active.|

In addition to a state, a contract can also have a substate.

|Substate|Description|
|--------|-----------|
|Awaiting Review|Contract is being prepared for review.|
|Under Review|Contract sent to the approver and the approver is reviewing the contract.|
|Approved|Contract reviewed and accepted by the approver.|
|Rejected|Contract reviewed and declined by the approver.|
|Renewal Approved|Contract renewal approved by the approver.|
|Renewal Rejected|Contract renewal rejected by the approver.|
|Renewal in process|Contract renewal is in progress through the contract renewal workflow.|
|Renewed|Contract renewal is complete through the contract renewal workflow.|
|Extension Approved|Contract extension approved by the approver.|
|Extension Rejected|Contract extension rejected by the approver.|
|None|No substate is specified.|

**Parent Topic:**[Contract Management use](c_UseContractManagement.md)

**Related topics**  


[Contracts](c_Contracts.md)

