---
title: Setting up the Anonymous Report Center
description: Set up and configure the Anonymous Report Center \(ARC\) to provide your employees a way to submit complaints anonymous to the agent.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Anonymous Report Center \(ARC\), Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Setting up the Anonymous Report Center

Set up and configure the Anonymous Report Center \(ARC\) to provide your employees a way to submit complaints anonymous to the agent.

Install and activate the Anonymous Report Center \(com.sn\_anonymous\_report\_center\) plugin to use the Anonymous Report Center \(ARC\) if you have the admin role. For more information, see [Activate the Anonymous Report Center](../task/arc-activate.md).

|Role|Description|Contains roles|
|----|-----------|--------------|
|sn\_anon\_rc.admin|Grants admin rights to Anonymous Report Center application.| |

## System properties

The following system properties are available:

-   Length of the auto generated secret key used for retrieving anonymously created reports. The minimum key length is 14. \(sn\_anon\_rc.secret\_key\_length\): Determines the length \(in characters\) of the auto generated secret key used for retrieving anonymously created reports. The minimum length is 14 and the default.
-   Enable Google reCaptcha V2 on Anonymous case creation. If true, please configure on Google and set these properties: google.captcha.secret, google.captcha.site\_key \(sn\_anon\_rc.arc.captcha.google.enabled\): You can enable Google reCAPTCHA V2 for anonymous case creation. Google reCAPTCHA V2 verifies if an interaction is legitimate and the complaint was created by a person. For more information, see [Google reCAPTCHA](https://www.google.com/recaptcha/about/).

    **Note:** If you decide to use Google reCAPTCHA V2, you must define the following Google reCAPTCHA V2 properties:

    -   google.captcha.secret
    -   google.captcha.site\_key
    You must also set up an enterprise Google captcha account. For more information, see [Configure Google reCAPTCHA for the password reset process](https://www.servicenow.com/docs/access?context=t_ConfigureGoogleRecaptcha&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   Allow anonymous user access to the anonymously created cases using secret key. \(sn\_anon\_rc.allow\_anonymous\_case\_access\): Determines if anonymous users can access the anonymous cases they submitted using a secret key.

    **Note:** A report key \(optional\) can be generated that allows the person filing the complaint to track and view details about the progress of the anonymous case and respond to any follow up questions. Without the report key, the person who made the anonymous report cannot access their report. HR agents that have access to the Anonymous Report Center \(ARC\) and admin has access. For more information, see [Setting up the Anonymous Report Center](arc-setup.md).


