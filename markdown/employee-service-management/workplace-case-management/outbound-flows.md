---
title: Outbound flows
description: Outbound flows are Integration Hub subflows that synchronize workplace cases or tasks from ServiceNow to a third‑party Facilities Management \(FM\) provider’s Work Order system, so cases tracked in ServiceNow can be executed as work orders in the provider system and remain in sync. Outbound flows send data from ServiceNow to external Facilities Management provider systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/outbound-flows.html
release: brazil
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Setup Integrated Facilities Management Integration Framework, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Outbound flows

Outbound flows are Integration Hub subflows that synchronize workplace cases or tasks from ServiceNow to a third‑party Facilities Management \(FM\) provider’s Work Order system, so cases tracked in ServiceNow can be executed as work orders in the provider system and remain in sync. Outbound flows send data from ServiceNow to external Facilities Management provider systems.

The IFM Integration Framework uses the following Workflow Studio subflows to manage the complete lifecycle of a work order in the FM provider's system. These subflows are referenced to the Facilities Management Provider record.

-   Create work order flow
-   Update work order flow
-   Cancel work order flow

Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

\[Omitted image "workorder\_subflows.png"\] Alt text:

## Create work order flow

The Create work order subflow handles the initial outbound request to create a work order in the FM provider system when a valid Workplace Case or Task is created in ServiceNow.

<table id="table_dcq_cgt_33c"><thead><tr><th>

Subflow Contract

</th><th>

Label and Description

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

-   **Record**

The Workplace Case or Task record to create the Work Order from.


</td></tr><tr><td>

Outputs

</td><td>

-   **Status**

success or failed

-   **Response Code**

HTTP response code from the provider API

-   **Message**

Error message to be logged in Workplace Task Sync History

-   **FM Work Order Id**

The Work Order ID created in the FM provider system


</td></tr><tr><td>

Actions

</td><td>

The Create work order action calls the provider spoke to create the work order through the FM provider's API and returns the Action Status object containing the Status, Response Code, Message, and FM Work Order Id.

</td></tr><tr><td>

Error Handling

</td><td>

If the FM provider API returns an error, the Status and Response Code outputs capture the failure details. The parent flow uses these values to set the Workplace Task's integration state to Create Failed and logs the error details in the Workplace Task History table for administrator review and troubleshooting.

</td></tr></tbody>
</table>## Update work order flow

The Update Work Order subflow synchronizes outbound updates from ServiceNow to the FM provider system by updating the corresponding work order when a Workplace Case or Task changes or when an agent adds comments to a synchronized task.

<table id="table_zbw_kgt_33c"><thead><tr><th>

Subflow Contract

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

-   **Record**

The Workplace Case or Task record to update the Work Order from.

-   **Changed fields**

List of field names that are updated

-   **Comment**

Comment to be added to the Work Order


</td></tr><tr><td>

Outputs

</td><td>

-   **Status**

success or failed

-   **Response Code**

HTTP response code from the provider API

-   **Message**

Error message to be logged in Workplace Task Sync History


</td></tr><tr><td>

Actions

</td><td>

The Update work order action calls the provider spoke to push the update to the FM provider's API, using the FM Work Order Id from the task record to identify the target work order. The Assign Subflow Outputs action then maps the action response values to the subflow's output.

</td></tr></tbody>
</table>## Cancel work order flow

The Cancel work order subflow handles outbound cancellation requests, notifying the FM provider's system to cancel the corresponding work order when the Workplace Task is cancelled in ServiceNow.

<table id="table_vfk_yht_33c"><thead><tr><th>

Subflow Contract

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

-   **Record**

The Workplace Case or Task record to cancel the Work Order from.


</td></tr><tr><td>

Outputs

</td><td>

-   **Status**

success or failed

-   **Response Code**

HTTP response code from the provider API

-   **Message**

Error message to be logged in Workplace Task Sync History


</td></tr><tr><td>

Actions

</td><td>

The Cancel work order action calls the provider spoke to cancel the work order through the FM provider's API. The Assign Subflow Outputs action then maps the action response values to the subflow's output.

</td></tr></tbody>
</table>