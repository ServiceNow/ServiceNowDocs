---
title: Configure a certificate attestation review
description: Send out emails to all certificate owners confirming their ownership or confirming they're no longer certificate owners at set intervals.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-22"
reading_time_minutes: 1
breadcrumb: [Certificate Attestation for Certificate Owners, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure a certificate attestation review

Send out emails to all certificate owners confirming their ownership or confirming they're no longer certificate owners at set intervals.

## Before you begin

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

2.  Select **Certificate Ownership Attestation Policy Processor**.

3.  Configure the fields to set when and how often the job runs.

    **Note:** The default settings are to run the job every month.

4.  Select **Update** or **Execute Now**.

    **Note:** You can test your attestation settings by executing them immediately to verify emails are sent to the configured users.


## Result

Email notifications are sent out to all certificate users based on the time and time intervals you set. As each user receives their notification of certificate ownership, they can attest or reject their ownership.

