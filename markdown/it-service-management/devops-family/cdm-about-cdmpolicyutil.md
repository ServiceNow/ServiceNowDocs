---
title: Adding warning and failure messages to validation results — CdmPolicyUtil
description: You use the CdmPolicyUtil script include to add warning and failure messages to validation results in the CDM Policy Validation Results table. CDM expects validation warnings and failures to contain a node path, a snapshot ID, and a reference to the impacted node.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validating and correcting configuration data, Use, DevOps Config, IT Service Management]
---

# Adding warning and failure messages to validation results — CdmPolicyUtil

You use the `CdmPolicyUtil` script include to add warning and failure messages to validation results in the CDM Policy Validation Results table. CDM expects validation warnings and failures to contain a node path, a snapshot ID, and a reference to the impacted node.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## CdmPolicyUtil

-   `CdmPolicyUtil` is a public script include.
-   Because `CdmPolicyUtil` is a global script include, you do not need to invoke it like a new CdmPolicyUtil\(\).
-   You can invoke `CdmPolicyUtil` in all scopes, but the expected invocation scope is PaCE \(specifically, during the execution of PaCE policies\).
-   The proper call is `CdmPolicyUtil.methodName(parameters)`.

**Note:** If you add warning and failure messages to validation results manually instead of using CdmPolicyUtil, the snapshot validation status will show Execution Error.

## Methods

-   **addFailure**

    Adds a failure message. The message appears on the **Validation results** tab for the snapshot.

    Parameters:

    -   **Output**: Policy decision for the subject snapshot \(**primarySnapshotId**\).
    -   **cdmNode**: Node \(**sn\_cdm\_node**\) that caused the failure.
    -   **name**: Name of the failure.
    -   **description**: Description of the failure.
-   **addWarning**

    Adds a policy warning message. The message appears on the **Validation results** tab for the snapshot.

    Parameters:

    -   **Output**: Policy decision for the subject snapshot \(**primarySnapshotId**\).
    -   **cdmNode**: Node \(**sn\_cdm\_node**\) that caused the warning.
    -   **name**: Name of the warning.
    -   **description**: Description of the warning.
-   **getLastCreatedSnapshotIds**

    Returns the latest created and published snapshot IDs for the supplied **additionalDeployables**. If no published snapshot is available for a particular deployable, adds a debug message.

    Parameter:

    **additionalDeployables** – can be passed directly as it comes to the policy.

-   **getLastPublishedSnapshotIds**

    Retrieves the latest and published snapshot IDs for the supplied **additionalDeployables**. If no published snapshot is available for a particular deployable, adds a debug message.

    Parameter:

    **additionalDeployables** - can be passed directly as it comes to the policy.


