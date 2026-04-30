---
title: System properties for configuring Walk-up Experience for guest users
description: System properties enable you to configure the Walk-up Experience for guest users to access the Walk-up Check-in widget from the Service Portal home page and schedule appointments online.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience for Customer Service Management, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# System properties for configuring Walk-up Experience for guest users

System properties enable you to configure the Walk-up Experience for guest users to access the Walk-up Check-in widget from the Service Portal home page and schedule appointments online.

## Properties to configure Walk-up Experience application

As an admin, in your instance, enter `sys_properties.list` in the filter navigator and add the following properties. The default values are listed in the following table.

|Property|Default Value|Description|
|--------|-------------|-----------|
|sn\_guest\_walkup\_cs.guest\_user\_walkup\_enabled \(true/false\)|true|Enables or disables Walk-up Experience for guest user.|
|sn\_guest\_walkup\_cs.captcha.enabled \(true/false\)|true|Enables or disables the CAPTCHA validation from the welcome page.|
|sn\_guest\_walkup\_cs.max\_confirmation\_validity\_in\_minutes \(integer\)|15 mins|The time to confirm the appointment booking.|
|sn\_guest\_walkup\_cs.max\_otp\_validity\_in\_minutes \(integer\)|5 mins|The time that the one-time password the user receives to modify or cancel the appointment is valid.|
|sn\_guest\_walkup\_cs.max\_guest\_appointments\_per\_location|0|The number of appointments the guest user can book per location.|
|sn\_guest\_walkup\_cs.captcha.timeout|10 mins|The time after which the CAPTCHA validation on the welcome page times out.|

