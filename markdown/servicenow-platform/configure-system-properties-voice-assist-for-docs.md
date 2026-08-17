---
title: Configure Document Voice Interaction
description: Enable and configure Document Voice Interaction to after installing ServiceNow Otto for Document Voice
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configure-system-properties-voice-assist-for-docs.html
release: australia
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Configure Voice Assist for Docs skill, Configure, ServiceNow Otto in Document Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Document Voice Interaction

Enable and configure Document Voice Interaction to after installing ServiceNow Otto for Document Voice

## Before you begin

ServiceNow Otto for Document Voice must be installed.

Role required: admin

## About this task

You can complete this configuration before or after configuring the skill in ServiceNow Otto.

## Procedure

1.  Change the application scope to ServiceNow Otto for Document Voice.

    1.  From the header, select \[Omitted image "globe-outline-24.svg"\] Alt text: Icon for application scope.

    2.  Select **Application scope: Global** and scroll and select S**erviceNow Otto for Document Voice**.

2.  Navigate to the sys\_api\_access\_scope table.

3.  Filter the records using the `2fe2655a37820310b1e86d7c24924b3e`.

4.  Select and open the matching record.

5.  Clear the **Apply auth scope to all versions in this API** check box.

6.  Select **Update**.

    The record is saved with the check box cleared.

    If the record does not save, verify that the application scope is set to ServiceNow Otto for Document Voice, then try again.


