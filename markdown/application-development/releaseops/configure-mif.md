---
title: Configure multi-instance management for instances using ReleaseOps
description: Manage the multi-instance configurations to enable access across instances in your ReleaseOps ecosystem.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Configure multi-instance management for instances using ReleaseOps

Manage the multi-instance configurations to enable access across instances in your ReleaseOps ecosystem.

## Before you begin

**Note:** Starting with version 1.2.1 of ReleaseOps, you can configure multi-instance management during guided setup. For more information, see [Complete ReleaseOps guided setup](complete-guided-setup.md).

Role required: admin or sn\_mif.mif\_admin

You must have ReleaseOps installed before configuring mulit-instance management. For more information, see [Install ReleaseOps](install-releaseops.md).

All non-production \(development and test\) instances must be configured as instances managed by your production instance to participate in your ReleaseOps ecosystem. For more information, see [Cross-instance application trust configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/grant-access-v2.md).

## Procedure

1.  Within your production instance, navigate to **All** &gt; **Multi-Instance Management** &gt; **Managed Instances**.

2.  Select **Add managed instances**.

3.  In the Add managed instances dialog, select the check box for each instance that you want to add to your ReleaseOps ecosystem.

    **Note:** You can select and hold the Shift key to select more than one instance at a time.

4.  Select **Send requests** to send the request to your selected instance or instances.

    It might take up to several minutes for the managed instance requests to appear on the instances that you selected.

5.  Within your development and test instances, navigate to **All** &gt; **Multi-Instance Management** &gt; **Manager Instances**.

6.  Open the record that was created from your production instance.

7.  Select **Approve Manager Instance**.


If you receive Trust Profile errors, confirm that both Managed Instances and Manager Instances are correctly set up and approved. For more information, see [Cross-instance application trust configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/grant-access-v2.md).

