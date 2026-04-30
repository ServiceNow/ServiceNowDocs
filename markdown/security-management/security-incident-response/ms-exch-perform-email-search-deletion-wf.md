---
title: Microsoft Exchange - Perform Email Search and Deletion flow
description: When the Microsoft Exchange - Perform Email Search and Deletion flow is executed, it searches the Exchange server using the search query provided, and returns the details to the on-premises instance.The Create Compliance Search Preview Action creates a new compliance search action of type preview on the exchange server for the created compliance search.The Preview Action Status checks the status of compliance search action of type preview and returns the preview information of the emails found like recipient, sender, subject, email date received.The Create Compliance Search Delete Action creates a new compliance search action of type purge on the exchange server for the created compliance search.The Check Delete Action Status checks the status of compliance search action of type purge and performs soft delete operation on the exchange server for the emails found as a part of compliance search.The Remove Compliance Search action removes the created compliance search from exchange server.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Microsoft Exchange On-Premises integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Exchange - Perform Email Search and Deletion flow

When the **Microsoft Exchange - Perform Email Search and Deletion** flow is executed, it searches the Exchange server using the search query provided, and returns the details to the on-premises instance.

## Before you begin

Role required: sn\_si.analyst

## About this task

The **Microsoft Exchange - Perform Email Search and Deletion** flow is executed when email searches are set up and the **Delete from Email Server\(s\)** or **Search on Email Server\(s\)** button are pressed.

Actions specific to this integration are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration Flow Actions](../../../security-operations-common/concept/common-wf-activities.md).

The flow actions include:

-   [Create Compliance Search Action](../reference/get-email-details-from-exch-server.md)
-   [Check Compliance Search Status Action](../reference/search-delete-email-threat-exchange.md)

## Create Compliance Search Preview Action

The Create Compliance Search Preview Action creates a new compliance search action of type preview on the exchange server for the created compliance search.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

### Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Complete|When compliance search action is successfully created.|
|Error Creating Action|When creation of compliance search action fails due to exception in exchange server.|
|Error|When exception occurs in flow action.|

## Check Preview Action Status

The Preview Action Status checks the status of compliance search action of type preview and returns the preview information of the emails found like recipient, sender, subject, email date received.

### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

### Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|response|Contains the status of compliance search action and the preview information of the email found as a part of compliance search.|

### Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Preview in Progress|When status of compliance search action is in progress.|
|No Mail Found|When status of compliance search action is completed, and no emails are found as a part of compliance search.|
|Preview Complete|When status of compliance search action is completed, and emails are found as a part of compliance search.|
|Error Checking Status|When status checking fails due to exception in exchange server.|
|Error|When exception occurs in workflow activity.|

## Create Compliance Search Delete Action

The Create Compliance Search Delete Action creates a new compliance search action of type purge on the exchange server for the created compliance search.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

### Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Complete|When compliance search action is successfully created.|
|Error Creating Action|When creation of compliance search action fails due to exception in exchange server.|
|Error|When exception occurs in flow action.|

## Check Delete Action Status

The Check Delete Action Status checks the status of compliance search action of type purge and performs soft delete operation on the exchange server for the emails found as a part of compliance search.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

### Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|response|Contains the status of compliance search action and count of emails deleted, which were found as a part of compliance search.|

### Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Delete in Progress|When status of compliance search action is in progress.|
|No Mail Found|When status of compliance search action is completed, and no emails are deleted as a part of compliance search.|
|Delete Complete|When status of compliance search action is completed, and emails are deleted as a part of compliance search.|
|Error Checking Status|When status checking fails due to exception in exchange server.|
|Error|When exception occurs in flow action.|

## Remove Compliance Search Action

The Remove Compliance Search action removes the created compliance search from exchange server.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|targetId|Mandatory target host identifier field where the Exchange Server is located.|
|searchName|Mandatory name of compliance search created on exchange server.|

