---
title: Creating incident, problem, change, and request records from Agent Workspace
description: As customer service agents, create incident, problem, change, and request records from open cases in Agent Workspace.As a customer service agent, create an incident record from a case or associate an existing incident to a case in Agent Workspace.As a customer service agent, create a problem record from a case or associate an existing problem to a case in Agent Workspace.As a customer service agent, create a normal change record from a case or associate an existing normal change to a case in Agent Workspace.As a customer service agent, create a standard change record from a case or associate an existing standard change to a case in Agent Workspace.As a customer service agent, create a request record from a case or associate an existing request to a case in Agent Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Creating incident, problem, change, and request records from Agent Workspace

As customer service agents, create incident, problem, change, and request records from open cases in Agent Workspace.

## Create an incident record from Agent workspace

As a customer service agent, create an incident record from a case or associate an existing incident to a case in Agent Workspace.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

### Procedure

1.  Open a customer service case.

2.  Select the More UI Actions icon \(![More UI Actions icon](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Incident**.

    The following information is copied from the case to the incident record:

    |Case fields|Incident fields|
    |-----------|---------------|
    |Short description|Short description|
    |Default impact|Impact|
    |Urgency|Urgency|
    |Contact|Caller|
    |Configuration item \(if available\)|Configuration item|

    **Note:** You can manually change the incident impact and urgency to different values on the incident record as needed.


### Result

Information about the incident is added as follows:

-   An update with the incident number is added to the case work notes.
-   The incident is added to the **Incident** field in the **Related Records** form section on the case form.
-   The case number is added to the Customer Cases related list on the Incident record.
-   If the case has an associated Problem, Change Request, or Caused by Change record, this information is also copied to the incident record.
-   The domain of the incident is mapped to the domain of the case.

## Create a problem record from Agent workspace

As a customer service agent, create a problem record from a case or associate an existing problem to a case in Agent Workspace.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

### Procedure

1.  Open a customer service case.

2.  Select the More Actions icon \(![More Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Problem**.

    The following information is copied from the case to the Problem record:

    |Case fields|Problem fields|
    |-----------|--------------|
    |Short description|Problem statement|
    |Impact|Impact|
    |Urgency|Urgency|
    |Priority|Priority|
    |Company|Company|
    |Configuration item \(if available\)|Configuration item \(if blank on case, agent can manually update on problem record\)|
    |Case sys\_id|First reported by|

    **Note:** You can manually change the problem impact and urgency to different values on the Problem record as needed.


### Result

Information about the problem is added as follows:

-   An update with the problem number is added to the case work notes.
-   The problem is added to the **Problem** field in the **Related Records** form section on the case form.
-   The case number is added to the Customer Cases related list on the Problem record.
-   The domain of the problem is mapped to the domain of the case.

## Create a normal change record from Agent workspace

As a customer service agent, create a normal change record from a case or associate an existing normal change to a case in Agent Workspace.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

### Procedure

1.  Open a customer service case.

2.  Select the More Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Normal Change**.

    The following information is copied from the case to the change record:

<table id="table_vvs_g4g_5fb"><thead><tr><th>

Case fields

</th><th>

Change fields

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Short description

</td></tr><tr><td>

Description

</td><td>

Description

</td></tr><tr><td>

Impact

</td><td>

Impact

</td></tr><tr><td>

Urgency

</td><td>

Urgency

</td></tr><tr><td>

Priority

</td><td>

Priority

</td></tr><tr><td>

Company

</td><td>

Company

</td></tr><tr><td>

Contact

</td><td>

Caller

</td></tr><tr><td>

Configuration item \(if available\)

</td><td>

Configuration item**Note:** The change manager can update the configuration item on the change record. If the configuration item is not available, the agent can also manually update this information.

</td></tr></tbody>
</table>    **Note:** You can manually change the change impact and urgency to different values on the change record as needed.

    Default values are added to the following fields on the change record:

    -   **Type**: Normal
    -   **State**: New
    -   **Category**: Other
    -   **Risk**: Moderate

### Result

Information about the change is added as follows:

-   An update with the change number is added to the case work notes.
-   The change is added to the **Change Request** field within the **Related Records** form section on the case form.
-   The case number is added to the Customer Cases related list on the Change record.
-   The **Requested by** field on the change record is updated with the case agent.
-   The domain of the change is mapped to the domain of the case.

## Create a standard change record from Agent workspace

As a customer service agent, create a standard change record from a case or associate an existing standard change to a case in Agent Workspace.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

### Procedure

1.  Open a customer service case.

2.  Select the More Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Standard Change**.

    The standard change record is created using the Standard Change template, which is defined in the Standard Change catalog. The data mapping is created from the template; no data is copied from the case to the change record.


## Create a request record from Agent workspace

As a customer service agent, create a request record from a case or associate an existing request to a case in Agent Workspace.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

### Procedure

1.  Open a customer service case.

2.  Select the More Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Request**.

    The following information is copied from the case to the request record:

    |Case fields|Request fields|
    |-----------|--------------|
    |Short description|Short description|
    |Contact|Contact|

    **Note:** You can manually change the request impact and urgency to different values on the request record as needed.


### Result

Information about the incident is added as follows:

-   An update with the request number is added to the case work notes.
-   The request is associated with the case and is added to the **Requests** related list on the Case form.
-   The case number is added to the Customer Cases related list on the request record.
-   The domain of the request is mapped to the domain of the case.

