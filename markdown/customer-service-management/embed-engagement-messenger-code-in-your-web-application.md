---
title: Embed Engagement Messenger in your web application
description: Embed the source code of the messenger module that you configured in your website so that you can enable your customers to start using Engagement Messenger in your website.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Embed Engagement Messenger in your web application

Embed the source code of the messenger module that you configured in your website so that you can enable your customers to start using Engagement Messenger in your website.

## Before you begin

-   [Activate an Engagement Messenger module](activate-engagement-messenger-module.md).
-   Role required: sn\_csm\_ec.ec\_admin

## About this task

Copy the source code of the messenger module that you activated and paste it in the HTML file of the website where you want to deploy the messenger.

Next, depending on the authentication type that you selected for your configured messenger module, you may have to write code for functions to get the ID token and to start and stop the session for a logged-in user in the messenger.

## Procedure

1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

2.  In the Edit module column of the messenger module that you want to install in your website, click **Edit**.

    The guided configuration view is displayed.

3.  Click the **Implement** tab.

4.  If you have done any changes to the Security settings section, click **Save**.

    The code of the Engagement Messenger module is updated.

5.  Scroll down to the Embed code section and click **Copy code**.

6.  Open the HTML file of your website and paste the copied code before the closing body tag.

7.  For a messenger module with OIDC-based or SAMl-based authentication, complete the following configuration.

<table id="choicetable_vhq_vtl_p4b"><thead><tr><th align="left" id="d97980e153">

Authentication type

</th><th align="left" id="d97980e156">

Action

</th></tr></thead><tbody><tr><td id="d97980e162">

**OIDC-based**

</td><td>

1.  Write code for the getTokenCallBack\(\) function.
2.  Call the SN\_CSM\_EC.onLogin\(\) function whenever users log in to your website.

This function enables authenticated users to log in to Engagement Messenger seamlessly when they log in to your website.

3.  Call the SN\_CSM\_EC.onLogout\(\) function whenever users log out from your website.

This function enables authenticated users to seamlessly log out from Engagement Messenger and your website.

</td></tr><tr><td id="d97980e202">

**SAML-based**

</td><td>

1.  Call the SN\_CSM\_EC.onLogin\(\) function whenever users log in to your website.

This function enables authenticated users to log in to Engagement Messenger seamlessly when they log in to your website.

2.  Call the SN\_CSM\_EC.onLogout\(\) function whenever users log out from your website.

This function enables authenticated users to seamlessly log out from Engagement Messenger and your website.

</td></tr></tbody>
</table>    **Note:** For more information about setup for OIDC and SAML-based authentication, see [Setting up auto login and logout for Engagement Messenger \[KB1560205\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1560205) article in the Now Support Knowledge Base.

8.  If you enabled the walk-up feature for unauthenticated users, uncomment the **//guestWalkupBaseUrl** code line and complete the configuration by entering the base URL of your customer support portal.

    For example, if your customer support portal is **https://www.example.com/support**, then update the code to **guestWalkupBaseUrl = https://www.example.com/support**

    ![Configure Engagement Messenger module with the help of the highlighted steps. For the implementation, use the embed code to fix any unauthenticated user issues.](../image/em-embed-code-with-walk-up.png "Copy Engagement Messenger code")

9.  To modify the embed code to set the preferred language in which Engagement Messenger is displayed, do one of the following.

    |Option|Description|
    |------|-----------|
    |**`lang: {ISO-locale code}`**|Enables you to load Engagement Messenger with a fixed language.|
    |**`setLang : getEMLanguage`**|Allows you to dynamically switch the language in which Engagement Messenger is displayed. The `getEMLanguage` value can return any ISO-locale code which can be used for messenger language.|

    The `setLang : getEMLanguage` function takes preference when both parameters are available. However, if the user has set the preferred language in the \[sys\_user\_preference\] table, Engagement Messenger will be displayed in that language.

    **Note:** Beginning with the Australia release, the upgraded customers can also modify the embed code to enable language switching.

10. Open the website to which you added the Engagement Messenger code to verify that the launcher icon is available and click the icon to verify that it launches Engagement Messenger.

11. Modify the embed code of Engagement Messenger to integrate Proactive Recommendations on a web page.

    For more information on using Engagement Messenger to integrate Proactive Recommendations on a web page, see [Use Engagement Messenger embed Code to integrate proactive recommendations on a web page](em-contextual-help.md).


## What to do next

Open the website that you added the Engagement Messenger code to and verify that the launcher icon of the messenger is available. Click the icon to launch the Engagement Messenger.

You can also embed Engagement Messenger in your native iOS and android applications using Now Mobile SDK:

-   [Embed Engagement Messenger in a native iOS app using Now Mobile SDK \[KB1587276\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1587276)
-   [Embed Engagement Messenger in a native android app using Now Mobile SDK \[KB1587611\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1587611)

