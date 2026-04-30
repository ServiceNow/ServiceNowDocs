---
title: Configure Google reCAPTCHA for external user self-registration
description: To use the Google reCAPTCHA service, you must request an API key pair from Google and then configure the related system properties.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring a user registration configuration for external users, Self-register to ServiceNow instance, Authentication, Access Management]
---

# Configure Google reCAPTCHA for external user self-registration

To use the Google reCAPTCHA service, you must request an API key pair from Google and then configure the related system properties.

## Before you begin

-   Request an API key pair \(a site key and a secret\) from Google at [https://www.google.com/recaptcha](https://www.google.com/recaptcha).
-   Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the following properties and set the values:

<table id="table_otz_245_3mb"><thead><tr><th>

Property

</th><th>

Value

</th></tr></thead><tbody><tr><td>

glide.user.registration.google.recaptcha.secret

</td><td>

The secret authorizes communication between the application and the reCAPTCHA server.

 Type: password2

</td></tr><tr><td>

glide.user.registration.google.recaptcha.site\_key

</td><td>

The site key used to invoke the reCAPTCHA service on your registration page.

 Type: string

</td></tr><tr><td>

glide.user.registration.captcha.widget

</td><td>

The Sys\_ID of the Captcha Widget.

 Type: String

</td></tr></tbody>
</table>
