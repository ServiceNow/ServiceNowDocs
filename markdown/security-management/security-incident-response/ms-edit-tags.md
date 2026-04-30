---
title: Edit security tags for the Microsoft Exchange Online integration
description: You can edit the names and colors of the security tags in your ServiceNow AI Platform instance for the Microsoft Exchange Online integration. These security tags help you quickly identify when email search either completes or fails. They also identify when requests to delete emails are initiated and when the email items are successfully deleted.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit security tags for the Microsoft Exchange Online integration

You can edit the names and colors of the security tags in your ServiceNow AI Platform® instance for the Microsoft Exchange Online integration. These security tags help you quickly identify when email search either completes or fails. They also identify when requests to delete emails are initiated and when the email items are successfully deleted.

## Before you begin

By default, the security tags are enabled in your ServiceNow AI Platform® instance if you select the **Display Tags** option during the configuration step. You can edit tag colors and names, and assign tags to security tag groups to help you organize them in your ServiceNow AI Platform® instance. For example, you can change the colors of tags so that the start tag of a capability is one color, and the completion tag is another color to match the other security tags that are enabled in your ServiceNow AI Platform® instance. These different colors can help you quickly identify when workflows start and are successfully completed. If you decide that you do not need a specific tag, without disabling tagging for the integration, you can also disable a single tag from the tag record. If disabled, this tag is no longer displayed on the related security incidents. For more information on how to set up security tag groups and tags, see Set up security tag groups and tags on the [Servicenow Product Documentation website](https://servicenow.com/docs).

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Exchange Online Settings**.

2.  Click the **Additional Settings** tab to select it.

3.  On the tab that is displayed, if the **Display Tags** option is cleared, select it to display tag names.

4.  With the tag names displayed, to the right of a tag, click the information icon.

    ![Additional settings page.](../image/ms-edit-tags-1.png)

5.  In the Security Tag dialog that is displayed, click **Open Record**.

6.  In the record that is displayed, edit the fields.

<table id="choicetable_ohy_xpv_bgb"><thead><tr><th align="left" id="d163022e160">

Option

</th><th align="left" id="d163022e163">

Description

</th></tr></thead><tbody><tr><td id="d163022e169">

**Name**

</td><td>

Unique name for the security tag.

</td></tr><tr><td id="d163022e178">

**Color**

</td><td>

Security tag color. Select a color from the choice list.

</td></tr><tr><td id="d163022e187">

**Security Tag Group**

</td><td>

Name of the security tag group. Click the information icon to view the available groups. Default is Metatag group.

</td></tr><tr><td id="d163022e196">

**Enforce restricted access**

</td><td>

Select this option to assign read and write roles needed by users to read or write to records that have this security tag. Default is cleared.

</td></tr><tr><td id="d163022e206">

**Order**

</td><td>

Specify the order the tag appears on forms or within a list. Default is 100.To set the order on the list, enter a value. For example, 100, 200, 300, 400. The tag with the lowest the number is displayed first on the list. The profile with the highest number is displayed last.

</td></tr><tr><td id="d163022e218">

**Active**

</td><td>

Turn this tag on or off. Default is selected \(active\)

</td></tr><tr><td id="d163022e227">

**Description**

</td><td>

Description for the tag.

</td></tr></tbody>
</table>7.  Click **Update** to save your changes.

    ![An updated security tag record.](../image/ms-edit-tags-2.png)

    You have now successfully edited the tag record for a security tag.


**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Recover deleted emails on the Microsoft Exchange Online service](ms-recover-deleted-emails.md)

**Next topic:**[Microsoft Exchange On-Premises integration](../../secops-integration-sir/secops-integration-ms-exchange-on-prem/reference/ms-exch-on-prem-landing-page.md)

