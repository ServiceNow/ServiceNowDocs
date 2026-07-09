---
title: Initiate wrap-up during an active call
description: Open the wrap-up modal, select a wrap-up code, and submit summary notes during an active call so that call context is captured in real time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/initiate-agent-wrap-up-agent-workflow.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [agent-initiated wrap-up, wrap-up, call wrap-up, Interaction Controls Component, ICC, wrap-up codes, summary notes]
breadcrumb: [Call Wrap-Up, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Initiate wrap-up during an active call

Open the wrap-up modal, select a wrap-up code, and submit summary notes during an active call so that call context is captured in real time.

## Before you begin

The ICC for voice is integrated, and the CCaaS administrator has configured and enabled agent-initiated wrap-up.

Role required: agent

## About this task

The following is a high-level overview of how an agent initiates wrap-up during an active call. The agent is handling an active call in the Agent Workspace via the ICC.

## Procedure

1.  Select **Open Wrap-Up** in the active call controls.

    The CCaaS platform receives the wrap-up event and returns the available wrap-up codes. The wrap-up modal opens in the agent's Workspace.

2.  In the wrap-up modal, select the appropriate wrap-up code and enter summary notes and comments.

3.  Review the entries and submit the wrap-up.

    A confirmation appears in the workspace and the data is saved to the system of record immediately, even while the call remains active.


## Result

The call remains active and the agent continues the call normally.

**Note:** Agents can initiate wrap-up even if the current call flow does not have mandatory wrap-up configured.

