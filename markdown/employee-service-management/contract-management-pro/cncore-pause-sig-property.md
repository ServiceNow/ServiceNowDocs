---
title: Configure signature pause duration when modifying signatories
description: Configure the duration for which a signature workflow is paused when signatories are modified for an ongoing signature workflow.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure additional features in CM Pro, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure signature pause duration when modifying signatories

Configure the duration for which a signature workflow is paused when signatories are modified for an ongoing signature workflow.

## Before you begin

The Modify Signatories and Resume Signature options enables a contract fulfiller to pause an ongoing signature process to add, remove, modify, or reorder pending signatories.

If the signature process is not resumed within the configured time limit set by the system property, changes made to the signatories are automatically reverted, and the signature process resumes from its previous state.

Role required: sn\_cm\_core.contract\_admin

## About this task

**Note:** This property is applicable only for wet signature workflow and electronic signature workflow with Docusign integration.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `maximum_signature_pause_duration` property.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field with the time duration for which the signature process is paused.

    -   The minimum value that can be set is 8 hours and the maximum is 24 hours. The default duration is set to 8 hours.
    -   The value of 8 hours is considered, if the value configured is outside the allowed range.
6.  Select **Update**.


## Result

The signature pause time duration is set. For more information on the signature workflow, see [Signature workflow for a contract request](../concept/cncore-signature-workflow.md) and [Modify signatories](cncore-pause-signature.md).

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace with UI Builder components](../concept/cncore-conf-cntrct-wrkspc.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

