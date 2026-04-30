---
title: Create a new WS-Security profile
description: Create a new WS Security profile to define how to authenticate a web services message when WS-Security is enabled.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Create a new WS-Security profile

Create a new WS Security profile to define how to authenticate a web services message when WS-Security is enabled.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **WS Security Profiles**.

2.  Click **New**.

3.  Fill in the WS-Security Profile form \(see table\).

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the security profile.|
    |Type|Select **X509** to verify the request's certificate. Select **Username** to verify the request's user credentials.|
    |Run as user|Select the ServiceNow user the instance will impersonate if authentication succeeds and the **Bind Session** field is selected. All web services requests will be attributed to this user. For example, if you select the **System Administrator** user then the instance treats all web services operations as being done by the system administrator. Make sure the user you select has appropriate SOAP privileges if you are using the `glide.soap.strict_security` high security setting. This field is only visible when the type is **X509**.|
    |Order|Enter the order in which the instance checks security profiles. The instance checks all security profiles when processing an incoming SOAP request. If a request fails any security profile authentication requirement, the instance stops processing additional security profiles and fails the request.|
    |Bind Session|Select this check box to have the instance impersonate the user listed in the **Run as user** field. You should only set this field for one profile at a time. If multiple profiles have this field selected, ServiceNow impersonates the user from the last successfully authenticated WS-Security profile. If no profile has this field selected, ServiceNow impersonates the user provided with the basic authentication headers or impersonates the default user \(Guest\).|
    |X509 Certificate|Select the certificate record containing the certificate for web service requests. ServiceNow only validates the request signature. It automatically trusts the certificate's certificate authority \(CA\). This field is only visible when the type is **X509**.|
    |Profile action|Select how you want the instance to authenticate the user credentials. Select **Authenticate with user** if you want the instance to authenticate the request based on an existing user record. The request's credentials must match values in an existing user record. Select **Specify user to authenticate** if you want to list a user name and password combination that all web services requests must meet. The request's credentials must match the user name and password you list. This field is only visible when the type is **Username**.|
    |User field to match UserName|Select the column from the User \[sys\_user\] table containing the value you want match against the request's UserName. For example, if you select **Email** then the request UserName header must contain an email address matching an existing ServiceNow user. This field is only visible when the profile action is **Authenticate with user**.|
    |User name|Enter the user name that all web services requests must contain. This field is only visible when the profile action is **Username**.|
    |User password|Enter the password that all web services requests must contain. This field is only visible when the profile action is **Username**|

    ![WS-Security Profile](../image/WS-SecurityProfile.png)

4.  Click **Submit**.


**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

**Related topics**  


[SOAP web services security](../concept/c_SOAPWebService.md#SOAP-web-services-security)

[WS-Security](../concept/c_SOAPWebService.md#WS-Security)

[WS-Security profiles](../concept/c_SOAPWebService.md#WS-Security-profiles)

