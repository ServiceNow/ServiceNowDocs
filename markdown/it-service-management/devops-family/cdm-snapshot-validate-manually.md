---
title: Validate a snapshot manually
description: Validate a snapshot from the Snapshot tab. For example, manually validate a snapshot to ensure that its valid for new policy requirements.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Validating and correcting configuration data, Use, DevOps Config, IT Service Management]
---

# Validate a snapshot manually

Validate a snapshot from the **Snapshot** tab. For example, manually validate a snapshot to ensure that its valid for new policy requirements.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_editor or cdm\_admin

## About this task

-   Do not manually validate snapshots that have already been validated and published.
-   If you select the **Validate snapshots** or **Validate and publish snapshots** option when committing a changeset, then the system auto-validates each snapshot when it is first generated.
-   To view the current validation failures or warnings for a snapshot, open the snapshot and select the **Validation Results** tab. For details, see [View the results of snapshot validation](cdm-validation-results-view.md).
-   Use the Policy Test Playground feature to revalidate snapshots while you develop a policy. The resulting validation results are flagged as test results and do not affect operations.
-   If there is a requirement to revalidate all snapshots for a deployable, revalidate only after you have tested and published the policies.

## Procedure

1.  Use either of the following methods to validate a snapshot:

    -   Use the REST API endpoint to validate.
    -   On the **Snapshots** tab for an application, select the name of the snapshot to validate and then select **Validate**.
    -   On any tab for an open snapshot, select **Validate**.
2.  Confirm the action on the Validate snapshot dialog box.

    The system follows this procedure to validate snapshots:

    -   The system executes all policies that are statically or dynamicallymapped to the associated deployable.
    -   If the snapshot passes all policies, then the Validation status value is set to **Passed** and no entries are listed on the **Validation Results** tab. If validation was invoked with the **Publish Valid** publish option, then valid snapshots are auto-published.
    -   If any policy encounters issues, then the Validation status value is set to **Failed**. The **Validation Results** tab displays all failures or warnings returned by policies.
    -   If any policy failed to run to completion, then the Validation status value is set to **Execution error** and the **Validation Results** tab indicates that validation failed due to error.

## What to do next

If the snapshot failed validation, you can view the issues to fix them. See [View the results of snapshot validation](cdm-validation-results-view.md).

**Related topics**  


[View the results of snapshot validation](cdm-validation-results-view.md)

