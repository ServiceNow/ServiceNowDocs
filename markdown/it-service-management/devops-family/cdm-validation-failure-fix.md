---
title: Fix the data that caused a validation failure
description: When a policy that executes against a deployable snapshot fails or generates an error or warning, the policy identifies the offending CDI and the reason for the failure. While working in a changeset, you can use the Validation failures panel to navigate directly to the offending CDI so you can correct the issue.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Fix the data that caused a validation failure

When a policy that executes against a deployable snapshot fails or generates an error or warning, the policy identifies the offending CDI and the reason for the failure. While working in a changeset, you can use the Validation failures panel to navigate directly to the offending CDI so you can correct the issue.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: sn\_devops\_config.admin

## About this task

The Validation failures panel appears on the application tab whenever validation fails for any deployable in the application. The panel displays only snapshots with error, warning, or execution failure status for validation. Snapshots with not validated or in progress status do not appear.

**Important:** The data changes and status settings that you update in this procedure apply only to the selected changeset. For that reason, be sure to coordinate your work with others on your team.

## Procedure

1.  While working in a changeset, select the validation failures icon \(![validation failures icon](../image/icon-validation-result-wrench.png)\) to view the list of snapshots from the application that failed validation.

    In this example, the snapshots for all three deployables in the application failed validation in some way \(error, warning, or execution failure\).

    ![Select a card in the validation failures panel to go to the problematic CDI](../image/cdm-val-results-select-snapshot.png)

2.  Navigate to the failure.

    1.  Select a snapshot to view the cards.

        Each card represents a policy validation failure. Use the filter to find a card with a particular validation result. If another user has worked on the issue, you might also filter on a resolution state \(resolved, unresolved, or ignored\).

    2.  Select a card to open the editor directly to the problematic CDI.

    ![Select a card in the validation results panel to go to the problematic CDI](../image/cdm-val-results-select-card.png)

3.  Review the data and perform the necessary updates.

4.  When you finish working on the data, update the status of the error.

    Open the more actions more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) to update the status of the error.

    -   **Unresolved**: This status is the initial status for a validation error. Leave this status if you are unable to repair the data. You might work on the issue with another user.
    -   **Resolved**: You have fixed the error. Be sure to commit the changeset and validate the data to ensure that the data is correct.
    -   **Ignored**: This status indicates that no further actions will be taken.

