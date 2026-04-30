---
title: AES properties
description: System properties control system behavior. The properties in this section are specific to the App Engine Studio \(AES\) application. You can access system properties for AES by navigating to All App Engine Studio Configuration Properties .
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [App Engine Studio reference, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# AES properties

System properties control system behavior. The properties in this section are specific to the App Engine Studio \(AES\) application. You can access system properties for AES by navigating to **All** &gt; **App Engine Studio** &gt; **Configuration** &gt; **Properties**.

-   **sn\_app\_eng\_studio.show\_servicenow\_studio\_banner**

    Controls whether the try ServiceNow Studio banner appears on the App Engine Studio home page. Set to true to show the banner or set to false to hide the banner.

    -   Type: true \| false
    -   Default value: true
-   **sn\_app\_eng\_studio.aes\_admin\_contact**

    Defines the contact email for the App Engine Studio administrator. The system sends deployment request notifications to each email address listed in this property. For more information, see [Add users to the App Engine Admin group](../task/add-users-to-admin-grp.md).

    -   Type: string
    -   Default value: none
-   **sn\_app\_eng\_studio.illustration\_supported\_content\_types**

    Defines the supported content types for Taxonomy Category illustrations. This property is read-only.

    -   Type: string
    -   Default value: image/svg+xml
-   **sn\_app\_intake.instance\_can\_provision\_users**

    Determines if the current instance can support the provisioning of users. The users on this instance will be provisioned to another instance. For more information on provisioning users, see [Configure Application Intake](../task/config-app-intake.md).

    -   Type: true \| false
    -   Default value: false

**Parent Topic:**[App Engine Studio reference](aes-reference.md)

