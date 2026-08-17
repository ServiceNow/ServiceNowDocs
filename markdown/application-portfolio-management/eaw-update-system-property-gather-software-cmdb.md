---
title: Update the system property to gather software products from a CMDB table
description: You can optionally customize the default values of the sn\_apm\_tpm.configurationItemsWithSoftwareInstalls system property, to capture the details of Technology Lifecycle Management \(TLM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-update-system-property-gather-software-cmdb.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update the system property to gather software products from a CMDB table

You can optionally customize the default values of the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property, to capture the details of Technology Lifecycle Management \(TLM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).

## Before you begin

This feature is available from Technology Lifecycle Management plugin \(sn\_apm\_tpm\) version 1.6.0.

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

You can include other CMDB tables that contain software products, to fetch and view TLM software products data from those tables.

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Navigate to the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property.

3.  Select **here** to update the property details.\[Omitted image "sys-prop-incl-cmdb-table.png"\] Alt text: Sysem property screen with the here hyperlink highlighted.

4.  In the **Value** field, add the CMDB table name that contains the details of the TLM software products, in comma-delimited format.

5.  Select **Update**.

    After the **Populate TPM Discovered Technologies and Lifecycles** job runs, the corresponding software records and their technology lifecycle details are populated in the list of TLM software products.


**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-tpm.md)

[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/update-tpm-data.md)

[Restart the TLM Discovered Technologies and Lifecycles job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

