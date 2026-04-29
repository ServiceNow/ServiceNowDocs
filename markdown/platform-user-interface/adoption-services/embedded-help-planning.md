---
title: Embedded Help planning
description: Before writing custom embedded help, plan the content and note the information used in the Embedded Help form. Careful planning ensures that the topic appears for the right page and role.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Embedded Help planning

Before writing custom embedded help, plan the content and note the information used in the Embedded Help form. Careful planning ensures that the topic appears for the right page and role.

Each UI page can display embedded help, specified in the **Page** field as shown in the following example.

![Page name in URL pointing to page name in form](../image/embedded-help-planning-form.png "Embedded help topic for the Service Catalog home page")

In planning for embedded help topics, consider how the following fields are used and note the values that you need for your custom topics.

-   **Page**

    Identify and note the UI page name which is found in the URL when the page is displayed as shown. If the page name begins with a dollar sign, such as $mid\_server\_user, include the dollar sign in the page name. Before you write an embedded help topic for the page, search for the page name to locate a file you can copy.

-   **Modifier**

    -   **Normal** content appears for any user with the appropriate role who navigates to the page.
    -   **Setup** content appears when the page is accessed from a link in Guided Setup.
    Many embedded help topics in the base system are for Guided Setup. You can copy **Setup** content and change the **Modifier** to **Normal** to quickly provide help for all users.

-   **Qualifier**

    Identify pages you want custom help for that are used in many applications. For example the `home.do` page opens for every Homepage module and for many Dashboard modules. The embedded help administrator can use qualifiers to customize content for a common page in the instance.

-   **Role**

    Specify the lowest level role to provide access to this embedded help topic. All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page.

    For example, if you add embedded help content for the itil role that describes your business process for entering incidents, the itil\_admin role also sees the content. If you write a different topic with the itil\_admin role, the itil\_admin sees that content instead of the itil content.

-   **Product**

    Write content only for the **Enterprise** topic. You can copy an **Express** topic and change this field to **Enterprise** if appropriate.

-   **Version**

    Base system content is typically specified to the current software version. If you are editing the content for a custom application or to provide information relevant to your organization business process, select **All**.

-   **Domain**

    If your organization uses domain separation and customizes help content, specify the domain the content applies to.

-   **ServiceNow Help**

    If the check box is selected, this field indicates a base system topic. You cannot edit a base system topic, but you can create a copy to add custom content.

-   **Content**

    You can use the formatting tools to format the content. The following list describes the limitations.

    -   You cannot include images in embedded help content.
    -   To embed video, you must code the video information in the source code &lt;**&lt;&gt;**&gt; view. Video content from YouTube and Vimeo are supported.
    -   To add a related information link, you must use a full URL, not a relative URL.
    -   Best practice is not to use the highlight text tool, as the color may make text unreadable depending on the theme the user has selected.
    -   Any changes you make to embedded help are not automatically deployed to another instance.
    -   Changes to the embedded help table are not captured in update sets, update\_sync=false is set intentionally.

-   **[Use qualifiers in Embedded Help](../task/embedded-help-qualifiers.md)**  
The embedded help administrator can use qualifiers to customize content for a common page in the instance.
-   **[Embedded Help roles](embedded-help-roles.md)**  
Embedded help content can be targeted to users with a specified role who access the UI page. All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page.
-   **[Embedded Help internationalization](embedded-help-internationalization.md)**  
Embedded help internationalization provides the ability for you to localize your embedded help content to a variety of languages to meet global user needs. You can write your embedded help content in a language of your choice and decide what languages to display.

**Parent Topic:**[Configuring Embedded Help](configuring-embedded-help.md)

