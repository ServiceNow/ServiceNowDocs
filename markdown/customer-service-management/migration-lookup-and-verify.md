---
title: Configure Lookup and Verify
description: Lookup and Verify helps agents identify and authenticate a caller at the start of an interaction. It has only limited support in CSM Agent Workspace, so configure it in CSM Configurable Workspace so that agents verify customers consistently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-lookup-and-verify.html
release: zurich
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure Lookup and Verify

Lookup and Verify helps agents identify and authenticate a caller at the start of an interaction. It has only limited support in CSM Agent Workspace, so configure it in CSM Configurable Workspace so that agents verify customers consistently.

## Before you begin

Role required: admin

-   Confirm that the CSM Configurable Workspace Lookup and Verify plugin \(com.snc.uib.lookup\_verify\) is active. It's installed automatically with the Customer Service plugin. For more information, see [Install CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-install-csm-config-ws.md).
-   Determine whether caller verification already happens earlier in your process, for example in an IVR system, so that you don't duplicate it.
-   Decide which users the feature applies to: contacts, consumers, or both.

## About this task

Lookup and Verify gives agents a guided way to find a caller's record and confirm their identity before discussing account details, for example on a phone interaction. It records that verification took place.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**. On the **Experiences** tab, select **CSM/FSM Configurable Workspace**.

2.  Open the record page where agents handle interactions, such as the interaction or case record page.

3.  Confirm that the contextual side panel includes the Lookup and Verify screen collection.

    The screen collection is provided in the base system as part of the UX screen collection configuration.

4.  Where possible, use an automated authentication method to select the **Verify** check box instead of relying on manual verification.

    Automated authentication is the most reliable way to verify callers.

5.  Open an interaction as an agent and confirm that Lookup and Verify appears and that you can find and verify the caller.


## What to do next

For full configuration details, including building the screen collection, see [Lookup and verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/lookup-and-verify-overview.md).

