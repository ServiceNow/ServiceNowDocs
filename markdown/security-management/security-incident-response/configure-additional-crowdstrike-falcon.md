---
title: Configure and trigger additional actions in CrowdStrike Falcon Insight
description: The CrowdStrike Falcon Insight integration supports running additional actions like regular expression \(regex\). The CrowdStrike Falcon Insight integration provides 40 additional actions with the base system.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure and trigger additional actions in CrowdStrike Falcon Insight

The CrowdStrike Falcon Insight integration supports running additional actions like regular expression \(regex\). The CrowdStrike Falcon Insight integration provides 40 additional actions with the base system.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Falcon Insight Integration** &gt; **CrowdStrike Additional Actions**.

2.  Select **New** to create your own additional action or select an existing action that comes with the base system.

    For example, let's create a new additional action.

3.  On the form, fill the fields.

<table id="table_uwr_ky4_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Command Name

</td><td>

Command name for the additional action. For example, reg set.

</td></tr><tr><td>

Base name

</td><td>

Base name for the additional action. This field is set by default. For example, reg.

</td></tr><tr><td>

Capability

</td><td>

Capability name for the additional action. This field is set by default. For example, Run Additional Actions on Endpoint.

</td></tr><tr><td>

Integration source

</td><td>

The source for the additional action. For example, CrowdStrike Falcon Insight Integration.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the additional is active or not.

</td></tr><tr><td>

Command Type

</td><td>

Command type for the additional action. This field is set by default. For example, RTR Custom Script.

</td></tr><tr><td>

Script

</td><td>

-   **OS Type**: Option to select the OS type for your script. Select one of the following:
    -   **Windows**
    -   **MAC OS X**
    -   **Linux**
    -   **None**
-   **Script**: Option to enter your script if you selected one of the following OS, except for None option.


</td></tr><tr><td>

Configuration

</td><td>

-   **Display Tag**: Option to display the tag for the configuration. You can select the tag for the following fields:
    -   Capability - Initiated. For example, reg set - Initiated.
    -   Capability - Completed. For example, reg set - Completed.
    -   Capability - Failed. For example, reg set - Failed.
-   **Require Approval**: Option to select an approver or group that needs to approve the configuration.


</td></tr></tbody>
</table>    ![CrowdStrike Falcon Insight Additional Actions](../image/falcon-insight-additional-action.png "CrowdStrike Falcon Insight Additional Actions")

4.  Select **Submit**.

5.  You can also choose from the following existing additional actions.

    There are 40 additional actions that come with the base system, which you can use to perform additional configurations.

    **Note:** Ensure that you open the CrowdStrike Additional Actions list and set the required additional action to **true**, else the additional action will not be available in the workspace.

    ![List of additional actions that comes with the base system](../image/falcon-insight-additional-action2.png "List of additional actions that comes with the base system")

6.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

7.  Select the security incident that you want to review with the run additional actions on Endpoint.

    1.  In the related links section, select **Run Additional Actions on Endpoint**.

    2.  Browse and select the required capability.

        For example, select **reg set** capability.

    3.  Select **Include Related CI** to run the additional actions on all the related CIs of the Endpoint.

    4.  You can define the **Subkey** for the run the additional actions on Endpoint.

        This Subkey can be a HKLM/Software/new key.

8.  To initiate the run additional actions on endpoint, click **Run Additional Action**.

9.  View the automation activities of the execution, and validate them.

10. Validate the status of the action on the Additional Actions on Endpoint related lists.


