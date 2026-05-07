---
title: Security Incident - Evaluate response task outcome workflow
description: Security Incident - Evaluate Response task outcome workflow determines the task to use, invokes a chosen workflow and evaluation script based on the outcome evaluator record provided as input to the chosen workflow.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident - Evaluate response task outcome workflow

Security Incident - Evaluate Response task outcome workflow determines the task to use, invokes a chosen workflow and evaluation script based on the outcome evaluator record provided as input to the chosen workflow.

## Before you begin

Role required: sn\_si.write

## About this task

This workflow runs at the same time as the create task activity to be evaluated. The evaluation script queries the artifacts \(such as sightings search records or running processes\) of the configured capability. It uses context information from the response task \(such as its parent security incident\) to determine the appropriate outcome. The outcome is generally yes or no, but can be workflow activity dependent. When creating an outcome evaluator record, only capabilities that have a configured workflow, with the **Is task based capability** check box selected, and a task input variable set are available to select.

## Procedure

1.  Review the workflow process activities and the workflow diagram.

    The workflow includes the following process activities:

    -   Run script to determine response task
    -   Should Run Workflow
    -   Parallel Flow Launcher Launch Capability Workflow
    -   Create Evaluation Event
    ![Security Incident Evaluate Response Outcome workflow diagram](../image/EvaluateResponseOutcomeWorkflow.png "Evaluate response task outcome")


**Parent Topic:**[Security Incident Response Orchestration workflows and activities](../concept/sec-inc-resp-orchestration-workflows.md)

**Related topics**  


[Create Lookup Request for IoC Changes workflow](t_CreateScanRequestforIoCChanges.md)

[Security Incident Response- Get Network Statistics flow](obtain-network-statistics-workflow.md)

[Security Incident Response - Get Running Services workflow](get-running-services-workflow.md)

[Run procdump flow](../concept/invoke_procdump.md)

