---
title: AIOps AI Specialist's task modules
description: Task modules are the AI Specialist's built-in capabilities. Each module handles a distinct part of the alert lifecycle, and you control which modules are active and how they behave.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/task-modules.html
release: australia
topic_type: concept
last_updated: "2026-11-01"
reading_time_minutes: 1
keywords: [task modules, AI specialist, deflect, investigate, remediate]
breadcrumb: [Onboard the AIOps specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# AIOps AI Specialist's task modules

Task modules are the AI Specialist's built-in capabilities. Each module handles a distinct part of the alert lifecycle, and you control which modules are active and how they behave.

## Noise Reduction

The Noise Reduction task module reduces alert noise. When enabled, the AI Specialist closes automatically alerts that were historically resolved without action or have no meaningful service impact. This keeps your team's queue focused on alerts that actually need attention.

The AI learns from your alert history. The more it processes, the more accurate its noise reduction decisions become over time.

## Investigate

Investigate is the AI Specialist's analysis engine. For every alert assigned to it, the AI runs two analyzations:

-   **Root cause analysis**

    Searches for related alerts and recent changes that explain why the alert fired. Surfaces a probable cause with supporting evidence.

-   **Impact analysis**

    Maps what the alert affects such as service instances, service offerings, and technical business services that the alert touches, and how far the impact reaches.


## Remediate

The Remediate task module searches existing KB articles for available automation and suggests the best possible remediation actions that the user can execute.

## Test

The Test task module lets you run the AI Specialist on a real alert that matches the filter you set in the Tasks section. It runs one record at a time, before it goes live for your team. You see exactly what the AI would do before committing to activation: the probable cause, impact summary, and any remediation options.

You can run the test multiple times, selecting a single record each time. Adjust the configuration between runs until you're satisfied with the results.

## Module dependencies

|Module|Prerequisite|Human action required|
|------|------------|---------------------|
|Noise reduction|Alert history in your instance|None- closes alerts automatically|
|Investigate|Alert scope configured|Review and validate AI findings|
|Remediate|Existing KB articles with available automation|Activate remediation|
|Test|At least one alert available in scope|Review output, then activate or adjust|

**Parent Topic:**[Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md)

