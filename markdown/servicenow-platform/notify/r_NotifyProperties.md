---
title: Properties installed with Notify
description: Notify adds the following properties.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with Notify, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Properties installed with Notify

Notify adds the following properties.

<table id="table_adn_xgq_4y"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_twilio\_driver.max\_conference\_participants

</td><td>

Twilio maximum limit for number of participants in the conference call.

</td></tr><tr><td>

com.snc.iam.notify\_number

</td><td>

The Notify number to use for conference calls. **Note:** This number must have a group configured with conference call workflows.

</td></tr><tr><td>

glide.notify.sms.max\_characters

</td><td>

Maximum number of characters allowed to send SMS messages.

</td></tr><tr><td>

glide.enable.notify\_on\_task

</td><td>

Use this property to enable Notify integration for Task table and its extensions. Entering phone number in 'glide.notify.task.phone\_number' property is equivalent to setting this to true.

</td></tr><tr><td>

glide.notify.endpoint

</td><td>

If the instance is accessible on public internet using some other name, which can happen if the instance is within a private network and is accessible via a reverse proxy from outside. In that case the public name needs to be provided here. e.g. https://some\_public\_domain.com

</td></tr><tr><td>

glide.notify.sms.save\_confirmation\_in\_db

</td><td>

Check **Yes**if you want track the confirmation of opt-in/out requests SMS. The confirmations are saved in notify\_message table.

</td></tr><tr><td>

com.snc.iam.enable\_notify

</td><td>

Use this property to enable Notify integration for Incident Communications Management. Entering phone number in 'com.snc.iam.notify\_number' property is equivalent to setting this to true.

</td></tr><tr><td>

com.snc.iam.notify\_number

</td><td>

The Notify number to use for conference calls. Note that this number needs to have a group configured with conference call workflows.

</td></tr><tr><td>

com.snc.on\_call\_rotation.notify\_webrtc\_number

</td><td>

Specify a valid Notify number with voice capability. This will enable On-Call integration with Notify which allows On-Call users to directly call people on rosters from the browser.

</td></tr><tr><td>

sn\_major\_inc\_mgmt.notify\_webrtc\_number

</td><td>

Specify a valid Notify Number with voice capability. This will enable a specific Major Incident Management integration with Notify which allows Workbench users to directly call people from the browser.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Notify](installed-with-notify2.md)

