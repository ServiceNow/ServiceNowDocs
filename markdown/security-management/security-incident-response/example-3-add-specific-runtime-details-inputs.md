---
title: Example 3: Add specific runtime details inputs to an implementation: Run Additional Actions
description: Add specific runtime details inputs to an implementation, Run Additional Actions.Add specific run time inputs for each of the selected implementation as applicable.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Examples, Unified experience framework, SIR Workspace Orchestration, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Example 3: Add specific runtime details inputs to an implementation: Run Additional Actions

Add specific runtime details inputs to an implementation, Run Additional Actions.

You can perform **Run Additional Actions** related integration capabilities action using the **Investigation** tab from the SIR Workspace.

1.  On the **Investigation** tab, navigate to the **Entry Points Lists** section displayed on the left side of the page.
2.  Select the respective entry point and run the integration capability action.

    **Note:** You can also navigate to the **Related Records** tab on the workspace to perform the integrations capabilities action.


**Parent Topic:**[Unified Experience examples](../concept/unified-expereince-example.md)

**Related topics**  


[Example 1: Select implementations: Threat Lookup](example-1-select-implementations-threat-lookup.md)

[Example 2: Common Inputs: Sighting Search](common-inputs.md#)

## Add specific inputs to an implementation

Add specific run time inputs for each of the selected implementation as applicable.

### Before you begin

Role required: sn\_si.analyst

The available implementations are listed. Select the implementation\(s\), after you select them only the supported records will be submitted against each selected implementation\(s\).

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any security incident.

3.  Go to **Investigation** tab of the workspace.

    The investigation tab with the entry points lists is displayed.

    ![Investigation tab.](../image/example1.png)

4.  Select the configuration item from the entry point list.

    For example, select **configuration Item** entry point list. The corresponding configuration items records are displayed.

    ![Select Configuration Item.](../image/config-items.png "Select Configuration Item")

5.  Select any **Configuration Item**.

6.  Navigate to the related lists drop down that is displayed on top of the page.

    For security incident configuration item \(CI\), the drop down lists contains the following list of capabilities actions. The listed CI actions collect the results and store them as enrichment data on a security incident:

    -   Get file: This capability performs the action to get files with a specific hash value or a file name.
    -   Isolate Host: This capability restricts system connections to other devices.
    -   Get Host Details: This capability retrieves the host details, details of logged-in users, and other enrichment capabilities.
    -   Run Additional Actions: This capability runs the additional actions beyond the standard actions.
    -   Get Network Statistics: This capability retrieves the network statistics for an affected resource.
    -   Get Running Process: This capability retrieves a list of running processes on a configuration item \(CI\) from a host.
    -   Get Logged on Users: This capability gathers the data of logged on users and relates it to the security incident.
7.  Select **Run Additional Actions** to perform threat intel related integration capabilities action.

    The Run Additional Implementations modal dialogue box is displayed.

8.  Select one or more implementations from the list.

    ![Run Additional Actions](../image/additional-actions.png)

9.  Click **Next**.

    You will now be moved to the next step to add the run time details.

10. Enter a comment to associate with the action.

11. Click **Submit**.

    ![Submitted records and Activity stream work notes.](../image/specific-run-time.png)

    After the selected records are submitted, a message is displayed that the Additional Action request is being executed. Also, the respective implementation action progress is displayed in the **Activity** section.

12. View the results from the EDR related list section.


