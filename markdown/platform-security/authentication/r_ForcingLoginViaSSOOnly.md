---
title: Redirect single sign-on \(SSO\) logins
description: When SSO is enabled, you can redirect users to specific pages or direct users to login locally.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Redirect single sign-on \(SSO\) logins

When SSO is enabled, you can redirect users to specific pages or direct users to login locally.

For example, if a user attempts to go to `https://customerX.service-now.com`, an internal company portal can display instead of the default login page. Or, when a user logs out of an application, the browser can redirect them to a specific internal page. You can set redirection properties within the instance to ensure that users see an SSO login page rather than the default login page.

**Note:** The following properties do not force SSO. The login.do page is still accessible and users can login to the system if they have a local password set.

## Redirection properties

When a user logs out, or if there is a failed attempt to sign on using SSO, you can define where the user is taken next, such as a main portal page or a knowledge base article with SSO login information. Use the following properties to specify the URLs. If one of these properties does not exist in your instance, you can create the property.

-   **glide.authenticate.honor.sso\_record.failed\_requirement\_redirect**

    URL to redirect users when they attempt to access a page that is private \(for example, to view an incident\) and do not provide SSO credentials. The property is typically set to a customer's login portal \(for example, `http://portal.companya.com/`\).

-   **glide.authenticate.failed\_redirect**

    URL to redirect users after a failed SSO attempt. You can redirect to a public knowledge article that describes the error and has helpful links \(for example, `http://portal.companya.com/error`\).

-   **glide.authenticate.external.logout\_redirect**

    URL to redirect users after logging out, typically back to the portal that enabled the single sign-on log in \(for example, `http://portal.companya.com/logout`\).

-   **glide.authentication.external.disable\_local\_login**

    When set to true, requires SSO credentials for the main login page. Defaults to false. This property needs to be used in conjunction with the **glide.authenticate.honor.sso\_record.failed\_requirement\_redirect** property.


The following table shows the relationship between the Installation Exit return values, the properties, and the expected behavior.

|Return value|Property|Behavior|
|------------|--------|--------|
|`failed_missing_requirement`|**glide.authenticate.honor.sso\_record.failed\_requirement\_redirect**|When this value is returned, it indicates that the required SSO credentials are not present in the session. Login fails and the session is redirected to the URL specified by the property. This is usually the URL for the SSO provider where login is challenged and credentials are collected.|
|`failed_authentication`|**glide.authenticate.failed\_redirect**|When this value is returned, it indicates that the supplied SSO credentials failed authentication, the user does not exist, or the user is locked out. Login fails and the session is redirected to the URL specified by the property. This is usually the URL for the SSO provider where login is challenged and credentials are collected.|
|`<*user\_id*>`|N/A|Login authorized for the user specified by &lt;*user\_id*&gt;. This value matches with the field name defined in the SSO property **glide.authenticate.header.value** \("the instance's field name to match against the incoming header"\)|

## Restricting local login

As a security precaution, you should do more than rely on redirection properties to prohibit logging in locally. If a user should never log in locally and will always be authenticated by your internal single sign-on system, then a random password should be assigned to each user that is imported into the instance. The random password is most easily set at the time of the user import. If the user data is imported into your system through an import set, you can create an onBefore transform script using the following code .

```
var r  = new Packages. java. util. Random ( ) ;

 var str1  = Packages. java. lang. Long. toString (Packages. java. lang.
 Math. abs (r. nextLong ( ) ) , 36 ) ; var str2  = Packages. java. lang.
 Long. toString (Packages. java. lang. Math. abs (r. nextLong ( ) ) , 36
 ) ;

 var newPass  = str1  + str2 ;

target. user_password = newPass ;

 //password now set to a random string like this:
 //qvm81zdrn7cwwylpvw94eebk
```

