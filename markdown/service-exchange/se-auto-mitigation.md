---
title: Automatic mitigation for connection issues
description: Automatic mitigation detects known connection errors and fixes them without administrator action when a Service Exchange connection goes down. You review the results in issue work notes and act when a fix fails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-auto-mitigation.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 6
keywords: [automatic mitigation, known error, connection down, connection health, work notes]
breadcrumb: [Explore, Service Exchange]
---

# Automatic mitigation for connection issues

Automatic mitigation detects known connection errors and fixes them without administrator action when a Service Exchange connection goes down. You review the results in issue work notes and act when a fix fails.

A down connection stops the exchange of all data between the provider and consumer instances. Many causes of a down connection are known errors with a known fix, such as inactive capture definitions.

With automatic mitigation, the system applies the fix for these known errors as soon as the connection goes down. It confirms that the fix worked, recordres what it changed in a Health issue record, and resolves the issue. You get involved only when a fix fails or when an error isn't covered by automatic mitigation. You review the resulting issues and work notes in the [Service Exchange Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-se-center.md) on the instance where the connection went down.

Automatic mitigation is rule-based. It runs predefined validation and mitigation scripts and doesn't use AI.

## Benefits

-   Restore data exchange faster, because common connection errors are fixed without waiting for an administrator.
-   Reduce manual troubleshooting for known errors, including errors that occur after an instance clone.
-   Keep an audit trail of every automatic change in the issue work notes.

## Known errors that are fixed automatically

The system fixes a known error automatically only when the known error meets all of the following conditions:

-   The **Tier** field is set to **Automatic**.
-   The **Category** field is set to **Connection**.
-   The **Validation script** field contains a script.

Known errors with the **Tier** field set to **Supervised** or left empty aren't fixed automatically. For the list of known errors that are fixed automatically, see [Automatic mitigations for known errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation-known-errors.md).

## How automatic mitigation works

1.  The inbound or outbound status of a connection changes to Down.
2.  The system checks whether any Automatic known error is present on the connection.
3.  If the error is present, the system applies the fix once. In this release, failed fixes aren't retried.
4.  If the fix succeeds, the system checks the connection again to confirm that the error is fixed.
5.  The system creates an issue for each detected error and adds a work note with the result.
6.  When the connection status changes back to Up, the system resolves the open issue for the down connection.

**Note:** Automatic mitigation runs only when a connection goes down. It doesn't run for Slow connections.

Automatic mitigation runs on the instance where the connection goes down, on both provider and consumer instances. The fixes change records only on that instance.

## What the system handles and what you handle

Automatic mitigation handles known, repeatable fixes. You must review automatic changes, fix what automation can't, and investigate connections that keep going down.

|Situation|What the system does|What you do|
|---------|--------------------|-----------|
|Known error detected and fixed|Applies the fix, confirms it, and creates a resolved issue with a work note.|Review the work note to confirm that the change is acceptable. No other action is required.|
|Fix fails or returns an error|Creates an open issue with a work note that records the failure.|Read the work note and complete the resolution steps for the issue.|
|Security-relevant fix applied|Reactivates the integration user or turns off elevated privilege on Remote Process Sync \(RPS\) roles.|Review the change against your security policies. To prevent the fix in the future, change the **Tier** field of the known error.|
|Error isn't an Automatic known error|Takes no automatic action. The error appears as an issue from scan checks or the error log.|Follow the resolution steps for the issue.|
|Connection is Slow|Takes no automatic action.|Monitor the connection on the **Connection health** tab, and investigate if it stays Slow.|
|Connection goes down repeatedly|Applies the fix each time the connection goes down and adds a work note to each issue.|Investigate the root cause. Repeated work notes for the same fix point to an underlying problem that automation repairs each time but doesn't resolve.|
|Instance is cloned|Can fix errors, such as inactive capture definitions, when the cloned connections go down.|Check the issue work notes before you complete the reestablish connection steps, and skip the steps that are already done.|

## Mitigation work notes

The work note on each mitigation issue is the record of what the system did. Use it to confirm a fix, find the cause of a failure, and tell automatic changes from changes that people made.

To view the work note, select the issue in the Issues list and select the **Activity** tab.

Issues that automatic mitigation resolves don't appear in the Issues list, because the list shows only unresolved issues. To view these issues, open the list for the `sn_sb_health_issue` table and filter on **\[Mitigation state\] \[is\] \[Success\]** and **\[State\] \[is\] \[Resolved\]**. Then open an issue and select the **Activity** tab.

Each work note includes the following information:

-   The known error that the system detected.
-   Each fix that the system ran.
-   The result of each fix: Success, Failed, or Errored.

|Result in the work note|What it means|What to do|
|-----------------------|-------------|----------|
|Success|The fix ran and the system confirmed that the error is gone. The issue is resolved.|Review what changed. No other action is required.|
|Failed|The fix ran, but the error is still present. For example, a required capture definition is missing. The issue stays open.|Complete the resolution steps for the issue, and then select **Validate &amp; Resolve**.|
|Errored|The fix didn't complete. The issue stays open.|Complete the resolution steps for the issue. If the error recurs, contact Now Support.|

Work notes that people add show the name of the user who added them. Work notes from automatic mitigation are added by the system.

## Changes made without administrator action

Automatic fixes change records on your instance without approval. No one selects an action before these changes happen. Review the following changes against your security policies.

**Note:** Reactivates an inactive integration user for the connection.

Every change is recorded in the work notes of the related issue. For all the records that each fix changes, see [Automatic mitigations for known errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation-known-errors.md).

**Note:** The **Tier**, **Validation script**, and **Mitigation script** fields on known errors form are read-only.

## Notifications for mitigation issues

Issues that automatic mitigation resolves don't send priority 1 notifications, because no action is needed. Issues that stay open follow the existing issue notification rules.

**Related topics**  


[Health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-hd-health.md)

[Automatic mitigations for known errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation-known-errors.md)

[Known error code form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-known-error-code-form.md)

[Reestablish connection after a clone for a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-cloning-instances.md)

[Reestablish connection after a clone for a consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-cloning-instances-con.md)

[List of scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-list-of-scan-checks-in-sb.md)

