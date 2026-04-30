---
title: CheckInstanceTestBuilder - Scoped
description: The CheckInstanceTestBuilder script include provides methods that enable building test check requests on check instances.Creates an CheckInstanceTestBuilder instance.Builds the test check request with the arguments set.Sets the sys\_id of the check definition to test.Sets the sys\_id of the configuration item to run the test against.Sets the credentials alias sys\_id to use during the test.Sets the credentials alias name to use during the test. If the given value matches the name of multiple credentials aliases records, then one of them is chosen randomly.Sets the credentials sys\_id to use during the test.Sets the credentials name to use during the test. If the given value is the name of several credentials records, then one of them is chosen randomly.Sets the agent to run the test. Allowed only in case the tested check instance and policy are proxy.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CheckInstanceTestBuilder- Scoped

The CheckInstanceTestBuilder script include provides methods that enable building test check requests on check instances.

This script include requires the Agent Client Collector Framework \(sn\_agent\) store application and is provided within the `sn_agent` namespace. For more information, refer to [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

For the REST API solution, refer to [Agent Client Collector API](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#).

This script include provides methods that enable the following:

-   Set the check instance to test
-   Set the configuration item to run the test against

You can also specify one of the following identifiers to use during the test:

-   Credential sys\_id
-   Credential alias id
-   Credential name

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CheckInstanceTestBuilder - CheckInstanceTestBuilder\(\)

Creates an CheckInstanceTestBuilder instance.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following example shows how to initialize CheckInstanceTestBuilder.

```
var builder = new sn_agent.CheckInstanceTestBuilder();
```

## CheckInstanceTestBuilder - build\(\)

Builds the test check request with the arguments set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Properties|Description|
|----------|-----------|
|Object|JSON object with two attributes – the test result record ID and an error. If the build is successful, the test result ID returns and error is null. If an error occurs during the build, the test result ID is null and the error displays.|

The following example shows how build a test check request:

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var ciId = "cc0dcc855374301062d1ddeeff7b12b0";
var builder = new sn_agent.CheckInstanceTestBuilder();

var testResultJson = builder.withCheckId(checkId).withCiId(ciId).build();

if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCheckId\(String checkId\)

Sets the sys\_id of the check definition to test.

|Name|Type|Description|
|----|----|-----------|
|checkId|String|Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var ciId = "cc0dcc855374301062d1ddeeff7b12b0";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCiId(ciId).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCiId\(String ciId\)

Sets the sys\_id of the configuration item to run the test against.

|Name|Type|Description|
|----|----|-----------|
|ciId|String|Sys\_id of a CMDB Configuration Item.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how to create a test check request with

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var ciId = "cc0dcc855374301062d1ddeeff7b12b0";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCiId(ciId).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCredentialsAliasId\(String credentialsAliasId\)

Sets the credentials alias sys\_id to use during the test.

**Note:** Running this removes any previous assignment done by calling withCredentialsName, withCredentialsAliasId or withCredentialsAliasName.

|Name|Type|Description|
|----|----|-----------|
|credentialsAliasId|String|Sys\_id of a credentials alias record.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check and set the credentials alias ID.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var credAlias = "<sys_id>";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCredentialsAliasId(credAlias).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCredentialsAliasName\(String credentialsAliasName\)

Sets the credentials alias name to use during the test. If the given value matches the name of multiple credentials aliases records, then one of them is chosen randomly.

**Note:** Running this removes any previous assignment done by calling withCredentialsName, withCredentialsAliasId or withCredentialsAliasName.

|Name|Type|Description|
|----|----|-----------|
|credentialsAliasName|String|Name of a credentials alias.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check and set the credentials alias name.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var credentialsAliasName = "credentialsAliasName";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCredentialsAliasName(credentialsAliasName).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCredentialsId\(String credentialsId\)

Sets the credentials sys\_id to use during the test.

**Note:** Running this removes any previous assignment done by calling withCredentialsName, withCredentialsAliasId or withCredentialsAliasName.

|Name|Type|Description|
|----|----|-----------|
|credentialsId|String|Sys\_id of a credentials record.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check and set the credentials ID.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var credID = "<sys_id>";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCredentialsId(credID).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withCredentialsName\(String credentialsName\)

Sets the credentials name to use during the test. If the given value is the name of several credentials records, then one of them is chosen randomly.

**Note:** Running this removes any previous assignment done by calling withCredentialsName, withCredentialsAliasId or withCredentialsAliasName.

|Name|Type|Description|
|----|----|-----------|
|credentialsName|String|Name of the credentials record.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check and set the credentials name.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var credname = "credentialsName";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withCredentialsName(credName).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

## CheckInstanceTestBuilder - withProxyAgentId\(String agentId\)

Sets the agent to run the test. Allowed only in case the tested check instance and policy are proxy.

|Name|Type|Description|
|----|----|-----------|
|agentId|String|Unique ID of an agent proxy to run this check. This value is listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

|Type|Description|
|----|-----------|
|CheckInstanceTestBuilder|The builder instance the method was invoked for.|

The following example shows how create a test check and set the proxy agent ID.

```
var checkId = "158279505372b30034b8ddeeff7b1270";
var agentId = "<agentID>";
var builder = new sn_agent.CheckInstanceTestBuilder();
var testResultJson = builder.withCheckId(checkId).withAgentId(agentId).build();
if (!gs.nil(testResultJson.error))
	gs.error(testResultJson.error);
```

