---
title: Update the system property for CMDB software products
description: You can optionally customize the default values of the sn\_apm\_tpm.configurationItemsWithSoftwareInstalls system property, to capture the details of Technology Lifecycle Management \(TLM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/eaw-update-system-property-gather-software-cmdb.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update the system property for CMDB software products

You can optionally customize the default values of the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property, to capture the details of Technology Lifecycle Management \(TLM\) software products that aren’t stored in the default CMDB tables, Computer \(CMDB\_CI\_Computer\) and all similar instances of the table, Docker Container \(CMDB\_CI\_Docker\_Container\), and Serverless Hardwares \(CMDB\_CI\_Serverless\_Hardware\).

## Before you begin

This feature is available from Technology Lifecycle Management plugin \(sn\_apm\_tpm\) version 1.6.0.

Role required: admin

## About this task

You can include other CMDB tables that contain software products, to fetch and view TLM software products data from those tables.

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Navigate to the **sn\_apm\_tpm.configurationItemsWithSoftwareInstalls** system property.

3.  Select **here** to update the property details.\[Omitted image "sys-prop-incl-cmdb-table.png"\] Alt text: System property screen with the here hyperlink highlighted.

4.  In the **Value** field, add the CMDB table name that contains the details of the TLM software products, in comma-delimited format.

5.  Select **Update**.

    After the **Populate TPM Discovered Technologies and Lifecycles** job runs, the corresponding software records and their technology lifecycle details are populated in the list of TLM software products.


**Parent Topic:**[Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-tpm.md)

**Related topics**  


[Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-tpm.md)

[Run a scheduled job to generate TPM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/run-scheduled-job-update-tpm-data.md)

[Schedule a job to generate TPM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/schedule-job-generate-tpm-data.md)

