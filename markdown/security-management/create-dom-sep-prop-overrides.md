---
title: Create domain-separated property overrides
description: When you use domain separation, you can create overrides to existing Security Operations properties that allow you to customize the functions of the applications in each of your domains.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Create domain-separated property overrides

When you use domain separation, you can create overrides to existing Security Operations properties that allow you to customize the functions of the applications in each of your domains.

## Before you begin

Requires that [Domain Support - Domain Extensions](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US) be activated. You can also learn about the [Domain Override Viewer](https://www.servicenow.com/docs/access?context=domain-sep-override-viewer&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Domain Separated Properties**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Override existing|Select this check box to create a domain-specific value for an existing property.|
    |Application|Select the application that contains the property you want to override.|
    |Property|Select the property for the selected application for which you want to create a domain-specific override.|
    |Domain|Select the domain for which you're creating this property override.|
    |Active|Turn the override on or off.|
    |Suffix|Displays the property suffix.|
    |Name|Displays the property name.|
    |Type|Displays the property type.|
    |Value|Displays the current value set for the property.|
    |New value|Enter a new value for the property to be applied to this domain.|

4.  Select **Submit**.

    The property override is applied to the selected property in the specified domain. When the logic for this property is triggered, the system checks for domain-separated property overrides. If an override for the domain is found, the new value is used. Otherwise, the value for the default domain is used.


**Parent Topic:**[Security Operations common functionality](../concept/sec-ops-common-functionality.md)

**Related topics**  


[Understanding domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=australia&pubname=australia-platform-security&ft:locale=en-US)

