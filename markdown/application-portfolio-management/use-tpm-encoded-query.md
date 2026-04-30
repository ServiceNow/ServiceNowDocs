---
title: Filter software results using an encoded query in TPM
description: Filter out unwanted software products and reduce the number of results to skip unwanted software and their lifecycles to be shown in the Lifecycle Timeline view of a business application. By default, the TPM picks licensable software. Use this encoded query when you want TPM to include other software \(non-licensable\) and filter the result.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Filter software results using an encoded query in TPM

Filter out unwanted software products and reduce the number of results to skip unwanted software and their lifecycles to be shown in the **Lifecycle Timeline** view of a business application. By default, the TPM picks licensable software. Use this encoded query when you want TPM to include other software \(non-licensable\) and filter the result.

## Before you begin

Role required: admin

## About this task

The TPM can track technology lifecycles for both licensable and non-licensable software. When you import non-licensable software, you may end up importing a large number of unnecessary software. You can restrict the number of results by specifying an encoded query as the value of the **sn\_apm\_tpm.softwareDiscoveryModelProductFilterForTPM** system property. When you set a value for this system property and run the TPM scheduled job, you can see the search results that satisfy your encoded query.

## Procedure

1.  Generate an encoded query string through a filter on the **Software Installations** page.

    1.  Navigate to the **Software Installations** \[cmdb\_sam\_sw\_install\] page.

    2.  Apply a filter as per your requirement.

    3.  Select **Run**.

    4.  Right-click at the end of the filter breadcrumb and select **Copy query** from the context menu.

        For example: \[discovery\_model.norm\_product.product\_type=child\] ![Copy query](../../image/eaw-image/eaw-tpm-encod-query-copy.png)

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

The technologies and lifecycle values are updated in the TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\_list\] table.

**Parent Topic:**[Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../../concept/eaw-concept/eaw-tpm.md)

