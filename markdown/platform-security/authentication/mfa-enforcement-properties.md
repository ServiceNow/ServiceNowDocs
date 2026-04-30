---
title: MFA enforcement properties
description: Configure the properties for MFA enforcement from Yokohama and upgrade to Yokohama.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MFA enforcement, Multi-factor authentication, Authentication, Access Management]
---

# MFA enforcement properties

Configure the properties for MFA enforcement from Yokohama and upgrade to Yokohama.

To set the MFA enforcement properties, navigate to **sys\_properties.list** to validate or change the MFA enforcement properties.

<table id="table_lcc_wdq_vcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.authenticate.multifactor.setup.bypass.count**

</td><td>

Number of times a user can bypass setting up multi-factor authentication \(Max possible bypass count is 3, beyond that it will treated as 3\).

</td></tr><tr><td>

**glide.authenticate.multifactor.self\_enrolment\_period**

</td><td>

Indicates number of days a user will be given an option to self enroll for MFA, post which user will be automatically challenged with MFA. Any value exceeding 90 will be treated as 90 days only.

</td></tr><tr><td>

**glide.authenticate.multifactor.enforcement.max\_relaxation\_period**

</td><td>

Indicates the maximum number of days a new user will be given an option to self-enroll for MFA, post which all new user's performing non-SSO logins are automatically challenged with MFA. Any value exceeding 270 is treated as 270 days only.

</td></tr><tr><td>

**glide.authenticate.multifactor.enforcement.debug**

</td><td>

MFA Enforcement debug logger. Helps in debugging the flows for MFA logins. **Note:** This property doesn't exist on the instance, you have to create and enable the property, if needed.

</td></tr><tr><td>

**glide.authenticate.hybrid\_user\_tracking.enabled**

</td><td>

Property for the tracking of hybrid users. The user accounts which are not marked as 'Web service access only' in corresponding sys\_user record, but still performs integrations \(For example, API logins\) using the username and password, will be tracked in the 'User Login Info' table when this property is enabled.**Note:** This property doesn't exist on the instance, you have to create and enable the property, if needed.

</td></tr><tr><td>

**glide.authenticate.hybrid\_user\_tracking.debug**

</td><td>

A debug logger for the tracking of hybrid user API logins.Side **Note:** This property doesn't exist on the instance, you have to create and enable the property, if needed.

</td></tr></tbody>
</table>