---
title: OCTimer - Global
description: The OCTimer script include provides methods to track the length of time it takes for a function to complete.Logs the entry based on the function name.Takes a millisecond value and returns a formatted duration.Calculates the time taken for each function registered.Initializes a timer based on the name provided.Registers the end of the timer for the provided name.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCTimer- Global

The OCTimer script include provides methods to track the length of time it takes for a function to complete.

This script include requires the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin to be activated. For more information, refer to the topic [Activate On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/t_ActivateOnCallScheduling.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCTimer - log \(String name, String entry\)

Logs the entry based on the function name.

|Name|Type|Description|
|----|----|-----------|
|name|String|Function name.|
|entry|String|Text that will be part of the output in the log.|

|Type|Description|
|----|-----------|
|void| |

## OCTimer - millisToTime \(Integer millis\)

Takes a millisecond value and returns a formatted duration.

|Name|Type|Description|
|----|----|-----------|
|millis|Integer|Duration in miliseconds.|

|Type|Description|
|----|-----------|
|String|A formatted duration.|

## OCTimer - result \(\)

Calculates the time taken for each function registered.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Time taken for each function registered.|

The following code example benchmarks the time taken by a REST API to fetch IP addresses from devices in Network Gear and then inserts them into IP Address table. API calls may require some time to process, so it is advisable to benchmark execution time before executing them in production.

```
var user = "<user name>"; // ServiceNow login user name
var password = "<password>";  // ServiceNow login password
var instance = "<instance name>";   // ServiceNow instance name

// Insert new IP address to IP address table using REST API
function insertIPAddress(ip_address) {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_ip_address');
 request.setHttpMethod('POST');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");
 request.setRequestHeader('Content-Type','application/json');request.setRequestBody("{\"ip_address\":\"" + ip_address + "\"}");
 var response = request.execute();
}

// Retrieve IP address from devices in Network gear
function getIPAddresses() {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_netgear?sysparm_fields=ip_address');
 request.setHttpMethod('GET');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");

 var response = request.execute();
 return response.getBody();
}

var timer = new OCTimer();             // create OCTimer object

// get the IP addresses from Network Gear table
timer.start("getIPAddresses");         // start timer to time fetching IP addresses from Network Gear table
var ipAddressStr = getIPAddresses();
timer.stop('getIPAddresses');          // stop timer

// insert IP addresses to IP Address table
var ipAddressJson = JSON.parse(ipAddressStr);  // parse result
var ipAddressList = ipAddressJson.result;      // extract IP addresses to a list
for (var i=0; i<ipAddressList.length;i++) {    // loop through
 var ip_address = ipAddressList[i]["ip_address"].trim();
 if (ip_address.length > 0) {
  timer.start("insertIPAddress");    // start timer to time inserting IP address to IP Address table
  insertIPAddress(ip_address);       // insert IP address
  timer.stop('insertIPAddress');     // end timer
 }
}

var result = timer.result();         // get timer results
gs.info(result);                     // output timer result

```

Output:

```
getIPAddresses method was invoked 1 time and took 00.288 seconds
insertIPAddress method was invoked 37 times and took 02.352 seconds
```

## OCTimer - start \(String name\)

Initializes a timer based on the name provided.

|Name|Type|Description|
|----|----|-----------|
|name|String|Function name.|

|Type|Description|
|----|-----------|
|void| |

The following code example benchmarks the time taken by a REST API to fetch IP addresses from devices in Network Gear and then inserts them into IP Address table. API calls may require some time to process, so it is advisable to benchmark execution time before executing them in production.

```
var user = "<user name>"; // ServiceNow login user name
var password = "<password>";  // ServiceNow login password
var instance = "<instance name>";   // ServiceNow instance name

// Insert new IP address to IP address table using REST API
function insertIPAddress(ip_address) {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_ip_address');
 request.setHttpMethod('POST');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");
 request.setRequestHeader('Content-Type','application/json');request.setRequestBody("{\"ip_address\":\"" + ip_address + "\"}");
 var response = request.execute();
}

// Retrieve IP address from devices in Network gear
function getIPAddresses() {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_netgear?sysparm_fields=ip_address');
 request.setHttpMethod('GET');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");

 var response = request.execute();
 return response.getBody();
}

var timer = new OCTimer();             // create OCTimer object

// get the IP addresses from Network Gear table
timer.start("getIPAddresses");         // start timer to time fetching IP addresses from Network Gear table
var ipAddressStr = getIPAddresses();
timer.stop('getIPAddresses');          // stop timer

// insert IP addresses to IP Address table
var ipAddressJson = JSON.parse(ipAddressStr);  // parse result
var ipAddressList = ipAddressJson.result;      // extract IP addresses to a list
for (var i=0; i<ipAddressList.length;i++) {    // loop through
 var ip_address = ipAddressList[i]["ip_address"].trim();
 if (ip_address.length > 0) {
  timer.start("insertIPAddress");    // start timer to time inserting IP address to IP Address table
  insertIPAddress(ip_address);       // insert IP address
  timer.stop('insertIPAddress');     // end timer
 }
}

var result = timer.result();         // get timer results
gs.info(result);                     // output timer result

```

Output:

```
getIPAddresses method was invoked 1 time and took 00.288 seconds
insertIPAddress method was invoked 37 times and took 02.352 seconds
```

## OCTimer - stop \(String name\)

Registers the end of the timer for the provided name.

|Name|Type|Description|
|----|----|-----------|
|name|String|Function name.|

|Type|Description|
|----|-----------|
|void| |

The following code example benchmarks the time taken by a REST API to fetch IP addresses from devices in Network Gear and then inserts them into IP Address table. API calls may require some time to process, so it is advisable to benchmark execution time before executing them in production.

```
var user = "<user name>"; // ServiceNow login user name
var password = "<password>";  // ServiceNow login password
var instance = "<instance name>";   // ServiceNow instance name

// Insert new IP address to IP address table using REST API
function insertIPAddress(ip_address) {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_ip_address');
 request.setHttpMethod('POST');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");
 request.setRequestHeader('Content-Type','application/json');request.setRequestBody("{\"ip_address\":\"" + ip_address + "\"}");
 var response = request.execute();
}

// Retrieve IP address from devices in Network gear
function getIPAddresses() {
 var request = new sn_ws.RESTMessageV2();
 request.setEndpoint('https://' + instance + '.service-now.com/api/now/table/cmdb_ci_netgear?sysparm_fields=ip_address');
 request.setHttpMethod('GET');

 request.setBasicAuth(user,password);
 request.setRequestHeader("Accept","application/json");

 var response = request.execute();
 return response.getBody();
}

var timer = new OCTimer();             // create OCTimer object

// get the IP addresses from Network Gear table
timer.start("getIPAddresses");         // start timer to time fetching IP addresses from Network Gear table
var ipAddressStr = getIPAddresses();
timer.stop('getIPAddresses');          // stop timer

// insert IP addresses to IP Address table
var ipAddressJson = JSON.parse(ipAddressStr);  // parse result
var ipAddressList = ipAddressJson.result;      // extract IP addresses to a list
for (var i=0; i<ipAddressList.length;i++) {    // loop through
 var ip_address = ipAddressList[i]["ip_address"].trim();
 if (ip_address.length > 0) {
  timer.start("insertIPAddress");    // start timer to time inserting IP address to IP Address table
  insertIPAddress(ip_address);       // insert IP address
  timer.stop('insertIPAddress');     // end timer
 }
}

var result = timer.result();         // get timer results
gs.info(result);                     // output timer result

```

Output:

```
getIPAddresses method was invoked 1 time and took 00.288 seconds
insertIPAddress method was invoked 37 times and took 02.352 seconds
```

