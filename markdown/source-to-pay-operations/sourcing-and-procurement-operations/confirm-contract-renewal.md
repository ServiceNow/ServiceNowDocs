---
title: Confirm contract renewal in Employee Center
description: As a business owner or shopper, confirm whether the expiring contract needs to be renewed.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 1
breadcrumb: [Create a pipeline project from an expiring contract, Using Sourcing Pipeline Management, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Confirm contract renewal in Employee Center

As a business owner or shopper, confirm whether the expiring contract needs to be renewed.

## Before you begin

Role required: sn\_shop.shopper

## About this task

After a pipeline project is created from an expiring contract, a sourcing task is automatically assigned to the business owner or shopper. This task prompts them to confirm whether the expiring product or service is still needed. Based on their selection, the system either cancels the project or duplicates a sourcing request.

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

2.  Select **My Tasks**.

    The form displays the **Open** and **Completed** tabs.

    The **Open** tab lists all to-dos that have not been completed.

3.  On the **Open** tab, select the contract renewal task.

    ![Contract renewal task in Employee Center.](../image/confirm-contract-renewal.png)

4.  In the Do you want to renew this contract section, select one of the following options:

    -   **Renew this contract**: The following occurs when you select this option:
        -   The pipeline project is canceled.
        -   A mandatory Close notes text box is displayed to the user.
        -   The shopper/business owner's input is stored in the **Close notes** field on the pipeline project record and in the Work notes section.
    -   **Do not renew**: The following occurs when you select this option:
        -   Task completion is recorded in the Work notes of the pipeline project.
        -   A new sourcing request is created by duplicating the original request linked to the expiring contract.
        -   Details from the previous request are displayed, with an option to update delivery information.
        -   The new request is linked to the active pipeline project and appears under the **Overview** tab and in the Sourcing related list on the pipeline project record.
5.  Select **Submit**.


**Parent Topic:**[Create a pipeline project from an expiring contract](create-pipeline-expire-contract.md)

