---
title: Continuous Integration and Continuous Delivery \(CICD\) Spoke
description: Build a Continuous Integration and Continuation Delivery \(CICD\) pipeline for your ServiceNow instances. You can automate publishing and installing applications from an application repository, activating plugins, running ATF test suites, and running an instance scan.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Continuous Integration and Continuous Delivery \(CICD\) Spoke

Build a Continuous Integration and Continuation Delivery \(CICD\) pipeline for your ServiceNow instances. You can automate publishing and installing applications from an application repository, activating plugins, running ATF test suites, and running an instance scan.

## CICD spoke application

The CICD spoke application is installed by default from the Orlando upgrade onward.

## Spoke version

Continuous Integration and Continuous Delivery \(CICD\) spoke v1.0.11 is the latest version.

## Supported versions

Continuous Integration and Continuous Delivery \(CICD\) REST API version 1.0.0, which is a ServiceNow AI Platform feature active by default.

## Spoke flows

This spoke has no sample flows.

## Spoke subflows

The Continuous Integration and Continuous Delivery \(CICD\) spoke provides sample subflows in the draft state to demonstrate automating CICD tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

<table id="table_hbd_qty_qfb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Plugin

</td><td>

Activate a plugin by ID on the specified instance URL.

</td></tr><tr><td>

Apply Changes From Source Control With ID

</td><td>

Apply remote changes from source control to an application by its Sys ID.

</td></tr><tr><td>

Apply Changes From Source Control With Scope

</td><td>

Apply remote changes from source control to an application by its scope name.

</td></tr><tr><td>

ATF Suite Start With ID

</td><td>

Start a test suite by its Sys ID on the specified instance URL. Return the test suite execution results.

</td></tr><tr><td>

ATF Suite Start With Name

</td><td>

Start a test suite by its name on the specified instance URL. Return the test suite execution results.

</td></tr><tr><td>

Batch Install

</td><td>

Given a Batch Plan in JSON format, install multiple packages \(applications, customizations to store applications, and plugins\) together in a single batch operation. Example JSON:```
{
  "applications": [
    {
      "id": "syd_id_abcefghi",
      "type": "application",
      "load_demo_data": false,
      "requested_version": "1.0.2",
      "notes": "User specific text to describe this application install"
    },
    { 
      "id": "syd_id_defabcde",
      "type": "application",
      "requested_version": "1.0.0",
      "requested_customization_version": "2.0.7",
      "notes": "Customization for CSM App1"
    },
    {
      "id": "com.glide.some.plugin",
      "type": "plugin",
      "load_demo_data": true,
      "notes": "Plugin related notes"
    }
  ],
  "rollback_on_failure": true
}
```

</td></tr><tr><td>

Batch Results

</td><td>

Given the sys\_id of a result object, view the installation status of each package along with entire batch plan.

</td></tr><tr><td>

Batch Rollback

</td><td>

With a rollback ID, roll back the installation\(s\) of package\(s\) installed as a single batch.

</td></tr><tr><td>

Get Instance Scan Results

</td><td>

Return Instance Scan execution results by progress ID. Scan\_results always return but scan\_finding results display only if present.

</td></tr><tr><td>

Import Application from Source Control

</td><td>

Import Application from Source Control using repository URL on the given instance.

</td></tr><tr><td>

Instance Scan Execute Full Scan

</td><td>

Start full Instance Scan on specified instance URL. Scan runs with all active checks.

</td></tr><tr><td>

Instance Scan Execute Point Scan

</td><td>

Start Instance Scan on specified instance starting from a particular table and record \(the table and sys\_ID\). Target is scanned using all relevant and applicable checks.

</td></tr><tr><td>

Instance Scan Execute Suite Scan

</td><td>

Start full Instance Scan on specified instance URL using a specific suite of checks.

</td></tr><tr><td>

Instance Scan Execute Suite Scan on one or more scoped apps

</td><td>

Start Instance Scan on specified scoped apps using checks from a specified suite ID.

</td></tr><tr><td>

Instance Scan Execute Suite Scan on one or more update sets

</td><td>

Start Instance Scan on the specified update sets using checks from a specified suite ID.

</td></tr><tr><td>

Install Application With ID

</td><td>

Install an application by its Sys ID from the application repository.

</td></tr><tr><td>

Install Application With Scope

</td><td>

Install an application by its scope name from the application repository.

</td></tr><tr><td>

Publish Application With ID

</td><td>

Publish an application by its Sys ID to the application repository.

</td></tr><tr><td>

Publish Application With Scope

</td><td>

Publish an application by its scope name to the application repository.

</td></tr><tr><td>

Rollback Application With ID

</td><td>

Roll back an application by its Sys ID. Confirm the rollback version number matches the specified version number or produce an error.

</td></tr><tr><td>

Rollback Application With Scope

</td><td>

Roll back an application by its scope name. Confirm the rollback version number matches the specified version number or produce an error.

</td></tr><tr><td>

Rollback Plugin

</td><td>

Roll back a plugin by ID on the specified instance URL to the last installed version.

</td></tr><tr><td>

Wait Until Tracker Completes

</td><td>

Wait for a tracker to complete its progress on the specified instance URL and return the results.

</td></tr></tbody>
</table>## Spoke actions

The Continuous Integration and Continuous Delivery \(CICD\) spoke provides actions to automate CICD tasks when events occurs in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Application Repo|Install Application With ID|Install an application by its Sys ID from the application repository.|
|Install Application With Scope|Install an application by its scope name from the application repository.|
|Publish Application With ID|Publish an application by its Sys ID to the application repository.|
|Publish Application With Scope|Publish an application by its scope name to the application repository.|
|Rollback Application With ID|Rollback an application by its Sys ID. Confirm the rollback version number matches the specified version number or produce an error.|
|Rollback Application With Scope|Roll back an application by its scope name. Confirm the rollback version number matches the specified version number or produce an error.|
|ATF|ATF Get Suite Results|Return the test suite execution results by Sys ID.|
|Get Execution Tracker Progress|Return tracker progress information by Sys ID.|
|Start ATF Suite With ID|Start a test suite by its Sys ID on the specified instance URL.|
|Start ATF Suite With Name|Start a test suite by its name on the specified instance URL.|
|Batch Install|Batch Install|Install multiple applications at once|
|Batch Results|View installation status of each package along with entire batch plan.|
|Batch Rollback|With a rollback ID, roll back the installation\(s\) of package\(s\) installed as a single batch.|
|Instance Scan|Get Instance Scan Results|Return Instance Scan execution results by progress ID. Scan\_results always display but scan\_finding results display only if present.|
|Instance Scan Execute Full Scan|Return Instance Scan execution results by progress ID. Scan\_results always return but scan\_finding results display only if present.|
|Instance Scan Execute Point Scan|Start full Instance Scan on specified instance URL. Scan runs with all active checks.|
|Instance Scan Execute Suite Scan|Start Instance Scan on specified instance starting from a particular table and record \(the table and sys\_ID\). Target is scanned using all relevant and applicable checks.|
|Instance Scan Execute Suite Scan on one or more scoped apps|Start full Instance Scan on specified instance URL using a specific suite of checks.|
|Instance Scan Execute Suite Scan on one or more update sets|Start Instance Scan on specified scoped apps using checks from a specified suite ID.|
|Plugin|Activate Plugin|Activate a plugin by ID on the specified instance URL.|
|Rollback Plugin|Rollback a plugin by ID on the specified instance URL to the last installed version.|
|Source Control|Apply Changes From Source Control With ID|Apply remote changes from source control to an application by its Sys ID.|
|Apply Changes From Source Control With Scope|Apply remote changes from source control to an application by its scope name.|
|Import Application from Source Control|Import Application from Source Control using repository URL on the given instance.|

## CICD account requirements

The Continuous Integration and Continuous Delivery \(CICD\) spoke requires creating basic authorization credentials. The user credentials must have either the admin or sn\_cicd.sys\_ci\_automation roles to authorize CICD actions and flows.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the CICD alias record to authorize actions on local and remote instances. For information about setting up the spoke, see [Set up the Continuous Integration and Continuous Delivery \(CICD\) spoke](../task/set-up-cicd.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the CICD alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

