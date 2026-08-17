---
title: Filter software results using an encoded query in TLM
description: Filter out unwanted software products and reduce the number of results to skip unwanted software and their lifecycles to be shown in the Lifecycle Timeline view of a business application. By default, the TLM picks licensable software. Use this encoded query when you want TLM to include other software \(non-licensable\) and filter the result.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/use-tpm-encoded-query.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Filter software results using an encoded query in TLM

Filter out unwanted software products and reduce the number of results to skip unwanted software and their lifecycles to be shown in the **Lifecycle Timeline** view of a business application. By default, the TLM picks licensable software. Use this encoded query when you want TLM to include other software \(non-licensable\) and filter the result.

## Before you begin

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The TLM can track technology lifecycles for both licensable and non-licensable software. When you import non-licensable software, you may end up importing many unnecessary software. You can restrict the number of results by specifying an encoded query as the value of the **sn\_apm\_tpm.softwareDiscoveryModelProductFilterForTPM** system property. When you set a value for this system property and run the TLM scheduled job, you can see the search results that satisfy your encoded query.

## Procedure

1.  Generate an encoded query string through a filter on the **Software Installations** page.

    1.  Navigate to the **Software Installations** \[cmdb\_sam\_sw\_install\] page.

    2.  Apply a filter as per your requirement.

    3.  Select **Run**.

    4.  Right-click at the end of the filter breadcrumb and select **Copy query** from the context menu.

        For example: \[discovery\_model.norm\_product.product\_type=child\] \[Omitted image "eaw-tpm-encod-query-copy.png"\] Alt text: Copy query

2.  Navigate to the System Property \[sys\_properties\] table list view.

    1.  Select **All**.

    2.  In the navigation filter, enter `sys_properties.list` and press Enter.

3.  Open the record for the **sn\_apm\_tpm.softwareDiscoveryModelProductFilterForTPM** system property.

4.  Set the system property's value to an encoded query.

    For example: \[discovery\_model.norm\_product.product\_type=child\]. If the system prompts you to change the application scope so that you can edit the record, select the provided link.

5.  Select **Update**.

6.  Run the scheduled job **Populate TPM Discovered Technologies and Lifecycles**.

    1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

    2.  Find and open the  scheduled job **Populate TPM Discovered Technologies and Lifecycles**.

    3.  Select  ** Execute Now**.


## Result

The technologies and lifecycle values are updated in the TLM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\_list\] table.

**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/update-tpm-data.md)

[Restart the TLM Discovered Technologies and Lifecycles job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-restart-tpm-scheduled-job.md)

[View technology lifecycle details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tech-lifecycle.md)

[View TLM risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tech-risk.md)

[Update the system property to gather software products from a CMDB table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-system-property-gather-software-cmdb.md)

[View technology portfolio audit risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-audit-risk-details.md)

[Update verification status of TLM audit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-verif-status.md)

[View TLM logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-tpm-logs.md)

