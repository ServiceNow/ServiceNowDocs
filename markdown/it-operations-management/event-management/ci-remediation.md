---
title: CI Remediation
description: Alert and configuration item \(CI\) remediations help troubleshoot and resolve underlying problems that generate alerts. Remediation is based on Orchestration workflows that can be scripted to perform remediation tasks such as gathering system information or rebooting a server.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# CI Remediation

Alert and configuration item \(CI\) remediations help troubleshoot and resolve underlying problems that generate alerts. Remediation is based on Orchestration workflows that can be scripted to perform remediation tasks such as gathering system information or rebooting a server.

Event Management provides a framework for configuring and implementing a system-wide remediation plan to resolve, minimize, or prevent problems that generate events and alerts. Configure alert management rules to remediate alerts and CI remediation rules to remediate a set of CIs.

## Alert remediation

Use alert management rules to associate specific alerts with a remediation workflow. You can apply a workflow to alerts manually. Alternatively, you can configure the alert management rule that executes a workflow automatically for alerts that match the rule criteria. The workflow can also be scripted to request user approval before executing subsequent workflow tasks. The workflow is paused for user approval, even if it was automatically triggered.

## CI remediation

Configure remediation more comprehensively by creating CI remediation rules to manually apply remediation to specific CIs.

## Remediation tasks

When a remediation workflow is executed, a remediation task is created to capture details such as the time that the workflow started to run, the alert that triggered the remediation workflow \(if relevant\), and the CI that was remediated. View these tasks to track remediation activities in the organization.

-   **[Create or edit CI remediation](../task/t_SACreateCIRemediation.md)**  
Create a CI remediation rule that lets users manually apply an Orchestration workflow for resolving issues with specific CIs associated with alerts. Define these CIs in the CI filter conditions of the rule.
-   **[View remediation tasks](../task/t_SAViewRemediationTasks.md)**  
Event Management automatically creates a remediation task to capture every remediation that was applied to a CI or to an alert. It gives you an overall view of remediation activities in the organization.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

**Related topics**  


[Migrate an alert action rule to an alert management rule](../task/t_EMCreateAlertRule.md)

