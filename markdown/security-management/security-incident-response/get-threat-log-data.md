---
title: Get Log Data Flow
description: If Security Incident Response, Threat Intelligence, and Palo Alto Networks - Firewall are activated, the Security Operations Palo Alto Networks - Get Log Data flow automatically executes when the Source IP for observables in a security incident is changed.This action retrieves the API key from the firewall.The Palo Alto Firewall: Get Firewall Config flow action gets all the related firewall configuration information from the database, and makes it available for use by the subsequent action.The Palo Alto Firewall: Get Log flow action schedules a query on the firewall to retrieve logs and returns a JobID used to retrieve the log data.After the Palo Alto Firewall: Get Log action queues the search query to the firewall and the job runs, the Palo Alto Firewall: Job Data Action action retrieves the threat log data from the firewall.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Palo Alto Networks - Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get Log Data Flow

If Security Incident Response, Threat Intelligence, and Palo Alto Networks - Firewall are activated, the **Security Operations Palo Alto Networks - Get Log Data** flow automatically executes when the Source IP for observables in a security incident is changed.

## Before you begin

Role required: sn\_si.analyst

## About this task

During flow execution, firewall configuration information is retrieved from the database and the API Key is retrieved from the firewall. The Get Log action queues up a search query on the firewall. When the query runs, it returns a Job ID that is used to retrieve threat logs data from the firewall. It attaches the log data as an XML file to the security incident.

![Get Log Data flow](../image/get-log-data.png "Security Operations Palo Alto Networks - Get Log Data flow")

## Procedure

1.  Navigate to a security incident that contains observables.

2.  Click the **Security Incident Observables** tab.

3.  In **Source IP**, add or modify the IP address.

4.  Click **Update**.

    The **Security Operations Palo Alto Networks - Get Log Data** flow executes and enriched threat log data is attached to the security incident. The information is also parsed and displayed in the **Firewall Logs** section under the **Enrichment Data** tab.


## Palo Alto Firewall: Get API Key Action

This action retrieves the API key from the firewall.

### Input variables

Input variables determine the initial behavior of the action. All input variable entries listed are mandatory.

|Variable|Description|
|--------|-----------|
|Username \[string\]|The user name of the firewall administrator.|
|Password \[string\]|The firewall administrator password.|
|FirewallIpAddress \[string\]|The IP address of the firewall.|

### Output variables

The output variables contain data that can be used in subsequent actions. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|APIKey \[string\]|The firewall API key.|

## Palo Alto Firewall: Get Firewall Config Action

The **Palo Alto Firewall: Get Firewall Config** flow action gets all the related firewall configuration information from the database, and makes it available for use by the subsequent action.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|firewallSysid \[string\]|The system id of the firewall. This input variable is mandatory.|
|typeOfValueToBeBlocked \[string\]|The type of value to be blocked on the firewall: IP, URL, or Domain.|
|firewallIPAddress \[string\]|The IP address of the firewall.|

### Output variables

The output variables contain data that can be used in subsequent actions. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|ipEDLName \[string\]|The External Dynamic List name for IP addresses.|
|urlEDLName \[string\]|The External Dynamic List name for URLs.|
|domainEDLName \[string\]|The External Dynamic List name for domains.|
|firewallVersionSysId \[string\]|The system id for the firewall version.|
|refreshEDLCommand \[string\]|The command to be used to refresh the EDL from the source.|
|ShowEDLDetailsCommand \[string\]|The command to be used to get the EDL details.|
|status \[Boolean\]|True indicates success. False indicates failure.|
|error \[string\]|The error, if any, that occurred in the action.|
|endpoint \[Encrypted\]|The encrypted endpoint from the database.|

## Palo Alto Firewall- Get Log Action

The **Palo Alto Firewall: Get Log** flow action schedules a query on the firewall to retrieve logs and returns a JobID used to retrieve the log data.

### Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|FirewallIpAddress \[string\]|The IP address of the firewall. This input variable is mandatory.|
|FirewallApiKey \[string\]|The API access key of the firewall. This input variable is mandatory.|
|FirewallLogType \[string\]|The type of log data to be retrieved \(set to threat\). This input variable is mandatory.|
|FirewallLogFilterQuery \[string\]|The query to be executed to search for logs on the firewall. This input variable is mandatory.|
|LogDirection \[string\]|Specifies whether logs are shown oldest first \(backward\) or newest first \(forward\) order.|
|LogNumber \[string\]|Specifies the number of logs to retrieve.|
|LogSkipCount \[string\]|Specifies the number of logs to skip when doing a log retrieval.|

### Output variables

The output variables contain data that can be used in subsequent actions. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|QueuedJobID \[string\]|The Job ID returned from the firewall.|
|JobScheduled \[string\]|Specifies \(success or failure\) whether the job was sent to the firewall.|
|error \[string\]|Any errors returned.|

## Palo Alto Firewall- Job Data Action

After the **Palo Alto Firewall: Get Log** action queues the search query to the firewall and the job runs, the **Palo Alto Firewall: Job Data Action** action retrieves the threat log data from the firewall.

### Input variables

Input variables determine the initial behavior of the action. All input fields are mandatory.

|Variable|Description|
|--------|-----------|
|FirewallIpAddress \[string\]|The IP address of the firewall.|
|FirewallApiKey \[string\]|The API access key of the firewall.|
|JobID \[string\]|The ID of the queued job.|

### Output variables

The output variables contain data that can be used in subsequent actions. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|commandStatus \[string\]|Specifies \(success or failure\) whether data was retrieved from the firewall.|
|JobData \[string\]|The data collected from the firewall.|
|error \[string\]|Any errors returned.|

