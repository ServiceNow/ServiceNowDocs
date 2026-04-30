---
title: Automate the AWS Security Hub finding updates and closures by the SIR incident status
description: Automate the updates and closures of findings on AWS Security Hub according to the SIR incident status. The AWS Security Hub integration has a bi-directional interface that enables findings ingestion to create security incidents and to update the findings' status according to the changes in the SIR incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate the AWS Security Hub finding updates and closures by the SIR incident status

Automate the updates and closures of findings on AWS Security Hub according to the SIR incident status. The AWS Security Hub integration has a bi-directional interface that enables findings ingestion to create security incidents and to update the findings' status according to the changes in the SIR incident.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  On the form, fill in the details.

    Follow the instructions to complete the configuration for updating AWS Security Hub findings when you create or close a security incident in SIR.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Category

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Update State

</td><td>

SIR Incident State

</td><td>

Displays a list of SIR incident states. Select an option from this list to map it to a Security Hub Finding State.

</td></tr><tr><td>

Security Hub Finding State

</td><td>

Displays a list of Security Hub workflow statuses.The workflow status of a finding is updated on AWS Security Hub when the corresponding SIR state incident state changes.

</td></tr><tr><td rowspan="2">

Update Priority

</td><td>

SIR Incident Priority

</td><td>

Displays a list of SIR incident priority levels. Select an option from this list to map it to a Security Hub finding priority level.

</td></tr><tr><td>

Security Hub Finding Priority

</td><td>

Select an option from the list of Security Hub severity levels.The severity of a finding is updated on AWS Security Hub when the corresponding security incident priority changes.

</td></tr><tr><td>

Update Work Notes

</td><td colspan="2">

Select this option to update the notes section of aSecurity Hub when a work note is updated for the correspondingSIR incident.The work notes section on SIR has a limit of 512 characters as the notes section of a Security Hub finding supports the same.

</td></tr><tr><td>

Update Additional Comments

</td><td colspan="2">

Select to update the AWS Security Hub finding comments section with the additional comments you provided in SIR incident.

</td></tr><tr><td>

Update Resolution Notes

</td><td colspan="2">

Select to update the AWS Security Hub closing comments section with the resolution notes you provided when the SIR incident is resolved.

</td></tr></tbody>
</table>    **Note:** Each update from the work notes overrides the last update in the notes section of a Security Hub finding. We recommend you to add relevant work notes in a SIR incident.

2.  Select **Finish**.


## What to do next

The profile moves to the Waiting state. When the confirmation message shows that the setup and configuration is complete, you can activate the profile.

