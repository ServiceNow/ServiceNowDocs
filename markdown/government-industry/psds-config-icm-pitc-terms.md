---
title: Configure terms and conditions for sign and submit in Investigative Case Management
description: Configure the terms and conditions that are displayed when investigators are asked to provide a signature before submitting a chain of custody log entry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-config-icm-pitc-terms.html
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Evidence Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure terms and conditions for sign and submit in Investigative Case Management

Configure the terms and conditions that are displayed when investigators are asked to provide a signature before submitting a chain of custody log entry.

## About this task

Create or modify point in time content, such as terms and conditions, that are displayed when investigators provide a signature before submitting a chain of custody log entry. This provides investigators an opportunity to make attestations before signing the chain of custody log form, creating a formal confirmation that the investigator has or will comply with evidence handling requirements. Terms and conditions information is stored in the table.

## Before you begin

Role required: admin

Ensure that the scope selected is the Investigative Case Management application scope.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Messages**.

2.  Select **psds.chain\_of\_custody.user\_acknowledgement** in the Key field.

3.  Add the following text to the Message field.

    `I confirm that I understand and comply with all evidence handling, security, and chain of custody requirements. I acknowledge that all information provided is accurate and complete. I attest that the property listed above is in the condition described and has been handled in accordance with federal evidence management standards.`

4.  Select **Update**.


