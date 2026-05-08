---
title: Test a credential for the PowerShell step
description: Test a configured credential in the PowerShell step. Confirm the credential is working before building the rest of your step.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PowerShell step, Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Test a credential for the PowerShell step

Test a configured credential in the PowerShell step. Confirm the credential is working before building the rest of your step.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Open the action with the PowerShell step that has the credential you want to test.

    If you don't have a PowerShell step you're already working with, you can Create an action with a new [PowerShell step](../../flow-designer/reference/powershell-step-action-designer.md).

3.  In the Connection Details section, enter the connection information.

4.  Click **Test PowerShell Step**.

5.  If the step has data pills as input, provide the required input in the **Step input pills** field.

6.  Click **Run Test**.


## Result

When the test completes, you can view information about the tested credential in the Test Results section. This section shows the username and target for the credential, its validation status, and any error messages.

![Test credential results showing the Username, Target, Validated, and Error fields.](../images/PowerShell-test-cred-result.png "Sample result of credential test in the PowerShell step")

**Parent Topic:**[PowerShell step](../../flow-designer/reference/powershell-step-action-designer.md)

**Related topics**  


[Configure logging for the PowerShell step](configure-logging-powershell-step.md)

