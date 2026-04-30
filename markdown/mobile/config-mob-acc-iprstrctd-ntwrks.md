---
title: Configure mobile access for IP-restricted networks
description: Configure mobile access to ServiceNow instances that use adaptive authentication, which restricts access outside a defined IP address range.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile access to IP-restricted networks, Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile access for IP-restricted networks

Configure mobile access to ServiceNow instances that use adaptive authentication, which restricts access outside a defined IP address range.

## Before you begin

To configure mobile access for IP-restricted networks, adaptive authentication must be activated on your ServiceNow instance. For more information, see [Activate adaptive authentication](https://www.servicenow.com/docs/access?context=adaptive-authentication-plugin&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Role required: admin

## About this task

For more information about adaptive authentication, see [Adaptive authentication](https://www.servicenow.com/docs/access?context=adaptive-authentication&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US), which describes this policy framework that is used to enforce authentication controls.

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Make sure that the application scope is set to **Global** by selecting the globe icon \(![Globe UI icon.](../image/globe-icon.png)\) in the upper right.

    If the application scope is not set to **Global**, then select the application scope setting and select **Global** from the list.

3.  Search for and make sure that the values for the following properties are set to `true`.

    -   **glide.authenticate.auth.policy.enabled**
    -   **glide.authenticate.preauth.allow.trusted.device**
    This step verifies that an adaptive authentication policy is activated on your ServiceNow instance.

4.  Search for the [adaptive authentication mobile system property names](../reference/adapt-auth-mob-apps-sys-props.md).

    To edit the values for a property, double-click its name and fill in the fields in the System Property New record form as needed. If you can't find a property, select **New** to add it.

    Enter information on the form as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the system property. If you are adding the system property, enter the name exactly as it appears in [Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md). For example, `glide.device.token.allowed.time.limit`.|
    |Application|Application scope. Check that the application scope is set to **Global**.|
    |Description|Description of the system property. The mobile adaptive authentication system properties are described in [Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md).|
    |Choices|Choices for your system property. Leave this field empty. The field does not apply to adaptive authentication for mobile apps.|
    |Type|The data type of the system property. The data types are described in [Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md).|
    |Value|The value that is used for the system property. The value ranges and default values are described in [Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md). If you don't enter a value for this field, the default value is used.|
    |Ignore cache|Option to ignore the cache. Make sure that this check box is selected.|
    |Private|Option to make the property private. Make sure that this check box is cleared.|
    |Read roles|Read roles for your system property. Leave this field empty. This field does not apply to adaptive authentication for mobile apps.|
    |Write roles|Write roles for your system property. Leave this field empty. This field does not apply to adaptive authentication for mobile apps.|

5.  Select **Update** or **Submit**.


-   **[Adaptive authentication for mobile apps system properties](../reference/adapt-auth-mob-apps-sys-props.md)**  
Use these system properties to configure access to IP-restricted networks for ServiceNow mobile apps.

**Parent Topic:**[Mobile access to IP-restricted networks](../concept/mob-access-ip-restrictd-netwrks.md)

