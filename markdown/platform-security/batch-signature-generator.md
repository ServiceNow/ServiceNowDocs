---
title: Generate batch signatures
description: Automatically generate batch update sets for records with invalid or missing signatures on the trusted instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [batch-signature-generator, utility, code-signing]
breadcrumb: [Utilities Dashboard, Health and Status Dashboard, Code Signing, Platform Security]
---

# Generate batch signatures

Automatically generate batch update sets for records with invalid or missing signatures on the trusted instance.

## Before you begin

You need the guardrail scan CSV report generated during CoT setup. To rerun the guardrail check, navigate to the **Signature Verification Status** tab in the Health and Status Dashboard. Select the **Rescan** button to start the scan.

Roles required:

-   security\_admin
-   codesigning\_admin
-   sn\_kmf.cryptographic\_manager

## About this task

Upload a CSV file of invalid records from guardrail checks. The utility creates optimized batches and produces signed update sets for download and import. This process streamlines your workflow and eliminates the need to create signing jobs individually.

## Procedure

1.  Select **+Add file**, select the CSV file from your device, and select the **Upload** button.

    **Note:** You can modify the CSV file to include only essential records based on organizational priorities.

    The banner displays a success message.

2.  Generate update sets by selecting the **Start scan** button.

    The progress bar indicates the status of the update set generation. If you encounter an error, verify the file contents and column names are correct. Confirm the file contains at least one eligible record.

3.  Select the **Next** button.

4.  Select the **Download all** button.

5.  View the update set generation summary by selecting **Download report**.

    The report shows:

    -   Update sets created with their names and scope information.
    -   Any unsigned records that require attention.
6.  Close or complete the session.

    -   If you have downloaded all the required update sets, select **Complete**.
    -   To return to the session at a later stage, select **Close**.

## Result

You can import the downloaded update sets on the protected instance to complete further signing steps.

