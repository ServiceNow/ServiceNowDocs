---
title: Exploring EMR Help
description: Learn more about the available features offered by EMR Help to help create a seamless experience for your clinicians to raise requests from an external EMR system.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Exploring EMR Help

Learn more about the available features offered by EMR Help to help create a seamless experience for your clinicians to raise requests from an external EMR system.

## EMR Help overview

Optimize clinician time in delivering patient care by automating and routing EMR service requests from clinicians to the right teams. If an issue-reporting capability is not available within an EMR system, clinicians might not have time to report the issue, which results in unreported issues or delayed resolutions. Having to access a separate issue-reporting process takes clinician time away from patients and interrupts routine workflows.

For example, a clinician might encounter an IT or healthcare-related issue while viewing a patient record. With EMR Help, the clinician can request service directly within the EMR system, which automatically creates a service request in a ServiceNow instance. Necessary details such as patient record are added automatically and the service agent can quickly and effectively solve the issues detected by the clinician.

The EMR Help application integrates an EMR system with your ServiceNow instance to enable clinicians to submit service requests from within the EMR system. An equivalent record is created in your ServiceNow instance for each service request. A healthcare agent can then look into and resolve such records from your ServiceNow instance.

**Note:** The healthcare case request capability can only be fulfilled for custom healthcare case types. To fulfill healthcare cases, you must first create your own custom healthcare case type. For more information on this, see [Configure healthcare case types for EMR Help](../task/configure-hcls-case-types-for-emr-help.md).

## EMR Help workflow

![Workflow of the EMR Help application.](../image/hcls-exploring-emr-help.png)

In the EMR Help workflow:

1.  An administrator configures the EMR Help application to address different types of clinician issues submitted from an EMR system.
2.  A clinician detects an issue and creates a service request from directly within the EMR system using the EMR Help portal.
3.  A hospital desk service agent receives the request and fixes the issue using a ServiceNow instance.

## EMR Help benefits

EMR Help provides the following benefits:

<table id="table_bmy_ml4_xzb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Save time by submitting requests to your ServiceNow instance directly from an EMR system.

</td><td>

[Creating requests within your EMR](creating-requests-within-your-emr.md)

</td><td>

Clinician

</td></tr><tr><td>

Enjoy improved visibility by tracking task-based records such as cases, incidents, or work orders.

</td><td>

[EMR Help data model](emr-data-model.md)

</td><td>

Service Desk Agent

</td></tr><tr><td>

Provide encryption support to secure sensitive information.

</td><td>

[Encryption options in EMR Help](emr-help-encryption-support.md)

</td><td>

Administrator

</td></tr><tr><td>

Automatically transmit instance information to hospital service desk agents.

</td><td>

[Resolving EMR Help requests](resolving-emr-help-requests.md)

</td><td>

Service Desk Agent

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using EMR Help, see:

-   [Configuring EMR Help](configuring-emr-help.md)
-   [Creating requests within your EMR](creating-requests-within-your-emr.md)
-   [Resolving EMR Help requests](resolving-emr-help-requests.md)
-   [EMR Help reference](../reference/emr-reference.md)

