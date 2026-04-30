---
title: Security Operations Palo Alto Networks - Check and Block Value workflow
description: As security incidents are created and triaged to identify potential threats, you can use the Security Operations Palo Alto Networks - Check and Block Value workflow to automatically check and update IP addresses, URLs, and domains using External Dynamic Lists defined in Palo Alto Networks - Firewall.This activity is called by other activities to set the Firewall block request status to success or failure.After the workflow has identified a value that is not on the firewall, the record is routed for approval. Upon approval, this activity connects to the MID Server via your SSH credentials and invokes a script that adds the value to the firewall External Block List.This activity checks if the value \(IP, URL, or domain\) is included in its respective External Dynamic List/Dynamic Block List \(EDL/DBL\) on firewall. The EDL/DBL details are obtained from the firewall using an operational command, and a routine is performed to check if the value is blocked on the firewall.This action retrieves the API key from the firewall.The Palo Alto Firewall: Get Firewall Config flow action gets all the related firewall configuration information from the database, and makes it available for use by the subsequent action.This activity executes an operational command on the firewall to refresh the External Dynamic List from the source configured on the firewall. The output of this activity indicates whether the Refresh job has been queued up.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Palo Alto Networks - Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Operations Palo Alto Networks - Check and Block Value workflow

As security incidents are created and triaged to identify potential threats, you can use the **Security Operations Palo Alto Networks - Check and Block Value** workflow to automatically check and update IP addresses, URLs, and domains using External Dynamic Lists defined in Palo Alto Networks - Firewall.

## Before you begin

Role required: sn\_si.analyst

## About this task

The **Security Operations Palo Alto Networks - Check and Block Value** workflow is executed when Firewall Block Requests are submitted. The block request specifies the firewall to be used, the type of observable to be checked and blocked \(if needed\), and the block value. That is, the IP address, URL, or domain in question.

During workflow execution, commands defined under **Palo Alto Networks Integration** &gt; **Firewall** &gt; **Commands** are run. The Show type commands \(for example, Show-IP-ExternalDynamicList\) determine whether the value exists on the firewall. The Refresh type commands \(for example, Refresh-IP-ExternalDynamicList\) add value that do not exist on the firewall to the block list.

After the [Blocked Status](check-and-block-values.md#) activity executes, approval by a system administrator is required before the workflow can proceed.

![Palo Alto Networks Firewall - Check and Block workflow](../../secops-integration-palo-alto-firewall/image/check-and-block-wf.png "Security Operations Palo Alto Networks - Check and Block Value workflow")

## Procedure

1.  Navigate to **Palo Alto Networks Integration** &gt; **Firewall** &gt; **Block Requests**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Firewall

</td><td>

Select the firewall to be used.

</td></tr><tr><td>

Block Type

</td><td>

Select the type of value to be checked:-   IP
-   URL
-   DOMAIN


</td></tr><tr><td>

Block Value

</td><td>

Enter the value of the selected type to be checked on the firewall.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Palo Alto Firewall- Block Request Status activity

This activity is called by other activities to set the Firewall block request status to success or failure.

### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|firewallBlockRequestSysid \[string\]|The system id of the firewall block request. This input variable is mandatory.|
|status \[string\]|Indicates whether the refresh job ran: success or failure.|

### Output variables

The output variables contain data that can be used in subsequent activities. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|result \[string\]|Indicates whether the success or failure of the refresh job.|

## Palo Alto Firewall- Block Value activity

After the workflow has identified a value that is not on the firewall, the record is routed for approval. Upon approval, this activity connects to the MID Server via your SSH credentials and invokes a script that adds the value to the firewall External Block List.

### Input variables

Input variables determine the initial behavior of the activity.

**Note:** You must manually enter the input variables for this activity and then [publish the workflow](https://www.servicenow.com/docs/access?context=work-on-workflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US). If the workflow is not published, the input variables will not be saved for non-admin users.

|Variable|Description|
|--------|-----------|
|toBeBlockedValue \[string\]|The value to be added to the EDL if not already present. This input variable is mandatory.|
|typeToBeBlocked \[string\]|The type of value to be blocked: IP, URL, or Domain. This input variable is mandatory.|
|targetHost \[string\]|The MID Server on which the script is executed.|
|SSHCredentialTag \[string\]|The [SSH credential tag defined on the MID server](../../secops-integration-palo-alto-firewall/task/set-up-and-config-MID-server.md).|
|scriptCommand \[string\]|The AppendValueToList.sh script used to add the value to the EDL. It requires the full path to the MID Server.|

### Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|result \[string\]|The result passed to the EDL.|

## Palo Alto Firewall- Blocked Status activity

This activity checks if the value \(IP, URL, or domain\) is included in its respective External Dynamic List/Dynamic Block List \(EDL/DBL\) on firewall. The EDL/DBL details are obtained from the firewall using an operational command, and a routine is performed to check if the value is blocked on the firewall.

### Input variables

Input variables determine the initial behavior of the activity. All input variable entries listed are mandatory.

|Variable|Description|
|--------|-----------|
|valueToBeChecked \[string\]|The value in the block request.|
|showEDLDetailsCommand \[string\]|The External Dynamic List command being used to determine whether the value exists on the firewall.|
|FirewallIpAddress \[string\]|The IP address of the firewall used.|
|FirewallApiKey \[string\]|The firewall API key.|

### Output variables

The output variables contain data that can be used in subsequent activities. The output consists of data from the firewall configuration, as well as data dynamically generated using the Palo Alto Firewall Operational Command API message.

|Variable|Description|
|--------|-----------|
|commandResult \[string\]|The results from the firewall for the show EDL Details command.|
|blockedStatus \[Boolean\]|True indicates blocked. False indicates not blocked.|
|commandResponse \[string\]|The response status obtained from the firewall for the show EDL Details Command.|

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

## Palo Alto Firewall- Refresh EDL/DBL activity

This activity executes an operational command on the firewall to refresh the External Dynamic List from the source configured on the firewall. The output of this activity indicates whether the Refresh job has been queued up.

### Input variables

Input variables determine the initial behavior of the activity. All input variable entries listed are mandatory.

|Variable|Description|
|--------|-----------|
|FirewallIpAddress \[string\]|The IP address of the firewall being refreshed.|
|FirewallApiKey \[string\]|The refreshed firewall API key.|
|FirewallCommand \[string\]|The operational command to be executed to queue up the refresh job.|

### Output variables

The output variables contain data that can be used in subsequent activities. The output consists of data from the firewall configuration, as well as dynamically generated data.

|Variable|Description|
|--------|-----------|
|activity.Output.result \[string\]|A text string to indicate whether refresh job was queued to run: success or failure.|

