---
title: Case states
description: A customer service case can be in one of several states as the agent gathers information and works toward a resolution.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-04"
reading_time_minutes: 2
breadcrumb: [Case form, Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Case states

A customer service case can be in one of several states as the agent gathers information and works toward a resolution.

<table id="table_gft_fjr_3r"><thead><tr><th>

Term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

New

</td><td>

The initial state for a new case, which is created through any one of the channels: customer portal, email, chat, telephone, or from the Customer Service application. Actions the agent can take:

-   **Assign to me**: The case is assigned to the agent and the state changes to **Open**.
-   **Accept**: If assigned by the customer service manager, the agent accepts the case and the state changes to **Open**.
-   **Update**: updates the case.
-   **Close Case**: Closes the case.
-   **Delete**: Deletes the case.

 Actions the customer can take:

-   **Update**: updates the case.
-   **Close Case**: Closes the case

</td></tr><tr><td>

Open

</td><td>

The case is assigned to an agent and the agent clicks **Accept** or an agent opens a case and clicks **Assign to me**. Both of these actions change the state from **New** to **Open**. Actions the agent can take:

-   **Update**: Updates the case.
-   **Request Info**: The agent requests additional information from the customer. The state changes to **Awaiting Info**.
-   **Propose Solution**: The agent proposes a solution for the case.

**Note:** The **Resolution Code** and **Resolution notes** must be entered in the **Resolution Information** tab.

The state changes to **Resolved**.

-   **Close Case**: Closes the case.
-   **Delete**: Deletes the case.

</td></tr><tr><td>

Awaiting Info

</td><td>

An agent clicks **Request Info**, changing the state from **Open** to **Awaiting Info**. Actions the agent can take:

-   **Open Case**: Changes the state back to **Open**.
-   **Update**: Updates the case
-   **Close Case**: Closes the case.
-   **Delete**: Deletes the case.

 Actions the customer can take:

-   **Update**: Once the customer updates the case, the state changes to **Open**.
-   **Close Case**: Closes the case.

</td></tr><tr><td>

Resolved

</td><td>

An agent provides a resolution code and enters resolution notes in the**Resolution Information** tab and clicks **Propose Solution**, changing the state from **Awaiting Info** to **Resolved**.The **Resolution code** and **Resolution notes** fields are mandatory when an agent proposes a solution for the case.

 Actions the agent can take: **Update** \(Updates the case\)

 Actions the customer can take:

-   **Accept Solution**: The customer accepts the solution proposed by the agent. The state changes to **Closed** and a survey is displayed.
-   **Reject Solution**: The customer rejects the solution proposed by the agent and the state changes to **Open**.
-   **Delete**: Deletes the case.
-   **Close Case**: Closes the case.

</td></tr><tr><td>

Closed

</td><td>

After proposing a solution, an agent waits for the customer to respond. -   If the customer clicks **Accept Solution**, the state changes from **Resolved** to **Closed**.
-   If the customer clicks **Reject Solution**, the state changes from **Resolved** to **Open**.

 An agent, agent manager, or a customer can close a case at any time, except when it is in the **Resolved** state. When it is in the **Resolved** state, only a customer can accept or reject the proposed solution.

 When an agent or agent manager closes a case, details must be included in the **Resolution notes**. This is not required when a customer closes a case.

 A case cannot be updated once it is closed.

</td></tr></tbody>
</table>**Related topics**  


[State flows](https://www.servicenow.com/docs/access?context=c_StateFlows&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

