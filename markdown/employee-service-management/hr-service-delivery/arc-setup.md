---
title: Setting up the Anonymous Report Center
description: Activate and set up the Anonymous Report Center \(ARC\) to provide your employees a way to report misconduct complaints anonymously to the agent.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Anonymous Report Center \(ARC\), Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Setting up the Anonymous Report Center

Activate and set up the Anonymous Report Center \(ARC\) to provide your employees a way to report misconduct complaints anonymously to the agent.

1.  Install and activate the Anonymous Report Center \(com.sn\_anonymous\_report\_center\) plugin: [Activate the Anonymous Report Center](../task/arc-activate.md).
2.  Navigate to **Anonymous Report Center** &gt; **Properties** to configure the following system properties:

<table id="table_uq1_xbr_z3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Secret key length

</td><td>

Length of the auto-generated secret key used to retrieve anonymously submitted reports. After a report is submitted, the system generates a secret key that allows the reporter to track case progress, view updates, and respond to follow-up questions. Without this key, the reporter cannot access their submission. The minimum key length is 14.

</td></tr><tr><td>

Enable Google reCaptcha V2 on Anonymous case creation

</td><td>

please configure on Google and set these properties: google.captcha.secret, google.captcha.site\_key \(sn\_anon\_rc.arc.captcha.google.enabled\): You can enable Google reCAPTCHA V2 for anonymous case creation. Google reCAPTCHA V2 verifies if an interaction is legitimate and the complaint was created by a person. For more information, see [Google reCAPTCHA](https://www.google.com/recaptcha/about/).**Note:** If you decide to use Google reCAPTCHA V2, you must define the following Google reCAPTCHA V2 properties:

-   google.captcha.secret
-   google.captcha.site\_key
You must also set up an enterprise Google captcha account. For more information, see Configure Google reCAPTCHA for the password reset process.

</td></tr><tr><td>

Allow anonymous user access to the anonymously created cases using secret key

</td><td>

Controls whether the system generates a secret key upon report submission, enabling reporters to return to their case to track progress, view updates, and respond to follow-up questions. If disabled, reporters will not be able to access their submitted case after initial submission.

</td></tr></tbody>
</table>3.  Give employees access to the Anonymous Report Center by adding the catalog items to the Employee Center: [Add ARC catalog items to the Employee Center](../task/add-arc-menu.md)

