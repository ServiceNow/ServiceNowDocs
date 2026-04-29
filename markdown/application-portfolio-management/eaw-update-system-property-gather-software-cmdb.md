---
title: Update the system property to gather software products from a CMDB table
description: You can optionally customize the default values of the sn\_apm\_tpm.configurationItemsWithSoftwareInstalls system property, to capture the details of Technology Portfolio Management \(TPM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update the system property to gather software products from a CMDB table

You can optionally customize the default values of the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property, to capture the details of Technology Portfolio Management \(TPM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).

## Before you begin

This feature is available from Technology Portfolio Management plugin \(sn\_apm\_tpm\) version 1.6.0.

Role required: admin

## About this task

You can include other CMDB tables that contain software products, to fetch and view TPM software products data from those tables.

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Navigate to the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property.

3.  Select **here** to update the property details.![Sysem property screen with the here hyperlink highlighted.](../../image/eaw-image/sys-prop-incl-cmdb-table.png)

4.  In the **Value** field, add the CMDB table name that contains the details of the TPM software products, in comma-delimited format.

5.  Select **Update**.

    After the **Populate TPM Discovered Technologies and Lifecycles** job runs, the corresponding software records and their technology lifecycle details are populated in the list of TPM software products.


**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](../../concept/eaw-concept/eaw-work-with-tpm.md)

**Related topics**  


[Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../../concept/eaw-concept/eaw-tpm.md)

[Run a scheduled job to generate TPM lifecycle data](../run-scheduled-job-update-tpm-data.md)

[Schedule a job to generate TPM lifecycle data](../schedule-job-generate-tpm-data.md)

