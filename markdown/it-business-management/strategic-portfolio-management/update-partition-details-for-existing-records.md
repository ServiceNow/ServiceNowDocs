---
title: Update partition details for existing records
description: Update existing records in the project, demand, programs, portfolios, and planning item tables with partition details by running the Update existing records with partition details scheduled job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/update-partition-details-for-existing-records.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Update partition details for existing records

Update existing records in the project, demand, programs, portfolios, and planning item tables with partition details by running the **Update existing records with partition details** scheduled job.

## Before you begin

Role required: admin

**Important:** This is a one-time job and is not meant to be run on a recurring schedule. Run it after you have completed partition configuration and assigned partition roles to users or user groups.

## About this task

-   Existing records in the project, demand, and planning item tables don't have partition details stamped. Run this scheduled job to update those records with the correct partition details based on the partition criteria EWD admin has configured.
-   Running this job enables segmentation for access control and configuration mapping on the updated tables, ensuring that existing records are subject to the same partition-based visibility rules as newly created records.
-   If you add new related tables to your partition configuration, you can clone this job and modify it to stamp partition values on records in those newly added tables.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the **Update existing records with partition details** scheduled job.

3.  On the Scheduled Script Execution form, ensure that the **Run** field is set to **On Demand**.

4.  Select **Execute Now**.

    The scheduled job runs and stamps partition details on all existing records in the project, demand, and planning item tables based on the configured partition criteria. After the job completes, segmentation for access control and configuration mapping is enabled on the updated records.


