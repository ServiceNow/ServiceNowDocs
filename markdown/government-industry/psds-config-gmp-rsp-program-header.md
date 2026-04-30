---
title: Configure a custom program record header in the Reviewer Service Portal
description: As an admin, you can configure the custom widget that renders the Program header displayed to the merit reviewer persona in the Reviewer Service Portal.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Reviewer Service Portal, Grants Management, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure a custom program record header in the Reviewer Service Portal

As an admin, you can configure the custom widget that renders the Program header displayed to the merit reviewer persona in the Reviewer Service Portal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Select `sn_gsm.StandardTicketExtension`.

3.  Select **Create implementation** in the Related Links list.

4.  On the form, fill in the fields.

    Ensure that **handle** is marked **true** when you want the implementation to be shown \(checking if the table is equal\). Set the fields that you want to return by using the process\(\) command.

5.  Select **Update**.


