---
title: Java Apache Axis2 web services client examples insert
description: An example class to insert an incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/c\_JAAWbSrvcsClntExInst.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Java Apache Axis2, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Java Apache Axis2 web services client examples insert

An example class to insert an incident record.

```
public class Insert  {
 
  public static void main ( String args [ ] ) { try {
   HttpTransportProperties. Authenticator basicAuthentication  = new HttpTransportProperties. Authenticator ( ) ;
   basicAuthentication. setUsername ( "admin" ) ;
   basicAuthentication. setPassword ( "admin" ) ;
 
   ServiceNowStub proxy  = new ServiceNowStub ( ) ;
 
   proxy._getServiceClient ( ). getOptions ( ). setProperty (org. apache. axis2. transport. http. HTTPConstants. CHUNKED,  Boolean. FALSE ) ;
   proxy._getServiceClient ( ). getOptions ( ). setProperty (org. apache. axis2. transport. http. HTTPConstants. AUTHENTICATE, basicAuthentication ) ;
 
   ServiceNowStub. Insert inc  = new ServiceNowStub. Insert ( ) ;
   ServiceNowStub. InsertResponse resp  = new ServiceNowStub. InsertResponse ( ) ;
 
   inc. setAssigned_to ( "Christen Mitchell" ) ;
   inc. setCategory ( "hardware" ) ;
   inc. setPriority ( BigInteger. ONE ) ;
   inc. setDescription ( "The WI_FI in the reception area is down" ) ;
   inc. setCaller_id ( "Joe Employee" ) ;
 
   resp  = proxy. insert (inc ) ;
 
    System. out. println ( "New Incident: " + resp. getNumber ( ) ) ; } catch ( Exception e ) { System. out. println (e. toString ( ) ) ; }
 
  } }
```

**Parent Topic:**[Java Apache Axis2 web services client examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_JAAWbSrvcsClntEx.md)

