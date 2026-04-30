---
title: Create a policy with the Integration Hub subflow
description: Use the Integration Hub subflow to create a Cloud Configuration Governance policy. An Integration Hub subflow uses graphical coding mechanisms to specify the policy conditions. It offers greater flexibility in audit violation reporting than the condition builder. That is, you can use the same policy to report different types of issues.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance policies, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a policy with the Integration Hub subflow

Use the Integration Hub subflow to create a Cloud Configuration Governance policy. An Integration Hub subflow uses graphical coding mechanisms to specify the policy conditions. It offers greater flexibility in audit violation reporting than the condition builder. That is, you can use the same policy to report different types of issues.

## Before you begin

Role required: sn\_itom\_ccg.governor

## About this task

Refer to the base system **Sample flow policy** as an example for creating new policies with the Integration Hub subflow.

## Procedure

1.  Create an Integration Hub subflow for the policy.

    1.  Copy the **CCG – Flow Policy Template** subflow.

        For more information on copying the subflow, see [Copy an Integration Hub subflow template](copy-ih-subflow-template.md).

    2.  To read the configuration data, add the **CCG – Read Config Setting** action.

        For more information on the **CCG – Read Config Setting** action, see [Cloud Configuration Governance actions reference](../reference/ccg-ih-reference.md).

    3.  Repeat step [1.b](ccg-create-policy-ih-subflow.md#ccg-read-config-settings) for all the configuration keys that you want to use in the policy.

    4.  Add the flow logic.

    5.  Assign subflow outputs.

        The subflow output settings define how Cloud Configuration Governance reports the audit violations. For more information on assigning the subflow output, see [Cloud Configuration Governance actions reference](../reference/ccg-ih-reference.md).

    6.  If you have not selected the **Report Issue** option in the **Assign Subflow outputs** form, add an action under the **Assign Subflow outputs** action, and then add the **Create Record** action.

        For more information on the **Create Record** action, see [Cloud Configuration Governance actions reference](../reference/ccg-ih-reference.md).

    7.  Save the subflow.

2.  Navigate to **Cloud Configuration Governance** &gt; **Policies**.

3.  Select **New**.

4.  On the Policy form, fill in the fields.

    For a description of the form fields, see [Cloud Configuration Governance Policy form](../reference/ccg-policy-form.md).

5.  Select **Submit**.


## What to do next

Test the policy to make sure that it is working properly. For more information, see [Test the policy](test-ccg-policy.md).

