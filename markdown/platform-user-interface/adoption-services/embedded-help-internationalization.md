---
title: Embedded Help internationalization
description: Embedded help internationalization provides the ability for you to localize your embedded help content to a variety of languages to meet global user needs. You can write your embedded help content in a language of your choice and decide what languages to display.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Embedded Help planning, Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Embedded Help internationalization

Embedded help internationalization provides the ability for you to localize your embedded help content to a variety of languages to meet global user needs. You can write your embedded help content in a language of your choice and decide what languages to display.

Existing embedded help content records are written in English by default. You can translate the English embedded help content provided with the base system into other languages to meet your needs. You can also create custom embedded help content in the language of your choice.

## Understanding localized embedded help content

To translate English embedded help content into another language or to create embedded help content in a language other than English, your working session must be configured to the language in which you want to write. For example, you must be working in a French session if you want to write embedded help content in French. Refer to [Localization settings](https://www.servicenow.com/docs/access?context=system-localization-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

Configure embedded help content to display in the language of your choice by accessing the **Language** field on the Embedded Help Queue \[sys\_embedded\_help\_queue\] table. Depending on the foreign language translations activated on your instance, you can choose which language to display your embedded help content.

If embedded help content is available in a particular language and users are working in an instance with that language, they will see available embedded help in the desired language.

## Working with localized embedded help content

When a user requests an embedded help content record, the associated embedded help queue record populates accordingly and the language specified in the embedded help queue record is set to the current session language.

When embedded help content is available in a user's session language, content will be shown in that same language. If embedded help content is not available in the user's session language, than English content is shown. However, if you do not want to see English content in a non-English session, you can configure the sys\_property to False \(default is True\).

## Embedded help content prioritization

Displaying embedded help content in the user's session language takes priority over all other mechanisms, such as role, whether content is user-created, and the latest content version.

When a user is in a non-English working session, the priority for embedded help content display is as follows:

1.  Working-session language \(other than English\) content displays, if available.
2.  User-created content displays when working-session language content is not available.
3.  Version-related content displays when working-session language and user-created content are not available.

For example, if an admin user is in a French working session and requests embedded help content, but French content is not available for the admin role, the same-language content for a lower role is displayed if available.

If there is no embedded help content for the French admin role, but there is content for the French itil role and English admin role, the French itil role takes priority over the English admin role. The French-language content will display at the itil-role level.

-   **[Create internationalized embedded help](../task/create-international-embedded-help.md)**  
Translate provided English embedded help content into other languages or create custom embedded help content in the language of your choice.

**Parent Topic:**[Embedded Help planning](embedded-help-planning.md)

