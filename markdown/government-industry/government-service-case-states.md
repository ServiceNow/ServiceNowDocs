---
title: Life cycle of a Public Service case
description: A public service request case within one of the three Public Sector Digital Services playbook applications can be in one of several states as it progresses through the fulfillment cycle.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Service Catalog, Reference, Public Sector Digital Services \(PSDS\)]
---

# Life cycle of a Public Service case

A public service request case within one of the three Public Sector Digital Services playbook applications can be in one of several states as it progresses through the fulfillment cycle.

## Public Service request case stages

A public service request case has four stages:

-   Intake
-   Review
-   Process
-   Decision

As a public service request case moves through the stages listed above and toward a resolution, the case status is updated. Stage and status are related to each other as described in the following table.

<table id="table_gft_fjr_3r"><thead><tr><th>

Case Stage

</th><th>

Case Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

Draft

</td><td>

The case has not yet been submitted, and the public service request case record has not yet been created.

</td></tr><tr><td>

**Intake** Guides the agent to collect the information needed to create the public service request case.

</td><td>

New

</td><td>

The initial status for a new public service case created through the Government Service Portal or one of the Public Sector Digital Services playbooks.In this state, a government service agent can do one of the following:

-   **Assign to me**: Assign themselves the case. The state changes to **Open**.
-   **Accept**: If the case was assigned to the agent by a government service manager, the can agent accept or re-assign the case. If accepted, the state changes to **Open**.
-   **Update**: Update the case.
-   **Close Case**: Close the case.
-   **Delete**: Delete the case.

 In this state, a constituent can do either of the following:

-   **Update**: Update the case with additional information.
-   **Close Case**: Close the case.

</td></tr><tr><td>

 

</td><td>

Open

</td><td>

A case changes from **New** to **Open** when a government service agent assigns the case to themselves \(**Assign to me**\), or accepts a case assigned to them by a government service manager.In this state, the agent can do one of the following:

-   **Update**: Update the case.
-   **Request Info**: Request additional information from the constituent. The case state changes to **Awaiting Info**.
-   **Propose Solution**: Propose a solution for the case. The case state changes to **Resolved**.
-   **Close Case**: Close the case.
-   **Delete**: Delete the case.

</td></tr><tr><td>

 

</td><td>

Awaiting Info

</td><td>

Additional information has been requested from the constituent. In this state, the constituent can do one of the following:-   **Update**: Add the requested information to the case. Once that information has been received, the case moves back to **Open**.
-   **Close Case**: Close the case.

</td></tr><tr><td>

**Review** Enables the agent to do initial troubleshooting on the case, check for similar or duplicate case requests, and determine what services need to be rendered.

</td><td>

Open

</td><td>

In this state, the agent can do one of the following:-   Check to see if there are similar or duplicate requests. If so, the case can be moved to progress directly.
-   **Request an Inspection**: If an inspection is requested, the case status moves to **Inspection in Progress**

</td></tr><tr><td>

 

</td><td>

Inspection in Progress

</td><td>

Inspection of the service location by a field service agent is in progress. Once complete, the case is moved to **Process**.

</td></tr><tr><td>

 

</td><td>

Awaiting Info

</td><td>

If an agent requests more information at any time during the Review stage, the status of the case changes to **Awaiting Info**. In this state, the agent can do one of the following:

-   **Open Case**: Change the case state back to **Open**.
-   **Update**: Update the case.
-   **Close Case**: Close the case.
-   **Delete**: Delete the case.

 In this state, the constituent can do one of the following:

-   **Update**: Add the requested information to the case. Once the constituent updates the case, the state changes to **Open**.
-   **Close Case**: Close the case.

</td></tr><tr><td>

**Process**

</td><td>

Work in Progress

</td><td>

The case status changes to **Work in Progress**when the agent selects **Start Work**. A work order is now in progress to solve the public service request.

</td></tr><tr><td>

 

</td><td>

Work Assignment in Progress

</td><td>

A work order is in progress, and the government service agent resolves any open case tasks associated with the case.

</td></tr><tr><td>

 

</td><td>

Awaiting Info

</td><td>

The case moves to the Awaiting Info state when an agent selects **Request Info** to request more information from the requester. The agent has requested more information during or after work has been done to resolve the case.

</td></tr><tr><td>

**Decision** Allows the requester to review the agent's decision and either accept or reject.

</td><td>

Ready for Decision

</td><td>

The case is ready for an agent decision.

</td></tr><tr><td>

 

</td><td>

Resolved

</td><td>

Once an agent provides a resolution code, enters resolution notes in the **Resolution Information** tab, and selects **Propose Solution**, the case state changes from **Awaiting Info** to **Resolved**.The **Resolution code** and **Resolution notes** fields are mandatory for an agent to propose a solution to the case.

 In this state, the agent can do one of the following:

-   **Update**: Update the case
-   **Close Case**: Close the case.

A case cannot be closed by an agent or agent manager when it is in this state. In this state, the constituent can do one of the following:

-   **Accept Solution**: Accept the solution proposed by the agent. The case state changes to **Closed** and a survey is displayed.
-   **Reject Solution**: Reject the solution proposed by the agent. The case state changes to **Open**.
-   **Delete**: Delete the case.

</td></tr><tr><td>

 

</td><td>

Closed

</td><td>

After proposing a solution, the agent waits for a constituent response. -   If the constituent clicks **Accept Solution**, the case state changes from **Resolved** to **Closed**.
-   If the constituent clicks **Reject Solution**, the state changes from **Resolved** to **Open**, and the agent must propose another solution.

 Closing a case as an agent or agent manager requires comments to be added to the **Resolution notes** field. This is not required when a customer closes a case.

 A case cannot be updated once it is closed.

</td></tr><tr><td>

 

</td><td>

Cancelled

</td><td>

The public service request is cancelled.

</td></tr></tbody>
</table>**Note:** You can't edit a public service request case when the state of the case is set to **Closed complete** or **Canceled**.

