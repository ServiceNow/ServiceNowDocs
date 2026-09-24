---
title: Exception questionnaire scenarios for vulnerable items
description: The questionnaire displayed when a user requests an exception on a vulnerability item depends on which questionnaires are configured in the exception management record and which request type is selected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-exception-ques-scenarios.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [exception questionnaire, deferral, risk reduction, compensating control, vulnerability item]
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Exception questionnaire scenarios for vulnerable items

The questionnaire displayed when a user requests an exception on a vulnerability item depends on which questionnaires are configured in the exception management record and which request type is selected.

## Workspace exception questionnaire behavior

In the workspace, users can request a deferral, risk reduction, or both when raising an exception on a vulnerability item. The following table shows which questionnaire is displayed for each combination of configuration and request type.

|Exception questionnaire configured|Compensating control questionnaire configured|Request type selected|Questionnaire displayed|
|----------------------------------|---------------------------------------------|---------------------|-----------------------|
|Yes|Yes|Deferral only|Exception questionnaire|
|Yes|Yes|Deferral and risk reduction|Compensating control questionnaire|
|Yes|Yes|Risk reduction only|Compensating control questionnaire|
|Yes|No|Deferral only|Exception questionnaire|
|Yes|No|Deferral and risk reduction|None — request submitted directly|
|Yes|No|Risk reduction only|None — request submitted directly|
|No|Yes|Deferral only|None — request submitted directly|
|No|Yes|Deferral and risk reduction|Compensating control questionnaire|
|No|Yes|Risk reduction only|Compensating control questionnaire|
|No|No|Any|None — request submitted directly|

**Important:**

When risk reduction is selected \(with or without deferral\), the compensating control questionnaire takes priority over the exception questionnaire. If the compensating control questionnaire is not configured, the exception request is submitted directly even when an exception questionnaire is configured.

## Classic UI behavior

In the classic UI, compensating control is not supported. All exception requests default to deferral, and only the exception questionnaire is displayed when configured. The risk reduction option and compensating control questionnaire don't apply in the classic UI.

**Parent Topic:**[Unified Security Exposure Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/unified-security-exposure-management-reference.md)

