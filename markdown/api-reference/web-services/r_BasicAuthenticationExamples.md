---
title: Basic authentication code samples
description: Samples of basic authentication code for several programming languages and versions.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Basic authentication code samples

Samples of basic authentication code for several programming languages and versions.

## Perl and the SOAP::Lite libraries

To supply basic authentication when using Perl and the SOAP::Lite libraries, you can implement the following function:

```
sub SOAP::Transport::HTTP::Client::get_basic_credentials {
   return 'user_name' => 'password';
}
```

## C\# .NET VS 2005 or older

When using C\# .NET VS 2005 or older, you can take advantage of the Credentials object. For example:

```
System.Net.ICredentials cred = new System.Net.NetworkCredential("user_name", "password");
 
service.ServiceNow proxy = new service.ServiceNow();
service.get getService = newservice.get();
service.getResponse getServiceResponse = new service.getResponse();
 
try
{
  proxy.Credentials = cred;
  getService.sys_id = "bf522c350a0a140701972dbf876f1610";
  getServiceResponse = proxy.get(getService);
catch (Exception ex) { }
```

## C\# .NET VS 2008

When using C\# .NET VS 2008, you can take advantage of the ClientCredentials object. For example:

```
Demo_Incident.ServiceNowSoapClient client = new Test08WebService.Demo_Incident.ServiceNowSoapClient();
client.ClientCredentials.UserName.UserName = "admin";
client.ClientCredentials.UserName.Password = "admin";
```

Then in your `app.config` file look for the following and change "None" to "Basic":

```
<transport clientCredentialType="None" proxyCredentialType="None" realm="" />
```

## VB .NET

When using VB .NET taking advantage of the Credentials object would look like the following:

```
 Sub Main()
        Dim cred As New System.Net.NetworkCredential("user_name", "password")
 
        Dim proxy As New VB_Democm.incident.ServiceNow
        Dim getIncident As New VB_Democm.incident.get
        Dim getResponse As New VB_Democm.incident.getResponse
 
        proxy.Credentials = cred
 
        getIncident.sys_id = "[your sysID here]"
 
        getResponse = proxy.get(getIncident)
 
    End Sub
```

The resulting response when Basic Authentication is turned on and no credentials are supplied looks like this:

```
 <html>
 <head>   
 <title>Apache Tomcat/5.0.28 - Error report</title>   
 <style>   <!--H1 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:22px;} 
  H2 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:16px;} 
  H3 {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;font-size:14px;} 
  BODY {font-family:Tahoma,Arial,sans-serif;color:black;background-color:white;} 
  B {font-family:Tahoma,Arial,sans-serif;color:white;background-color:#525D76;} 
  P {font-family:Tahoma,Arial,sans-serif;background:white;color:black;font-size:12px;}
  A {color: black;}
  A.name {color: black;}
  HR {color: #525D76;}-->   
  </style>   
  </head>   
  <body>   
  <h1>HTTP Status 401 -\</h1>   
  <HR size="1" noshade="noshade">   
  <p><b>type</b> Status report</p>   
  <p><b>message</b> <u></u></p>   
  <p><b>description</b> 
  <u>This request requires HTTP authentication ().</u></p>   
  <HR size="1" noshade="noshade">   
  <h3>Apache Tomcat/5.0.28</h3>   
  </body>   
  </html>
```

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

