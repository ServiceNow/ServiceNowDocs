---
title: FlowKMFEncrypter in a Flow Action
description: Resolve the "undefined is not a function" error that occurs when a Flow Action calls the FlowKMFEncrypter API, by allowing the operation in the Restricted Caller Access Privilege record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/platform-encryption/allow-flowkmfencrypter-restricted-caller-access.html
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [FlowKMFEncrypter, Restricted Caller Access Privilege, Flow Action, troubleshooting, undefined is not a function]
breadcrumb: [FlowKMFEncrypter API, Key Management Framework, Encryption]
---

# FlowKMFEncrypter in a Flow Action

Resolve the "undefined is not a function" error that occurs when a Flow Action calls the FlowKMFEncrypter API, by allowing the operation in the Restricted Caller Access Privilege record.

## Before you begin

Role required: admin and security\_admin

## About this task

When you use FlowKMFEncrypter in a Flow Action, the action might fail with the following error:

```
Error: undefined is not a function., Detail: undefined is not a function
```

This error occurs because the Restricted Caller Access Privilege record is not permitted. To resolve the error, locate or create the **Restricted Caller Access Privilege** record using Workflow Studio for the Flow Action and set its status to allowed.

## Procedure

1.  Create or locate the auto-created Restricted Caller Access Privilege record with the following values:

    |Field|Value|
    |-----|-----|
    |**Source Scope**|Global|
    |**Source Type**|Flow Action|
    |**Source**|Name of Flow Action|
    |**Target**|Script Include: **FlowKMFEncrypter**|
    |**Operation**|Execute API|

2.  Change **Status** from **Requested** to **Allowed**.

3.  Retest the action.


## Result

The Flow Action runs without the error, and the FlowKMFEncrypter operation is permitted.

## What to do next

**Note:** If the Flow Action is updated later, the Restricted Caller Access Privilege status changes to **Invalidated**. Update it back to **Allowed**.

**Parent Topic:**[FlowKMFEncrypter API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/flowkmfencrypter-api.md)

