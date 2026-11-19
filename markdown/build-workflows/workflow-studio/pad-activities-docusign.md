---
title: Docusign activities
description: Enable agents and fulfillers to collect electronic signatures during a playbook run, via Workflow Data Fabric's Docusign spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/pad-activities-docusign.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Docusign activities

Enable agents and fulfillers to collect electronic signatures during a playbook run, via Workflow Data Fabric's Docusign spoke.

## Roles and availability

-   Users with the playbook.admin or pd\_author role can add these activities to a playbook.
-   You must have access to Workflow Data Fabric's Docusign spoke.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/dot-walking-examples.md).

<table id="table_esz_w4c_35b"><thead><tr><th>

 

</th><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when the activity should start running:-   **When stage starts**: The activity starts running as soon as its stage starts running.
-   **After specific activities**: The activity starts running after specified activities have finished running. You can select one more activities from the available activities. By default, the previous activity is selected.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Attachment

</td><td>

Choice

</td><td>

File or document to be signed.

</td></tr><tr><td>

Email subject

</td><td>

String

</td><td>

Subject of the email sent to signatories.

</td></tr><tr><td>

Email body

</td><td>

String

</td><td>

Message displayed to signatories.

</td></tr><tr><td>

Signatory

</td><td>

Choice

</td><td>

User record from the sys\_user table that specifies who the signature request is sent to.

</td></tr><tr><td>

DocuSign account

</td><td>

String

</td><td>

Account record from the sn\_docusign\_spoke\_accounts table that specifies where the signature request is sent from.

</td></tr></tbody>
</table>## Outputs

Your signed document, available for review.

