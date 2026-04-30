---
title: Integrations Capabilities framework 2.0
description: The new Integration Capabilities Framework 2.0 has been redesigned to enable implementation of integrations in a simple and consistent manner. This ensures a consistent experience for similar types of integrations \(for example: observable reputation lookup\).The Security Incident Response plugin includes all the capability flows listed in Integration Capabilities Framework 2.0, and standard high-level filters that you can enable or disable depending on your requirement.This section describes the configurations available in the new framework.This section describes how to use the new framework for an existing integration.Use the steps below to create a flow and call the subflow provided by the new capability framework.The Capability Executions option provides detailed information on each capability that has been executed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Integrations Capabilities framework 2.0

The new Integration Capabilities Framework 2.0 has been redesigned to enable implementation of integrations in a simple and consistent manner. This ensures a consistent experience for similar types of integrations \(for example: observable reputation lookup\).

The new framework has capabilities implemented using [Flows](https://www.servicenow.com/docs/access?context=flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

Benefits from the enhanced framework implementation include:

-   The capability flows that include only business level components without any implementation specific logic.
-   The capability flows now accept a broad array of inputs and formats for maximum flexibility \(For example, observable references, CI references, tasks, any table or sys\_id combinations\).
-   Rate limiting or throttling on integration executions are now easy to configure \(removing the need to do this using custom code or changes to implementation workflows\).
-   Enhanced auditing and execution tracking capabilities now enable better reporting and easier troubleshooting.
-   Robust error handling functions are built into the capability flows to avoid duplicating implementation routines.
-   Ability to configure conditional triggering of the capabilities or the integrations. This provides flexibility to automatically launch automations based on incident category.
-   A default filter condition has been introduced on all capabilities to filter allow listed observables before inputs are provided to the integrations.

**Note:** This new capability framework does not upgrade the current capability framework. Both frameworks can work in parallel. For instructions on how to leverage the new capability framework, see [Using the new Capability Framework with an installed integration](cj-sir-capfmw-about.md#) and [Using the new Capability Framework with a Flow](cj-sir-capfmw-about.md#).

**Parent Topic:**[Security Operations Integration Reference](../../secops-integration-reference/concept/secops-integ-ref.md)

## Supported integrations and components

The Security Incident Response plugin includes all the capability flows listed in Integration Capabilities Framework 2.0, and standard high-level filters that you can enable or disable depending on your requirement.

**Note:** If you want to use the new Capability Integration Framework with the New York release, you must install the ServiceNow IntegrationHub Starter Pack Installer plugin. Contact Customer Support for assistance with the installation.

### Supported application versions

Starting with Security Incident Response 10.0, the following integrations are supported:

|Application|Minimum version required|
|-----------|------------------------|
|Security Operations Hybrid Analysis Integration|10.0.0|
|Security Operations PhishTank Integration|10.0.0|
|Security Operations ThreatCrowd Integration|10.0.0|
|Security Operations CrowdStrike Intelligence Integration|10.0.0|
|Security Operations 'Have I been pwned?' Integration|10.0.0|
|Security Operations Metadefender Integration|10.0.0|
|Security Operations Recorded Future Integration|10.0.0|
|Security Operations VirusTotal Integration|10.0.0|
|Security Operations Reverse WhoIs Integration|10.0.0|

Starting with Security Incident Response 10.4, the following integrations are supported:

|Application|Minimum version required|
|-----------|------------------------|
|Security Operations RiskIQ Integration|10.0.0|
|Security Operations Shodan Integration|10.0.0|
|Security Operations WhoIs Integration|10.0.0|
|Security Operations Carbon Black Integration|10.3.1|
|Security Operations Splunk Search Integration|10.3.0|
|Security Operations ArcSight Logger Integration|10.3.0|
|Security Operations McAfee ESM Integration|10.3.0|
|Security Operations Elasticsearch Integration|10.3.0|
|Security Operations IBM QRadar Integration|10.3.1|
|Security Operations CrowdStrike Falcon Host|10.3.0|

### Components included

The new Capability Integration Framework includes the following components:

-   **Capabilities**: All of the following capabilities that exist in the product today as workflows have been redesigned using [Flows](https://www.servicenow.com/docs/access?context=flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US):
    -   **Block Request**: Provides a way to block observables associated with a security incident on a firewall, web proxy, or some other control point. This capability is used during incident response investigations to contain an identified threat.
    -   **Email Search and Delete**: Provides a way to search an email server during a security investigation and if necessary, delete emails from the server.
    -   **Enrich Configuration Item**: Provides a general way to enrich configuration items with additional information from a variety of sources. This capability is used during incident response investigations to enrich data associated with a security incident.
    -   **Enrich Observable**: Provides a general way to enrich observables with additional information from a variety of sources. This capability is used during incident response investigations to contain an identified threat.
    -   **Event Ingestion**: Provides a general way to create a security incident by mapping events from an integration source to a security incident.
    -   **Get Network Statistics**: Retrieves a list of active network connections from an endpoint or host. This capability is used for incident enrichment during investigations.
    -   **Get Running Processes**: Retrieves a list of running processes from an endpoint or host. This capability is used for incident enrichment during investigations.
    -   **Isolate Host**: Provides a way to isolate an endpoint or a host associated with a security incident. Isolate host is executed against a configuration item \(CI\).
    -   **Publish to Watchlist**: Provides a way to add observables associated with a security incident to a watchlist that monitors for security events and generates alerts. This capability is used as part of incident response during investigations.
    -   **Sightings Search**: Searches various SIEMs or other log stores for instances of observables. This capability is used to determine the presence of malicious IoCs in your environment.
    -   **Threat Lookup**: Performs threat intelligence lookups to determine whether a certain observable is associated with a known security threat. This capability is used as part of incident response during investigations.
-   **New tables**:
    -   sn\_sec\_cmn\_capability: Capability and flow that implements the capability.
    -   sn\_sec\_cmn\_capability\_implementation: The actual implementation flow that provides the services of the capability.
    -   sn\_sec\_cmn\_capability\_execution: The execution record for a capability at runtime.
    -   sn\_sec\_cmn\_capability\_implementation\_execution: The execution record for a capability implementation at runtime.
    -   sn\_sec\_cmn\_filter\_condition: The filter conditions that can be applied at runtime to the capability or a capability implementation.
-   **Include script**: CapabilityProcessor: Handles all the processing code for the framework.
-   **Rate limit**: Capability Max Concurrent Req Per Period: Defines how many integrations can be executed in parallel.
-   **Scheduled job process capability implementation**: Runs every 15 seconds and can be disabled in the Security Administration Properties page \(**Security Incident** &gt; **Administration** &gt; **Properties**\).
    -   Enables or Disables the scheduled job, Process Capability Implementations: This job automatically schedules and manages capability implementation execution flows.
    -   Enables or Disables Automated Lookups or Enrichments: Setting that activates or deactivates the scheduled job that performs automated threat lookup or enrichment of observables when observables are added to security incidents in the current capability framework.
    -   Enables or Disables the scheduled job, Lookup Security Incident Observables: This job automatically schedules a Threat Lookup or Enrich Observables job when observables are added to a security incident.

## Configurations in the new Capability Framework

This section describes the configurations available in the new framework.

### Before you begin

Role required: sn\_si.admin, flow\_designer, action\_designer

### Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Capabilities**.

    **Note:** Version 10.4: Starting with Security Incident Response 10.4, the menu name **Capabilities** has been changed to **Integration Capabilities \(Flows\)**.

2.  The capabilities available with the base system are displayed.

    ![Capability flows: out-of-the-box](../image/cj-sir-capfmw-oob-cap.png)

    **Note:**

    These are the capabilities provided with the base system. You can use the capabilities, or you can customize them as required. The following steps describe how to configure a capability and the integrations implemented for the capability.

3.  Click the link in the Name column to configure a capability.

    The Name, Application, Description, and the Flow that the Capability implements is displayed.

    ![Capability flows: Configure capability](../image/cj-sir-capfmw-config1.png)

4.  Select the **Active** check box to activate the capability.

    -   **Filter conditions at the capability level**: When an integration capability implements a flow, the filter conditions associated with the flow will be executed before the capability flow is launched. For example, the Threat Lookup capability includes the Filter Allowlisted Observables condition as shown above. Click on the Name link to edit the filter condition.

        **Note:** Select the **Add worknote to task** checkbox to add worknotes to include information on the filter conditions used.

        ![Capability flows: configure capability: edit filter condition](../image/cj-sir-capfmw-config2.png)

        You can either define filter conditions or a script, or a combination of both. In the above example, a script is used to define the filter conditions. When the capability flow is executed, the script searches for allowlisted observables and removes them from the table.

        **Note:** The filter conditions set here are applicable to all active integrations defined in the **Capability Implementations** tab.

    -   **Capability implementations**: Click the **Capability Implementations** tab. The implementations \(integrations\) that have been configured for the capability are displayed. The example below shows the integrations configured for the Threat Lookup capability:

        ![Capability flows: Threat Lookup: Capability implementations](../image/cj-sir-capfmw-config3.png)

5.  Click the Name link to view the Capability Implementation.

    The Name, Application, Description, and the Flow that the capability implements is displayed.

6.  Click the **Active** checkbox to activate the capability.

    ![Capability flows: Threat Lookup: VirusTotal](../image/cj-sir-capfmw-config4.png)

    You can specify the following details:

<table id="simpletable_szm_sg5_xkb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Select this check box to enable disable this integration.**Note:** If you configure this integration using the integration tile in the **Security Operations** &gt; **Integrations** &gt; **Integrations Configurations**page, this flag is automatically set to **Active**.

</td></tr><tr><td>

Order

</td><td>

Indicates the order in which the integrations are executed.

</td></tr><tr><td>

Capability

</td><td>

The capability implemented by this integration.

</td></tr><tr><td>

Flow

</td><td>

The subflow that implements the capability.

</td></tr><tr><td>

Configuration

</td><td>

The integration configuration for this capability. **Note:** This is initially set to the default configuration provided with the base system. When an integration is configuring using the integration tile in the **Integration Configurations** page, this value is automatically reset to the new configuration created.

</td></tr><tr><td>

Rate Limit

</td><td>

Indicates the number of integrations that can be executed at run-time \(in parallel or per unit of time\).

</td></tr><tr><td>

Batch Inputs Size

</td><td>

The batch input size for each execution. For example, for a Sighting Search integration you may want to group the observables into batches of 50 so that the queries generated do not become too large. 0 indicates that there is no limit.

</td></tr><tr><td>

Timeout Period

</td><td>

The maximum duration before the capability implementation flow is cancelled. 0 indicates that there is no timeout period.

</td></tr><tr><td>

Total Requests

</td><td>

The total number of implementation execution requests. This field in conjunction with the Total Reqs Period field, can be used to limit the number of requests to the service. For example, you can limit the number to 4 requests per minute.

</td></tr><tr><td>

Total Reqs Period

</td><td>

The total number of execution requests allowed per period.

</td></tr><tr><td>

Retry Limit

</td><td>

The number of retries allowed for a failed execution request. This limit will be applicable if the **Retry** flag is set in your integration to retry an execution request when a condition is met. For example, a retry request is made when you have exceeded your license limit for that service for a time period or the service is down.

</td></tr><tr><td>

Retry After

</td><td>

The period after which an attempt is made to retry a failed execution request.

</td></tr><tr><td>

Max Concurrent Reqs

</td><td>

The maximum number of concurrent implementation execution requests. 0 indicates no limit.

</td></tr><tr><td>

Sighting Search Configurations

</td><td>

The default sighting search queries that can be executed.

</td></tr></tbody>
</table>    Click the Name link in the Filter Conditions section to configure the conditions defined for the implementation. Add or delete filter conditions, modify the script if required and update the record.

    ![Capability flows: Threat Lookup: VirusTotal: filter condition](../image/cj-sir-capfmw-config5.png)


## Using the new Capability Framework with an installed integration

This section describes how to use the new framework for an existing integration.

Use the steps below to enable an already installed and configured integration \(see supported list of Integrations in [Supported integrations and components](cj-sir-capfmw-about.md#)\) to use the new capability framework.

**Note:** Integration Capability Framework 2.0 available with Security Incident Response 10.0.2 supports implementations for the **Threat Lookup** and **Enrich Observable** capabilities. Implementations for other capabilities will be made available in a future release.

**Before you begin**

-   Role required: sn\_si.admin
-   Security Incident Response 10.0.2

1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Capabilities**.
2.  Click on **Threat Lookup** capability.
3.  Click the Capabilities Implementation tab.

    ![Capability framework: New capability](../image/cj-sir-capfmw-new-cap.png)

4.  4. View the Capability Implementation record for the integration of interest \(example: Crowdstrike Falcon Intelligence\). The **Active** column should have the value as **False**.
5.  Click the **Name** link to view the implementation record.

    ![Capability framework: New capability implementation record](../image/cj-sir-capfmw-new-cap-det.png)

6.  Select the **Active** check box.
7.  Ensure the implementation record is pointing to the right configuration record \(the tile name for the integration in **Integration Configurations** &gt; **Show Configurations \(Yes\)**\).

    ![Capability Framework: Configuration Tile](../image/cj-sir-capfmw-config-tile.png)

8.  The implementation is enabled for use with the new framework.

**Note:** All supported Integrations when installed with Security Incident Response 10.0.2 will automatically be enabled under the new Integration Capability framework.

## Using the new Capability Framework with a Flow

Use the steps below to create a flow and call the subflow provided by the new capability framework.

### Before you begin

-   Role required: sn\_si.admin, flow\_designer, action\_designer
-   Install one of the supported integrations \(see [Supported integrations and components](cj-sir-capfmw-about.md#)\)

The steps below describe how to create a sample flow and call one of the subflows provided with the new capability framework.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **New** to create a new flow and provide the necessary information for the properties.

    ![Capability Framework: Create new flow](../image/cj-sir-capfmw-create-flow.png)

    **Note:** Select **System User** in the Run As choice list as shown in the above image.

3.  Select a Trigger condition for the flow \(a common trigger is the creation of a security incident record for a certain incident category\).

    ![Capability Framework: Create new flow: trigger](../image/cj-sir-capfmw-create-flow-trigger.png)

4.  In step 1 of the flow, select an action to get inputs from the security incident \(for example, observables\).

    You can select an action from the actions provided with the base system with the Security Support Common Spoke.

    ![Capability Framework: Create new flow: action](../image/cj-sir-capfmw-create-flow-action.png)

5.  In step 2, select a subflow \(for example, Threat Lookup\).

    ![Capability Framework: Create new flow: subflow](../image/cj-sir-capfmw-create-flow-subflow.png)

6.  Configure the subflow you have selected as shown below:

    ![Capability Framework: Create new flow: configure subflow](../image/cj-sir-capfmw-create-flow-subflow-config.png)

7.  Save and publish the flow.


## Troubleshooting Integration Capability flows

The Capability Executions option provides detailed information on each capability that has been executed.

**Note:** Completed executions are archived after 30 days.

1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Capability Executions.**.

    ![Capability Framework: Capability Executions](../image/cj-sir-capfmw-execute-1.png)

2.  Click on the Capability Executions link to view additional details.

Security Incident Record Worknotes

When observables have been added to a security incident and the trigger condition for the flow is met, the Threat Lookup and Enrich Observable subflows are initiated and the following work notes are added to the security incident:

-   Flow execution started: Security Operations Integration - Enrich Observable V1
-   Flow execution completed: Security Operations Integration - Enrich Observable V1
-   Flow execution started: Security Operations Integration – Threat Lookup V1
-   Flow execution completed: Security Operations Integration – Threat Lookup V1

To view these worknotes, login as a user with the `sn_si.admin` or `sn_si.analyst`, and `flow_designer`, and `action_designer` roles.

Navigate to the security incident record page and click on these worknotes to view the flow execution details.

![Capability Framework: Security Incident: Worknotes](../image/cj-sir-capfmw-worknotes.png)

