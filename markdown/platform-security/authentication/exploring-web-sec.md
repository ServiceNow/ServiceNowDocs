---
title: Exploring Web service security
description: Enforce security using basic authentication, mutual authentication, or WS-Security.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Web service security, Authentication, Access Management]
---

# Exploring Web service security

Enforce security using basic authentication, mutual authentication, or WS-Security.

## Basic Authentication

To enforce basic authentication on each request for a WSDL document or posting of SOAP messages, you may set the property **glide.basicauth.required** to `true`. If you do so, each WSDL or SOAP request would have to contain the "Authorization" header as specified in the [Basic Authentication](http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html#BasicAA) protocol. Because the request is non-interactive, the **Authorization** header is always required during a request.

Supplying basic authentication information whether or not it is required has the added advantage that the data created or updated as a result of the Web Service invocation is done on behalf of the user supplied in the basic authentication credentials. As an example, when creating an Incident record, the journal fields have the user id of the basic authenticated user, instead of the default **Guest** user.

To make the authorization header ignore the capitalization rules, use the **glide.security.script.include.name.case.insensitive.list** property. You can modify this property in the System Properties \[sys\_properties\] table and add the script includes that are necessary to process the authentication. By default, this property has these values:

-   BasicAuth
-   CustomAuth

Add other script includes as needed.

To supply basic authentication when using Perl and the SOAP::Lite libraries, you can implement the following function:

```
sub SOAP :: Transport :: HTTP :: Client :: get_basic_credentials { return 'user_name' => 'password' ; }
```

-   When using C\# .NET VS 2005 or older, you can take advantage of the Credentials object, for example:

    ```
    System.Net . ICredentials cred  = new System.Net . NetworkCredential ( "user_name",  "password" ) ;
     
    service . ServiceNow proxy  = new service . ServiceNow ( ) ;
    service . get getService  = newservice . get ( ) ;
    service . getResponse getServiceResponse  = new service . getResponse ( ) ;
     
     try {
      proxy . Credentials = cred ;
      getService . sys_id = "bf522c350a0a140701972dbf876f1610" ;
      getServiceResponse  = proxy . get (getService ) ; catch (Exception ex ) { }
    ```

-   When using C\# .NET VS 2008, you can take advantage of the ClientCredentials object, for example:

    ```
    Demo_Incident. ServiceNowSoapClient client  = new Test08WebService . Demo_Incident . ServiceNowSoapClient ( ) ;
    client . ClientCredentials . UserName . UserName = "admin" ;
    client . ClientCredentials . UserName . Password = "admin" ;
    ```

    Then in your app.config file look for the following and change `None` to `Basic`:

    ```
    <transport clientCredentialType= "None" proxyCredentialType= "None" realm= "" />
    ```

-   When using VB .NET taking advantage of the Credentials object would look like the following:

    ```
    Sub Main()
             Dim cred  As New System.Net.NetworkCredential( "user_name",  "password")
     
             Dim proxy  As New VB_Democm.incident.ServiceNow
             Dim getIncident  As New VB_Democm.incident. get Dim getResponse  As New VB_Democm.incident.getResponse
     
            proxy.Credentials = cred
     
            getIncident.sys_id =  "[your sysID here]"
     
            getResponse = proxy. get(getIncident)
     
         End Sub
    ```

    The resulting response when Basic Authentication is turned on and no credentials are supplied looks like this:

    ```
    <html> <head > <title >Apache Tomcat/5.0.28 - Error report </ title > <style > <!--H1 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:22px;}    H2 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:16px;}    H3 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:14px;}    BODY {font-family:Tahoma,Arial,sans-serif;color:black;background-color:white;}    B {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;}    P {font-family:Tahoma,Arial,sans-serif;background:white;color:black;font-size:12px;}   A {color&nbsp;: black;}   A.name {color&nbsp;: black;}   HR {color&nbsp;: #525D76;}--> </ style > </ head > <body > <h1 >HTTP Status 401 -\ </ h1 > <HR size = "1" noshade = "noshade" > <p >< b >type </ b > Status report </ p > <p >< b >message </ b > <u >< / u >< / p > <p >< b >description </ b > <u >This request requires HTTP authentication (). </ u >< / p > <HR size = "1" noshade = "noshade" > <h3 >Apache Tomcat/5.0.28 </ h3 > </ body > </ html >
    ```


