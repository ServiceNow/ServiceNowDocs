---
title: Configure Notify properties for SOW
description: Manage the Notify application properties to configure the meeting capabilities in SOW.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Notify in Service Operations Workspace, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure Notify properties for SOW

Manage the Notify application properties to configure the meeting capabilities in SOW.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Select **Notify**, and then select **Notify Configurations**.

3.  Select **Configure** against **Review/Configure Notify properties**.

4.  On the form, fill the fields.

<table id="table_esc_zcm_1rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Notify integration for Task table and its extensions. Entering phone number in 'glide.notify.task.phone\_number' property is equivalent to setting this to true.

</td><td>

Option to enable Notify integration for Task table and extensions.

 Select the check box.

</td></tr><tr><td>

Notify phone number used for sending SMS and starting conference calls from any record that belongs to the task table or table that extends task table. Number must be entered in E.164 compliant format.\(Deprecated\)

</td><td>

Option to provide the phone number to be used for sending SMS and making conference calls.

</td></tr><tr><td>

If the instance is accessible on public internet using some other name, which can happen if the instance is within a private network and is accessible via a reverse proxy from outside. In that case the public name needs to be provided here. e.g. https://some\_public\_domain.com

</td><td>

Option to provide the public name for your instance.

</td></tr><tr><td>

Should confirmation SMSs for opt-in/out requests be saved into notify\_message table for tracking purpose.

</td><td>

Option to opt-in or out to save the confirmation SMS message in notify\_message table.

</td></tr><tr><td>

Enable Notify integration for Incident Communications Management. Entering phone number in 'com.snc.iam.notify\_number' property is equivalent to setting this to true.

</td><td>

Option to use Notify Webex Connector for incident and major incident-related records.

 Select the check box.

</td></tr><tr><td>

The Notify number to use for sending SMS-s and starting conference calls for Incident Communications Management. Note that for making conference calls, this number needs to have a group configured with conference call workflows.

</td><td>

Option to provide the phone number to be used for sending SMS and making conference calls.

</td></tr><tr><td>

Specify a valid Notify Number with voice capability. This will enable On-Call integration with Notify which allows On-Call users to directly call people on rosters from the browser.

</td><td>

Option to provide the phone number to be used for sending SMS and making conference calls.

</td></tr><tr><td>

Specify a valid Notify Number with voice capability. This will enable a specific Major Incident Management integration with Notify which allows Workbench users to directly call people from the browser.

</td><td>

Option to provide the phone number to be used for sending SMS and making conference calls.

</td></tr><tr><td>

Maximum SMS message length

</td><td>

1600

</td></tr></tbody>
</table>5.  Select **Save**.


**Parent Topic:**[Configuring Notify in Service Operations Workspace](../concept/configure-notify-sow.md)

