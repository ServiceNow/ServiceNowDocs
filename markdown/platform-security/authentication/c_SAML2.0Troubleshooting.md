---
title: SAML 2.0 troubleshooting
description: Before contacting support, try the troubleshooting solutions available in the knowledge base on Hi.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# SAML 2.0 troubleshooting

Before contacting support, try the troubleshooting solutions available in the knowledge base on Hi.

**Note:** The instance does not support solutions provided by external sites.

See the following knowledge base article: [KB0540617 '''SAML Error Matrix'''](https://support.servicenow.com/kb_view.do?sysparm_article=KB0540617).

<table id="table_e5z_lcd_np"><thead><tr><th>

Error or Symptom

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Error message: "is not a function." This issue might occur in a multi-node environment. If the plugin does not get activated on all nodes, an error like the following appears:

 org.mozilla.javascript.EcmaError: **\[JavaPackage org.opensaml.saml2.core.impl.AuthnRequestBuilder\]** is not a function.

</td><td>

This error occurs because the plugin was not active and did not load the .jar file. Therefore, the code appears to be missing. Contact Technical Support to restart nodes that are missing the plugin.

</td></tr><tr><td>

SAML does not authenticate users accessing CMS pages.

</td><td>

By default, CMS pages are public and therefore do not require authentication. If you want SAML to authenticate CMS pages, change the view\_content.do public page from active=true to active=false.

</td></tr><tr><td>

Cannot redirect a user back to a CMS page after SAML authentication.

</td><td>

By default, the SSO integration uses a URL parameter called URI to control where the user is directed after authentication at the IdP. SSO ignores relative URLs. For example, SSO cannot redirect users to a /ess relative URL. Instead, the user has to navigate to a URL such as /nav\_to.do?uri=/ess, which uses deep linking syntax. However, this puts the ESS portal inside the main navigation content IFrame. In other words, the site does not take up the full page, but rather loads as a page in your instance. For more information, see CMS Sites and Single Sign-On.

 If you change the CMS entry page to make it private by setting view\_content.do to active=false, deep linking behavior then requires a customization to the Installation Exit login script. Create a script that looks for the URI portion of the URL and constructs a RelayState URL parameter containing the relative URL path to redirect users after authenticating at the IdP.

</td></tr><tr><td>

SAML does not redirect users to the appropriate page after authentication.

</td><td>

Determine if the relay state is passed out to the IdP and then passed back during authentication. You can do this with a browser capable of saving HTTP request headers and POST info, such as Chrome with its built-in developer tools, or Firefox with the add-on called HTTPfox. For Internet Explorer, use a third-party application such as Fiddler. The goal is to watch the requests pass from the client \(browser\) to the instance, and from the client to the IdP.

</td></tr></tbody>
</table>