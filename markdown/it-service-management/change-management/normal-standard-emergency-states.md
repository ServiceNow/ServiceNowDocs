---
title: State progression for normal, standard, and emergency changes
description: Each change request model progresses through a number of state values in a specific order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/normal-standard-emergency-states.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Change Management, IT Service Management]
---

# State progression for normal, standard, and emergency changes

Each change request model progresses through a number of state values in a specific order.

To enable state transitions, you can attach a process with defined conditions to the change model states. For more information, see [Attach a process for Change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/attach-process-change-model.md).'

## Change type progression

Each change type progresses through the same states in a different sequence:

-   Normal changes progress through all states: **New**, **Assess**, **Authorize**,**Scheduled**, **Implement**, **Review**, and **Closed**.
-   Standard changes are pre-authorized, so they bypass the **Assess** and **Authorize** states and move from New to Scheduled.
-   Emergency changes bypass the **Assess** state but still require the **Authorize** state before scheduling.

For the state values and descriptions, see [Legacy: State model and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_ChangeStateModel.md)

## State transition triggers

A change request moves between states based on defined conditions, user actions, and approval outcomes and not on elapsed time. A change manager attaches a process with the change model states using Workflow Studio or business rules. When the conditions for a state are met, the change request progresses to the next state. For example, when a required approval is granted, or a user submits the change. For more information on configuration details, see [Attach a process for Change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/attach-process-change-model.md).

<table id="table_bls_cnj_11b"><thead><tr><th>

 

</th><th>

State

</th><th>

Can be canceled?

</th><th>

Diagram

</th></tr></thead><tbody><tr><td>

1.

</td><td>

**New**

</td><td>

Yes

</td><td rowspan="7" align="center">

\[Omitted image "NormalChangeStateModel2.png"\] Alt text: Normal change state model

</td></tr><tr><td>

2.

</td><td>

**Assess**

</td><td>

Yes

</td></tr><tr><td>

3.

</td><td>

**Authorize**

</td><td>

Yes

</td></tr><tr><td>

4.

</td><td>

**Scheduled**

</td><td>

Yes

</td></tr><tr><td>

5.

</td><td>

**Implement**

</td><td>

Yes

</td></tr><tr><td>

6.

</td><td>

**Review**

</td><td>

No

</td></tr><tr><td>

7.

</td><td>

**Closed**

</td><td>

No

</td></tr></tbody>
</table><table id="table_zfv_rfl_b1b"><thead><tr><th>

 

</th><th>

State

</th><th>

Can be canceled?

</th><th>

Diagram

</th></tr></thead><tbody><tr><td>

1.

</td><td>

**New**

</td><td>

Yes

</td><td rowspan="5" align="center">

\[Omitted image "StandardChangeStateModel2.png"\] Alt text: Standard change state model

</td></tr><tr><td>

2.

</td><td>

**Scheduled**

</td><td>

Yes

</td></tr><tr><td>

3.

</td><td>

**Implement**

</td><td>

Yes

</td></tr><tr><td>

4.

</td><td>

**Review**

</td><td>

No

</td></tr><tr><td>

5.

</td><td>

**Closed**

</td><td>

No

</td></tr></tbody>
</table><table id="table_imz_sgl_b1b"><thead><tr><th>

 

</th><th>

State

</th><th>

Can be canceled?

</th><th>

Diagram

</th></tr></thead><tbody><tr><td>

1.

</td><td>

**New**

</td><td>

Yes

</td><td rowspan="6" align="center">

\[Omitted image "EmergencyChangeStateModel2.png"\] Alt text: Emergency change state model

</td></tr><tr><td>

2.

</td><td>

**Authorize**

</td><td>

Yes

</td></tr><tr><td>

3.

</td><td>

**Scheduled**

</td><td>

Yes

</td></tr><tr><td>

4.

</td><td>

**Implement**

</td><td>

Yes

</td></tr><tr><td>

5.

</td><td>

**Review**

</td><td>

No

</td></tr><tr><td>

6.

</td><td>

**Closed**

</td><td>

No

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/exploring-change-management.md)

