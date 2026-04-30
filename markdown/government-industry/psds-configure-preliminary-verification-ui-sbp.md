---
title: Configure the Preliminary Verification Checklist UI in Social Benefits Playbook
description: Configure the preliminary verification checklist to determine if an applicant is eligible to begin an application for one or more social benefits.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Eligibility Rules Engine, Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Preliminary Verification Checklist UI in Social Benefits Playbook

Configure the preliminary verification checklist to determine if an applicant is eligible to begin an application for one or more social benefits.

## About this task

Create a pre-screener so constituents can be provided with an understanding of their potential eligibility, before they begin the application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Select the **Social Benefits Preliminary Verification** table by selecting the label.

3.  Select **Create Draft**.

4.  Under Inputs, enter one or more labels for your desired verification questions, and select **String** as Type.

    By default, inputs are provided. Customers and implementors have the flexibility to add and remove inputs as needed.

5.  Add the necessary filter conditions using the condition builder.

    These conditions determine the outcome of the policy.

6.  Select **Add condition column** for the input.

7.  On the dialog pop up, verify that the Default operator is set to **is**.

8.  Select **Done**.

9.  Add a condition column for each input above by selecting the **Add** \(\) icon.

10. Use the dropdown to set what combination of answers will yield an approval or denial.

11. Select **Save**.

    more steps

12. At the modal pop-up, select **Publish**.


## Result

The questions are shown on the first page of the Government Service Portal intake page.

