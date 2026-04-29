---
title: Java Apache Axis2 web services client examples advanced
description: Examples showing how to construct and use an Axis2 client to consume a ServiceNow Web Service.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Java Apache Axis2, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Java Apache Axis2 web services client examples advanced

Examples showing how to construct and use an Axis2 client to consume a ServiceNow Web Service.

Axis is essentially a SOAP engine -- a framework for constructing SOAP processors such as clients, servers, or gateways. The current version of Axis is written in Java. This content is intended for system admins with a light development background in Java. To begin you would need Java JDK version 1.4.2 or higher and Axis2 version 1.0 or higher.

## Create a Java Project

This example uses Eclipse SDK Version: 3.4.2 for managing the source code and executing the web request. Eclipse is not required.

-   Open Eclipse and from the menu select **File** &gt; **New** &gt; **Project** &gt; **Java Project**.
-   Give the project a name.
-   Verify that the correct JRE is specified.
    -   If using wsdl2java run "java -version" on the command line and this will be the version to specify for the project specific JRE.
    -   If using the Axis2 Codegen plugin use default JRE.

        ![](../image/JavaProject.png "Java Project")


## Generate your Axis2 client code

-   From a command line in the bin directory of the axis folder:

    ```
    ./wsdl2java.sh -uri https://<instance name>.service-now.com/incident.do?WSDL -o /glide/workspace/TestWebService/
    
    ```

-   In the above example:
    -   The "-uri" is either the path where you have saved a copy of the wsdl to either ".wsdl" or ".xml", or the URL the WSDL resides at.
    -   The "-o" is the path where you want the files to be written out to. If not specified, the files will be written out to the current bin location.
-   In Eclipse refresh the project and the generated Stub and CallbackHandler should now be displayed

    ![](../image/AxisStub.png "Axis Stub")


## Basic Authentication

```
HttpTransportProperties.Authenticator basicAuthentication  = new HttpTransportProperties. Authenticator ( ) ;
basicAuthentication. setUsername ( "admin" ) ;
basicAuthentication. setPassword ( "admin" ) ;
...
 ServiceNowStub proxy  = new ServiceNowStub ( ) ;
...
 
 proxy._getServiceClient ( ). getOptions ( ). setProperty (org. apache. axis2. transport. http. HTTPConstants. AUTHENTICATE, basicAuthentication ) ;
```

## Compatibility with Axis2 Versions 1.1 and higher

Chunking support is only available in HTTP Version 1.1. By default chunking is enabled in Axis2.xml for versions 1.1 and higher. ServiceNow does not support Chunking, so you will need to disable chunking at deployment time or at runtime.

-   Deployment time: One can disable HTTP chunking by removing or commenting out the following element from Axis2.xml

    ```
    <parameter name= "Transfer-Encoding" >chunked</parameter>
    ```

-   Runtime: User can disable the chunking using following property set in Client or Stub, versions 1.1.1 and higher only

    ```
    options.setProperty (org. apache. axis2. transport. http. HTTPConstants. CHUNKED,  Boolean. FALSE ) ;
    ```


## Creating Unique Packages

You can use the Axis2 parameter namespace2package \(ns2p\) to create unique package names. The parameter uses this format:

```
<Axis path>\bin\wsdl2java.bat -u -p cr2 -ns2p <namespace>=<package name> -uri <wsdl to convert>
```

For example:

```
<Axis path>\bin\wsdl2java.bat -u -p cr2 -ns2p http://www.service-now.com/change_request=my.change_request -uri change_request
```

**Parent Topic:**[Java Apache Axis2 web services client examples](c_JAAWbSrvcsClntEx.md)

