---
title: Java Apache Axis2 web services client examples update
description: An example of an Axis Client program that calls the getKeys function to query all incidents where the category is Hardware.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Java Apache Axis2 web services client examples, Inbound web service examples, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Java Apache Axis2 web services client examples update

An example of an Axis Client program that calls the getKeys function to query all incidents where the category is Hardware.

## getKeys

A list of `sys_id` is returned as a result:

```
package com.service_now.www ;
 
 public class DemoClient  {
 
  public static void main ( String args [ ] ) { try {
   ServiceNowStub proxy  = new ServiceNowStub ( ) ;
   ServiceNowStub. GetKeys getInc  = new ServiceNowStub. GetKeys ( ) ;
   ServiceNowStub. GetKeysResponse resp  = new ServiceNowStub. GetKeysResponse ( ) ;
 
   getInc. setActive ( true ) ;
   getInc. setCategory ( "hardware" ) ;
 
   proxy._getServiceClient ( ). getOptions ( ). setProperty (org. apache. axis2. transport. http. HTTPConstants. CHUNKED,  Boolean. FALSE ) ;
 
   resp  = proxy. getKeys (getInc ) ;
 
    String [ ] keys  = resp. getSys_id ( ) ;
 
    System. out. println ( "Key: " + keys [ 0 ] ) ; } catch ( Exception e ) { System. out. println (e. toString ( ) ) ; }
 
  } }
```

## getRecords

```
package com.service_now.www ;
 
 import com.service_now.www.ServiceNowStub.GetRecordsResult_type0 ;
 
 public class GetRecords  {
 
 /**
* @param args
*/ public static void main ( String [ ] args ) { try {
  ServiceNowStub proxy  = new ServiceNowStub ( ) ;
  ServiceNowStub. GetRecords incidents  = new ServiceNowStub. GetRecords ( ) ;
  ServiceNowStub. GetRecordsResponse result  = new ServiceNowStub. GetRecordsResponse ( ) ;
 
  incidents. setActive ( true ) ;
  incidents. setCategory ( "hardware" ) ;
  incidents. setSys_created_on ( "> 2009-06-08 10:30:00" ) ;
 
  proxy._getServiceClient ( ). getOptions ( ). setProperty (org. apache. axis2. transport. http. HTTPConstants. CHUNKED,  Boolean. FALSE ) ;
 
  result  = proxy. getRecords (incidents ) ;
 
  GetRecordsResult_type0 [ ] keys  = result. getGetRecordsResult ( ) ;
 
   for ( int key  = 0 ; key  < keys. length ; key ++ ) { System. out. println ( "Key: " + keys [ 0 ]. getSys_id ( ) ) ; } } catch ( Exception e ) { System. out. println (e. toString ( ) ) ; }
 
 
 }
 
 }
```

**Parent Topic:**[Java Apache Axis2 web services client examples](c_JAAWbSrvcsClntEx.md)

