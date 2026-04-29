---
title: Deployment process
description: Order an application from a CSD 2.0 catalog item in the service catalog triggers the Order Client Software flow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Deployment process

Order an application from a CSD 2.0 catalog item in the service catalog triggers the Order Client Software flow.

This process deploys an application to a user or device through a service catalog order:

1.  If the **Skip approval** check box is cleared in the software catalog item, the Order Client Software flow sends the catalog request to the requesting user's manager for approval.
2.  If the **Check license compliance** check box is selected in the software catalog item, the flow performs a software license check from SAM or CSD 2.0 depending on your configuration. If there is no license available, the flow creates a catalog task to procure more licenses and assigns the task to the CSD Administrators group.
3.  The Order Client Software flow triggers the Deploy Client Software flow that in turn triggers the provider-specific **Deployment Flow** that is specified in the provider record.

    ![Deployment flow specific to the Jamf provider.](../image/csd2-jamf-flows2.png)


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

