---
title: Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]
description: Verify that you're using v2 of the MultiSSO plugin and that it's set to true to reduce security vulnerabilities.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]

Verify that you're using v2 of the MultiSSO plugin and that it's set to true to reduce security vulnerabilities.

If the Multi SSO plugin is enabled on an instance, reduce security vulnerabilities by confirming that the v2 version is enabled. The latest version enhances security and has more features, such as Assertion encryption support, and IDP-initiated Single Logout \(SLO\). If the latest version is not enabled, the new security features cannot be used and the instance is at risk of using an plugin which is deprecated.

Follow the steps in [KB0756504](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504) to upgrade to the latest version. This process includes checking for and migrating any customization-related changes, then upgrading the version. When complete, the **glide.authenticate.multissov2\_feature.enabled** system property is automatically set **true**.

## More information

|Attribute|Description|
|---------|-----------|
|Configuration name|glide.authenticate.multissov2\_feature.enabled|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Data type|Boolean|
|Recommended value|true|
|Default value|true|
|Category|[Configuration](sc-configuration.md)|
|Security risk|If the latest version is not enabled, the new security features cannot be used and the instance is at risk of using an plugin which is deprecated|
|Dependencies and prerequisites|None|
|References|[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0756504](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504)|

**Parent Topic:**[Configuration](sc-configuration.md)

