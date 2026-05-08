---
title: Mobile deep link structure
description: Familiarize yourself with how to construct and use mobile deep links in any screen type within a mobile app.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Deep linking, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile deep link structure

Familiarize yourself with how to construct and use mobile deep links in any screen type within a mobile app.

Mobile deep links essentially consist of three components. The name of the variable, a reference to a mobile app, and the public method used to pull the mobile deep link. The following mobile deep link has a variable with the name `deepLinkGen`, where a specified screen opens in the Mobile Agent.

```java
var deepLinkGen= new global.MobileDeepLinkGenerator('Agent');
 return deepLinkGen.getScreenLink('73f3d135532033002d96ddeeff7b1212');
```

-   **Variable name**

    You can give any variable name for the mobile deep link, although it should be identifiable for future reference.

-   **Mobile app call**

    Enter one of the mobile apps that the mobile deep link points to. You can enter either `Request` for the Now Mobile app or `Agent` for the Mobile Agent app. For example, to generate a link using the mobile deep link generator that points to the Now Mobile app, use the following code: `new global.MobileDeepLinkGenerator('Request');`

-   **Public method**

    Use one of the public methods that can be used to create a mobile deep link. Reference the table for an explanation of each method, and the reason for its use.

<table id="table_nm2_jwd_ypb"><thead><tr><th>

Method

</th><th>

Reason for use

</th><th>

Method parameters

</th></tr></thead><tbody><tr><td>

`getButtonLink(buttonId, tableName, recordSysId)`

</td><td>

getButtonLink is used to link into any input form screen.

</td><td>

**buttonId** \(required\): sys\_id of the button you want to launch the input form screen**tableName** \(optional\): name of the table for the current context

 **recordSysId** \(optional\): sys\_id of the current context record

</td></tr><tr><td>

`getFormScreenLink(formScreenId, tableName, recordSysId)`

</td><td>

getFormScreenLink is used to link into any non-parameterized form screen.

</td><td>

**formScreenId** \(required\): sys\_id of required form screen**tableName** \(required\): table name of required form screen

 **recordSysId** \(required\): sys\_id of record from **tableName**

</td></tr><tr><td>

`getLauncherScreenLink(launcherScreenId)`

</td><td>

getLauncherScreenLink is used to link into any launcher screen.

</td><td>

**launcherScreenId** \(required\): sys\_id of the required launcher screen.

</td></tr><tr><td>

`getPrefillLink(forceLocalLogin)`

</td><td>

getPrefillLink is useful for first-time ServiceNow mobile users. This link format pre-fills the instance link for users who have not yet added an instance to their mobile app. This method is the default authentication experience.This method does not generate a link to a specific screen.

</td><td>

**forceLocalLogin** \(required\): Enter `true` for the system to pre-fill the instance login details of the user.

 Enter `false`, for the user to manually enter login details.

</td></tr><tr><td>

`getScreenLink(documentId, uiParams)`

</td><td>

getScreenLink is used to link into any list screens, including both parameterized and non-parameterized types. Can also be used for any non-parameterized screen type. An optional UI parameter can be passed into this method.

</td><td>

**documentId** \(required\): sys\_id of desired screen**uiParams** \(optional\): Parameter of a data item

</td></tr><tr><td>

`getSSOPrefillLink(sys_id)`

</td><td>

getSSOPrefillLink generates a link that uses the identity provider \(IdP\) that is identified by the `sys_id` parameter. This link can be used to authenticate end users that use different IdPs. For example, pre-hires might use Microsoft Azure as their IdP, and on-boarded employees might use Okta as their IdP. A common use of these SSO \(single sign-on\) pre-filled links is to embed them in emails sent to employees. These emails contain a link that can be used to log in securely to a ServiceNow instance using their mobile apps.**Important:** You must activate the Multi-Provider SSO plugin and have an active IdP to use this method. For more information, see Activate Multi-Provider SSO plugin

</td><td>

**sys\_id** \(required\): Enter the sys\_id of the IdP you want to use from the Identity Providers \[sso\_properties\] table.To get the sys\_id of the IdP:

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.
2.  Right-click an identity provider record and select **Copy sys\_id**.


</td></tr><tr><td>

`getUniversalLink(url)`

</td><td>

getUniversalLink generates a link into either a list, form, or browser. A screen is generated based on the content of this URL. See [Universal linking for mobile](../concept/universal-links-mobile.md).

</td><td>

**url** \(required\): a link to a resource on an instance

</td></tr></tbody>
</table>
**Parent Topic:**[Deep linking for mobile](../concept/deep-link-mobile.md)

