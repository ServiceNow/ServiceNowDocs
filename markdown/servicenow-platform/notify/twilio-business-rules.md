---
title: Business rules installed with Twilio Direct driver
description: Twilio installs the following business rules.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with Twilio Direct driver, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Business rules installed with Twilio Direct driver

Twilio installs the following business rules.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Account Connected Disconnected Message|\[sn\_twilio\_direct\_twilio\_config\]|Verifies if Twilio is completely configured and displays an info message.|
|Calculate test duration|\[sn\_twilio\_direct\_callback\_test\]|Sets the duration for Twilio Callback tests.|
|Machine detection timeout range check|\[sn\_twilio\_direct\_twilio\_config\]|Verifies the timeout values for detecting the answering machine if the **Detect answering machine**is enabled. The valid range of the timeout is 3-120 seconds.|
|Move credentials|\[sn\_twilio\_direct\_twilio\_config\]|Moves the account credentials to \[sn\_twilio\_direct\_basic\_auth\]|
|Populate Credentials|\[sn\_twilio\_direct\_twilio\_config\]|Populates the current SID and Auth token from the \[sn\_twilio\_direct\_basic\_auth\] table to display them.|
|Set outbound calculated fields &amp; auth|\[sn\_twilio\_direct\_twilio\_config\]|Sets the account credentials in the basic auth profile|
|Set Reset JWT Key|\[sn\_twilio\_direct\_basic\_auth\]|Copies the auth token from \[sn\_twilio\_direct\_basic\_auth\] to signing key password in \[jwt\_keystore\_aliases\].|
|Validate &amp; set inbound calculated fields|\[sn\_twilio\_direct\_twilio\_config\]|Populates the callback\_endpoint field based on the inbound rest field value. Displays an error message if the endpoint URLs are not in the correct format.|
|Validate Fast Bulk SMS option|\[sn\_twilio\_direct\_twilio\_config\]|When **Twilio Notify bulk SMS** is enabled, validates the Twilio messaging and Notify service id.|
|Validate Intelligent SMS option|\[sn\_twilio\_direct\_twilio\_config\]|When **Intelligent SMS handling** is enabled, validates the Twilio messaging service id.|

**Parent Topic:**[Components installed with Twilio Direct driver](installed-with-twilio.md)

