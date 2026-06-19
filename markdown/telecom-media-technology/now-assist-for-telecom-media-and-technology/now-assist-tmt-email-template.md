---
title: Create touchpoints and meeting records using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Send the email to instance to create the touchpoint and meeting records directly from the inbound email using Now Assist for Telecommunications, Media and Technology \(TMT\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-email-template.html
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Create touchpoints and meeting records using Now Assist for Telecommunications, Media and Technology \(TMT\)

Send the email to instance to create the touchpoint and meeting records directly from the inbound email using Now Assist for Telecommunications, Media and Technology \(TMT\).

## Before you begin

Role required: Success agent

To enable the email sending, see .

To enable the email receiving, see .

## Procedure

1.  Launch the email application.

2.  Select **New Email**.

    The new Email must contain the following information:

    \[Omitted image "touchpoint-mail-example.png"\] Alt text: touchpoint and meeting records.

<table id="table_ogx_wzn_hgc"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

From

</td><td>

Email id of the sender.

</td></tr><tr><td>

To

</td><td>

Email id of the instance that is instancename@service-now.com.

 For example: devgen@service-now.com

</td></tr><tr><td>

Subject

</td><td>

The subject of the email must start with the prefix Touchpoint:

 For example: Touchpoint: Create a touchpoint for test.

</td></tr><tr><td>

Email message

</td><td>

For Touchpoints, the Email message must contain the required fields:

-   Engagement number
-   Due date
-   Subject
-   Description
 For Meetings, the Email message must contain the required fields:

-   Source
-   Start date and time
-   End date and time
-   Meeting subject


</td></tr></tbody>
</table>3.  Select **Send**.

    **Note:** The instance may take several seconds to receive the email.


## Result

-   In the instance, the Inbound Email Actions validates the email.
-   If the validation fails, you receive the email with the validation error and template description.
-   If the validation passes, a record is created in the touchpoint and you receive a success email with the link to the created record.
-   The emails are prepared and pushed to the outbound queue where they’re scheduled to be sent.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

