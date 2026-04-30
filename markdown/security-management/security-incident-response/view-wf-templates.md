---
title: Understand Security Incident Response Orchestration workflows and workflow templates
description: The Security Incident Response base system includes a series of workflows and workflow templates designed to work with security incident records.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Understand Security Incident Response Orchestration workflows and workflow templates

The Security Incident Response base system includes a series of workflows and workflow templates designed to work with security incident records.

## Before you begin

Role required: sn\_si.basic

## About this task

You can tailor all workflows and workflow templates to better suit your needs, assuming you have the appropriate role: sn\_sec\_cmn.admin. Workflows are used throughout the Security Operations system to perform a variety of tasks.

Workflow templates, however, are triggered by selecting a value in the **Category** field in a security incident. When this occurs, the workflow template associated with the selection kicks off a workflow template that instructs the security analysts how to deal with a specific type of threat.

For example, if you select **Denial of Service** from the **Category** field in a security incident, the **Security Incident - Denial of Service - Template** is executed and the analyst is directed to determine whether the target of the DOS is business critical. If so, the next task causes the priority of the security incident to be set to **1 - Critical**, and then executes the next task. And so on.

So Security Incident Response workflows and workflow templates are essentially the same, except the templates are used for a specific set of functions within a security incident.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Workflows** &gt; **View Security Workflows**.

2.  A list of the workflows and workflow templates shipped in the base system are displayed.

    Any new workflows that you have created in the Security Operations application suite are also included in the list.

3.  Click the name of the workflow or workflow template you want to view.

    **Note:** Workflows can be triggered in several different ways. Be aware that associating a workflow with a workflow trigger does not necessarily mean the workflow is active.


-   **[Security Incident Response Orchestration workflows and activities](../../../product/security-incident-response-orchestration/concept/sec-inc-resp-orchestration-workflows.md)**  
Several workflows and activities are included with Security Incident Response Orchestration.
-   **[Security Incident Response workflow templates](../../../product/security-incident-response-orchestration/concept/sir-orch-workflow-templates.md)**  
Workflow templates are provided with Security Incident Response Orchestration to allow you to perform basic security operation-related analysis procedures. The templates can be used as is or you can customize them to create workflows to better suit your specific needs. The workflow templates are deactivated by default.

**Parent Topic:**[Security Incident Response Orchestration](../../../product/security-incident-response-orchestration/concept/c_SecIncRespOrchestration.md)

