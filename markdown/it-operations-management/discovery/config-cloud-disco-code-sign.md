---
title: Configure Cloud Discovery for code-signed instances
description: Configure a system property to disable unsupported script tracking for Cloud Discovery operations on instances with code signing enabled.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Cloud Discovery for code-signed instances

Configure a system property to disable unsupported script tracking for Cloud Discovery operations on instances with code signing enabled.

## Before you begin

Confirm the following:

-   You're using the Australia version of the ServiceNow AI Platform.
-   You're using the following ServiceNow Store applications and versions:
    -   Discovery Admin Workspace v1.13.0.
    -   Visibility Content v6.13.10.
    -   Discovery and Service Mapping Patterns v1.30.2.
-   You have Code Signing enabled with the Circle of Trust established. For more information, see [Configuring Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Role required: security\_admin

## About this task

The **com.glide.codesigning.tracking.unsupported\_script\_tracking.enabled** property controls script tracking for code signing on Cloud Discovery. When this property is set to **true** and code signing is enabled, ECC queue records inserted through unsupported scripts aren’t notarized, which causes Cloud Discovery operations to fail. Setting this property to **false** enables Cloud Discovery on code-signed instances.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All properties**.

2.  Search for the property **com.glide.codesigning.tracking.unsupported\_script\_tracking.enabled**

3.  Set the **Value** field to **true**.

4.  Select **Update**.

    Cloud Discovery is now configured to work with code signing. You can run Cloud Discovery on your code-signed instances.


**Related topics**  


[Discovery on Code Signing instances](../concept/code-sign-disco-probes.md)

[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)

