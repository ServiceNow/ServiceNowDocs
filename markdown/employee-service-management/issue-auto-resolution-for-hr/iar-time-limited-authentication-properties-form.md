---
title: Time Limited Authentication Properties form
description: Use the Issue Auto Resolution time-limited authentication record to set the fields that are related to the link's validity, expiry, and failed redirect.
locale: en-US
release: zurich
product: Issue Auto Resolution for HR
classification: issue-auto-resolution-for-hr
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Simplifying authentication experience, Use, Issue Auto Resolution for HR, HR Service Delivery, Employee Service Management]
---

# Time Limited Authentication Properties form

Use the Issue Auto Resolution time-limited authentication record to set the fields that are related to the link's validity, expiry, and failed redirect.

<table id="table_jhj_kpr_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record.

</td></tr><tr><td>

One time use

</td><td>

Maximum number of times that a user can log in.

</td></tr><tr><td>

Active

</td><td>

Option to enable the time limited authentication property.**Note:** Select this option to activate the property.

</td></tr><tr><td>

Expiry field

</td><td>

Expiry in minutes. The minimum is 30. The maximum is 1440.**Note:** The maximum login attempts are changed to one when expiry is more than 120 min.

</td></tr><tr><td>

Maximum login attempts

</td><td>

Maximum number of times that can be used log in.

</td></tr><tr><td>

Failed redirect

</td><td>

URL to redirect your users after a failed login attempt. An example of this type of URL is a public knowledge article that describes the error and has helpful links. Another example is an internal company URL \(e.g. http://portal.companya.com/logout\). **Note:** You must change the base link with the instance base link.

</td></tr><tr><td>

External logout redirect

</td><td>

URL to redirect your users after logout, typically back to the portal that enabled the single sign-on \(SSO\) \(e.g. http://portal.companya.com/logout\).**Note:** Change the link in the example to match your instance base link.

</td></tr></tbody>
</table>