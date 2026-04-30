---
title: Import failure and resolution codes in bulk
description: Import multiple failure and resolution codes via Excel templates in the Admin center to assist enterprise asset technicians in diagnosing asset issues and their resolutions.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage failure and resolution codes, Configure, Enterprise Asset Management, IT Asset Management]
---

# Import failure and resolution codes in bulk

Import multiple failure and resolution codes via Excel templates in the Admin center to assist enterprise asset technicians in diagnosing asset issues and their resolutions.

## Before you begin

The source for the codes that you want to import should already be available. For more details, see [Create a source for failure and resolution codes](create-source-failure-res-code.md).

Role required: sn\_eam.enterprise\_admin or inventory\_admin

## About this task

**Note:** The import records are stored in the Asset service import \[sn\_itam\_common\_asset\_service\_import\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Failure and resolution**.

2.  In the Failure and resolution list, select **Import**.

3.  Create an asset service import.

    1.  Select **New**.

    2.  Download, update, and save the code import template.

        1.  Select **Download Template**.
        2.  Fill in the template with the details of the codes.

            The template has the following fields:

            -   **Code**: A unique identifier used to identify an asset failure or the solution to it. For example, `F1001` or `R1001`. This field is required to import the template.
            -   **Description**: A brief description that explains what the code signifies. For example, `Power failure`.
            -   **Type**: Type of code. You can either specify `Failure` or `Resolution` in this field. This field is required to import the template.
            -   **Parent code**: Code of the parent.

                **Note:** The parent code is of the same type as the child code. For example, the parent of a failure code is another failure code, and the same applies to resolution codes.

            -   **Model categories**: Model categories to which the code can be applied.

                **Note:** When you select a parent on the code, the model category is inherited from the parent code. However, you can still update this field.

                If you don't specify any model category, the code applies to all model categories.

            -   **Source**: Source of the code.
        3.  Save the template.
    3.  On the Create New Asset service import form, fill in the details.

        1.  In the **Name** field, provide a name for the asset service import.
        2.  Select **Attach file** and then select the code import template that you created in step b.
4.  Select **Import**.


## Result

-   The Code import result section shows the following details:
    -   Code rows
    -   Code inserts
    -   Code ignored
    -   Code skipped
    -   Code errors
-   If the import is successful, the Status of the asset import changes from **Draft** to **Completed**.
-   If there are no issues with the template, all the codes that you imported are shown in the Codes list.

