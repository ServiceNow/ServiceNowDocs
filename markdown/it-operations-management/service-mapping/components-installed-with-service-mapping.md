---
title: Components installed with Service Mapping
description: Several types of components are installed with activation of the Service Mapping plugin, including tables, user roles, properties, and scheduled jobs.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Components installed with Service Mapping

Several types of components are installed with activation of the Service Mapping plugin, including tables, user roles, properties, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

<table id="table_ncv_xhf_pt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\[app\_service\_admin\]

</td><td>

Creates and modifies service instances, creates service groups, views, and edits service instance maps.

</td><td>

\[itil\]

</td></tr><tr><td>

\[app\_service\_user\]

</td><td>

Views maps for operational service instances and retrieves service content using the getContent - GET REST API. The itil role that serves as the basic helpdesk technician role contains the app\_service\_user role.

</td><td>

\[cmdb\_read\]

</td></tr><tr><td>

\[itom\_admin\]

</td><td>

Configure IT Operations Management applications using the ITOM Guided Setup. **Note:** The ITOM Guided Setup does not cover Service Mapping.

</td><td>

\[sn\_bm\_client.benchmark\_data\_viewer\]\[sm\_itom\_license.reader\]

</td></tr><tr><td>

\[sam\_core\_admin\]

</td><td>

An internal role.

</td><td>

\[sam\_core\_user\]

</td></tr><tr><td>

\[sam\_core\_user\]

</td><td>

An internal role.

</td><td>

\[itil\]

</td></tr><tr><td>

\[service\_mapping\_admin\]

</td><td>

Sets up the Service Mapping application. Maps, fixes, and maintains service instances. Also performs advanced configuration and customization of the product. Assign this role to application administrators.

</td><td>

-   \[app\_service\_admin\]
-   \[app\_service\_owner\]
-   \[discovery\_admin\]
-   \[itil\_admin\]
-   \[itom\_admin\]
-   \[sam\_core\_admin\]
-   \[personalize\_dictionary\]
-   \[pd\_admin\]
-   \[pd\_user\]
-   \[service\_mapping\_user\]

</td></tr><tr><td>

\[sm\_app\_owner\]

</td><td>

Provides information necessary for successful mapping of a service instance. Once a service is mapped, this user reviews the results and either approves it or suggests changes. Assign the sm\_app\_owner role to users who own service instances and are familiar with the infrastructure and applications that make up the services.

</td><td>

\[service\_mapping\_user\]

</td></tr><tr><td>

\[sm\_itom\_license.reader\]

</td><td>

Views subscription information and statistics for IT Operations Management applications.

</td><td>

\[cmdb\_read\]

</td></tr><tr><td>

\[service\_mapping\_user\]

</td><td>

Views maps for operational service instances to plan change or migration, as well as analyze the continuity and availability of services. Assign this role to application users.

</td><td>

-   \[sam\_core\_user.service\_mapping\_user\]
-   \[itil.service\_mapping\_user\]

</td></tr><tr><td>

\[sn\_svc\_err.admin\]

</td><td>

Fixes discovery errors in bulk using the error framework feature in Service Mapping and Discovery.

</td><td>

\[itil\]

</td></tr><tr><td>

\[pd\_admin\]

</td><td>

Creates new and modifies existing patterns, which Service Mapping and Discovery use for performing horizontal and top-down discovery.

</td><td>

\[pd\_user\]

</td></tr></tbody>
</table>**Note:** Users with the sn\_cmdb\_editor or itil role only can view all service instances.

## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deferred Discovery Cleanup \[sysauto\_script\_ba4bee737f0022008f1c3b19befa9108\]

</td><td>

Runs every minute. Detects and cancels discovery schedules on TCP connections that are not in the active state anymore \(5 minutes of no activity\).

</td></tr><tr><td>

Update Query Based Services \[sysauto\_script\_08745913f31131002e6bae4716612bf1\]

</td><td>

Runs every 10 minutes. Updates views for all defined technical services.

</td></tr><tr><td>

Update App Service Status \[sysauto\_script\_5641702ac32102003e76741e81d3ae9e\]

</td><td>

Runs every minute. Updates the discovery status attribute for application services. The discovery status is calculated as the overall status over all endpoints that an service instance contains.

</td></tr><tr><td>

Flow Discovery Scheduler \[sysauto\_script\_74c676f0dbb0220060ff742eaf9619f2\]

</td><td>

Runs every 10 minutes. Triggers the network flow discovery and writes the data into the \[sa\_flow\_connector\] table. This scheduled job is disabled by default. Enable this scheduled job to discover CIs using Netflow as described in [Data collection and discovery using Netflow](../concept/data-collection-netflow-mapping.md).

</td></tr><tr><td>

Generate entry point candidates from netflow and netstat data \[sysauto\_script\_b0b95067c3d0030039a3553a81d3aeb5\]

</td><td>

Runs daily. Scans the TCP Connection \[cmdb\_tcp\] table and uses this data to generate entry points and store them in the Candidate Entry Points \[sa\_cand\_entry\_point\] table. This scheduled job supports generating entry points necessary for [mapping multiple application services \(in bulk\)](../task/map-business-services-in-bulk.md). This scheduled job is enabled by default.

</td></tr><tr><td>

Save thread dumps \[sysauto\_script\_a49cd030c302020039a3553a81d3aefb\]

</td><td>

Not active by default. When enabled, collects thread dumps and stores the data in the \[sys\_thread\_dump\] table.

</td></tr><tr><td>

Slow steps stats persist \[sysauto\_script\_dc0de690c302020039a3553a81d3aee0\]

</td><td>

Runs every minute. Collects data on slow execution of pattern steps and writes this data into the \[sys\_step\_pattern\] table.

</td></tr><tr><td>

Calculate number of servers \[sys\_trigger\_db438f407f510200f128134f8dfa91c6\]

</td><td>

Runs every Sunday. Updates the licensing metric with the overall number of discovered servers on instance. This information is used for billing. On domain separated instances, the number is updated for each domain.

</td></tr><tr><td>

Run DNS Lookup For All Entry Points and Manual Connection Endpoints \[f178ab457fb213001952baf8befa91d3\]

</td><td>

Runs the DNS lookup probe on all entry points and manual connection endpoints and updates information on their IP addresses in the CMDB. This scheduled job is disabled by default.

</td></tr><tr><td>

\[sm dedup tracker for specific discovery sources\]

</td><td>

In some cases, Service Mapping and third-party discovery or monitoring tools identify the same configuration item \(CI\) differently. It results in the CMDB application table containing two records for the same CI. This scheduled job scans the CMDB application tables that contain information about CIs identified as generic applications. If the scheduled job identifies duplicate records based on the CI type and the discovery source, it creates a deduplication task.

</td></tr><tr><td>

\[sys\_auto\_flush\_5211e7e1c320220039a3553a81d3aee6\]

</td><td>

Cleans the \[sa\_flow\_connection\] table from records not updated for the last seven days.

</td></tr><tr><td>

\[sys\_auto\_flush\_956d498b938503006a7031f6357ffbec\]

</td><td>

Cleans the \[sa\_performance\_statistics\] table from records containing statistics of overall event processing time and created earlier than 30 days ago.

</td></tr><tr><td>

\[sys\_auto\_flush\_ce1a978193001200e0e931f6357ffb59\]

</td><td>

Cleans the \[sa\_performance\_statistics\] table from records created earlier than 2 days ago.

</td></tr><tr><td>

\[sys\_auto\_flush\_b24d9c30c302020039a3553a81d3ae53\]

</td><td>

Cleans the \[sys\_thread\_dump\] table from records created earlier than 7 days ago.

</td></tr><tr><td>

\[sys\_auto\_flush\_cf129ebe7f223200995cbaf8befa916f\]

</td><td>

Cleans the \[sa\_ml\_feature\_data\] table from records not updated in the last 7 days, and have a special state \(empty label field\).

</td></tr><tr><td>

\[sys\_auto\_flush\_d2516be1c320220039a3553a81d3ae21\]

</td><td>

Cleans the \[sa\_flow\_service\] table from records not updated in the last 7 days.

</td></tr><tr><td>

\[sys\_auto\_flush\_db416be1c320220039a3553a81d3ae1f\]

</td><td>

Cleans the \[sa\_flow\_server\_comm\] table from records not updated in the last 7 days.

</td></tr><tr><td>

\[sys\_auto\_flush\_41d9b007b71310105984eb25de11a96e\]

</td><td>

Cleans the Connection Suggestion \[sa\_ml\_connection\_suggestion\] table from the old records that match the following conditions: -   They weren't updated in the last 7 days.
-   The suggestion record has an active discovered TCP connection \(the TCP connection record is not absent\).
-   The record doesn't have a user decision “Add” or “Remove” associated with it.

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Tables installed

<table id="table_xqr_k1n_kx"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pre Service Mapping Task Scripts \[sa\_pre\_task\_script\]

</td><td>

Contains scripts that Service Mapping runs on the instance and collect information that helps identify the relevant pattern for a CI.

</td></tr><tr><td>

Traffic Based Connection Qualifiers \[cmdb\_ci\_qualifier\_traffic\_based\_connection\]

</td><td>

Legacy content. Not used in the current version.

</td></tr><tr><td>

Dynamic CI Group \[cmdb\_ci\_query\_based\_service\]

</td><td>

Contains technical services.

</td></tr><tr><td>

Components \[sa\_bs\_components\]

</td><td>

Contains information on components that are part of the service instance. Customers enter this information manually in the Questionnaire tab of the service instance form.

</td></tr><tr><td>

Candidate Entry Points \[sa\_cand\_entry\_point\]

</td><td>

Contains information on potential entry points that Service Mapping retrieved from load balancers or traffic-based connections.

</td></tr><tr><td>

Dashboard View \[sa\_dashboard\_view\]

</td><td>

Contains configuration that defines which services to display in the Service tree.

</td></tr><tr><td>

Service Discovery Messages \[sa\_discovery\_message\]

</td><td>

Contains discovery messages and errors that Service Mapping generates during the discovery process.

</td></tr><tr><td>

ITOM Error task \[sa\_error\_handler\_task\]

</td><td>

Contains information that Service Mapping and Discovery use for error-handling functionality.

</td></tr><tr><td>

Error EP AS Manual EP \[sa\_errors\_as\_manual\_ep\]

</td><td>

Contains data on errors that customers skip during the following procedure: [Skip errors to continue discovering an application service](../task/skip-errors-continue-discovery-individual-services.md).

</td></tr><tr><td>

Manual connections \[sa\_manual\_connections\]

</td><td>

Contains information on endpoints that customers use while adding manual connections.

</td></tr><tr><td>

ML Feature Data \[sa\_ml\_feature\_data\]

</td><td>

Internal table.

</td></tr><tr><td>

ML Model \[sa\_ml\_model\]

</td><td>

Internal table

</td></tr><tr><td>

ML Traffic Validation \[sa\_ml\_traffic\_validation\]

</td><td>

Internal table

</td></tr><tr><td>

Performance Statistics \[sa\_performance\_statistics\]

</td><td>

Internal table for storing performance data on impact calculation in Event Management.

</td></tr><tr><td>

Service Maps \[sa\_service\_counters\]

</td><td>

Stores data about number of CIs and discovery errors per each discovered service.

</td></tr><tr><td>

Simulation entry points \[sa\_simulation\_entry\_points\]

</td><td>

Internal table.

</td></tr><tr><td>

Service Process Tasks \[service\_process\_task\]

</td><td>

Stores data requests and review requests for application services.

</td></tr><tr><td>

Slow Steps \[sys\_step\_pattern\]

</td><td>

Stores information about slow execution of pattern steps. This data is used for monitoring and troubleshooting.

</td></tr><tr><td>

Thread dump \[sys\_thread\_dump\]

</td><td>

Internal table for storing performance data used for troubleshooting in Event Management.

</td></tr><tr><td>

Automation Error Category \[automation\_error\_category\]

</td><td>

Stores all supported categories for errors.

</td></tr><tr><td>

Automation Error Categories Statistics \[automation\_error\_category\_stats\]

</td><td>

Stores the latest error statistics on all error categories.

</td></tr><tr><td>

Automation Error Code \[automation\_error\_code\]

</td><td>

Stores all supported error codes for discovery errors.

</td></tr><tr><td>

Automation Error Code Statistics \[automation\_error\_code\_stats\]

</td><td>

Stores the latest error statistics on all error codes.

</td></tr><tr><td>

Automation Error Discovery Categories Statistics \[automation\_error\_discovery\_category\_stats\]

</td><td>

Deprecated.

</td></tr><tr><td>

Automation Error Discovery Code Statistics\[automation\_error\_discovery\_code\_stats\]

</td><td>

Deprecated.

</td></tr><tr><td>

Automation Error Discovery Message \[automation\_error\_discovery\_msg\]

</td><td>

Stores the latest error messages.

</td></tr><tr><td>

Automation error instance category statistics \[automation\_error\_instance\_category\_stats\]

</td><td>

Stores the latest error statistics on all categories per instance \(discovery status\).

</td></tr><tr><td>

Automation Error Categories Statistics\[automation\_error\_instance\_code\_stats\]

</td><td>

Stores the latest error statistics on all error codes per instance \(discovery status\).

</td></tr><tr><td>

Automation error instance message \[automation\_error\_instance\_msg\]

</td><td>

Stores all latest errors associated with the instance \(discovery status\).

</td></tr><tr><td>

Automation error instance message\[automation\_error\_stats\_update\_time\]

</td><td>

Stores the last statistics update time for every application.

</td></tr><tr><td>

Automation Error Suggestion \[automation\_error\_suggestion\]

</td><td>

Contains all the configured suggestions that presented in the UI per different error codes.

</td></tr><tr><td>

Automation Source Application \[automation\_source\_application\]

</td><td>

Contains the source applications that are using the Discovery and Service Mapping error framework.

</td></tr><tr><td>

Mapping between suggestion and error code \[suggestion\_error\_code\_m2m\]

</td><td>

Contains information on mapping between error code and suggestion.

</td></tr><tr><td>

ITOM Error task \[sa\_error\_handler\_task\]

</td><td>

Contains the tasks configured per different groups of errors.

</td></tr><tr><td>

Applicative Credentials\[sa\_applicative\_credentials\]

</td><td>

Contains credentials used when running application-specific commands on servers.

</td></tr><tr><td>

Service Mapping CI attributes \[sa\_ci\_attr\]

</td><td>

Contains CI attributes relevant only for discovery process.

</td></tr><tr><td>

Related CI Types \[sa\_ci\_to\_pattern\]

</td><td>

Assigns CI types to patterns \(relevant only for the horizontal discovery performed by Discovery\).

</td></tr><tr><td>

Pattern Debugger Session\[sa\_debug\_session\]

</td><td>

This internal table is used for the Pattern Designer components.

</td></tr><tr><td>

Pattern Debugger Session Status for UI\[sa\_debug\_session\_status\]

</td><td>

This internal table is used for the Pattern Designer components.

</td></tr><tr><td>

Sa Deferred Service Discovery\[sa\_deferred\_service\_discovery\]

</td><td>

This internal table is used for Service Mapping components.

</td></tr><tr><td>

Service Discovery Log\[sa\_discovery\_log\]

</td><td>

Contains discovery logs collected by Service Mapping.

</td></tr><tr><td>

Service Discovery Messages\[sa\_discovery\_message\]

</td><td>

Contains messages created by Service Mapping during service discovery.

</td></tr><tr><td>

Sa Endpoint Status\[sa\_endpoint\_status\]

</td><td>

Contains discovery status for endpoints in Service Mapping.

</td></tr><tr><td>

Find Host Scripts\[sa\_find\_host\_scripts\]

</td><td>

Contains the names of script includes that find hosts based on the endpoint glide records.

</td></tr><tr><td>

nfdump file\[sa\_flcon\_file\_nfdump\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

nfdump install\[sa\_flcon\_local\_nfdump\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

AWS VPC flow logs\[sa\_flcon\_vpc\_flow\_log\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

SA Flow Connection\[sa\_flow\_connection\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

Flow Connector\[sa\_flow\_connector\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

Flow Server Communication\[sa\_flow\_server\_comm\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

Flow Services IP/Port and Statistics\[sa\_flow\_service\]

</td><td>

This internal table contains information used for Netflow-based discovery.

</td></tr><tr><td>

Host Class to Capability\[sa\_host\_class\_to\_capability\]

</td><td>

Maps server type to capabilities required by Service Mapping.

</td></tr><tr><td>

Infra Path To Elements\[sa\_infra\_path\_assoc\]

</td><td>

Contains data on components which are part of a network path.

</td></tr><tr><td>

Mapping External Discovery Commands\[sa\_mapping\_ext\_commands\]

</td><td>

Contains data on customized commands created by user.

</td></tr><tr><td>

Network Paths\[sa\_network\_paths\]

</td><td>

Contains data on network paths discovered by Service Mapping.

</td></tr><tr><td>

Horizontal Discovered Paged Payloads\[sa\_paged\_payload\]

</td><td>

Service Mapping uses data in this table for splitting payload sent from the MID Server if the discovery results in a very large payload.

</td></tr><tr><td>

Discovery Patterns\[sa\_pattern\]

</td><td>

Contains preconfigured and customized patterns that Service Mapping uses for discovery.

</td></tr><tr><td>

Service Mapping Draft Pattern\[sa\_pattern\_draft\]

</td><td>

Contains non-activated discovery patterns.

</td></tr><tr><td>

Service Mapping Relation attributes\[sa\_rel\_attr\]

</td><td>

Contains relation attributes used during service discovery process.

</td></tr><tr><td>

Rel to Infra Path\[sa\_rel\_to\_infra\_path\]

</td><td>

Maps relations to network or storage paths.

</td></tr><tr><td>

Service Mapping Server Usage\[sa\_server\_usage\]

</td><td>

Contains count of servers used by Service Mapping.

</td></tr><tr><td>

File System To Storage Path\[sa\_storage\_paths\]

</td><td>

Contains data on storage paths discovered by Service Mapping.

</td></tr><tr><td>

Storage Path Connectivity Map\[sa\_storage\_path\_connectivity\_map\]

</td><td>

Maps file system to storage volume.

</td></tr><tr><td>

Traffic Based Discovery Rules\[sa\_traffic\_based\_rules\]

</td><td>

Contains data on configuration of traffic-based discovery.

</td></tr><tr><td>

Uploaded File\[sa\_uploaded\_file\]

</td><td>

Contains data on files uploaded to the MID Server and used by Service Mapping.

</td></tr><tr><td>

Configuration Item \[cmdb\_ci\]

</td><td>

Stores data on all configuration items \(CIs\) in the CMDB.

</td></tr><tr><td>

Application\[cmdb\_ci\_appl\]

</td><td>

Stores data on all configuration items \(CIs\) of application type in the CMDB.

</td></tr><tr><td>

IP Service \[cmdb\_ip\_service\]

</td><td>

Stores data for credentialless discovery support for the original table.

</td></tr><tr><td>

Application Category \[discovery\_category\_appl\]

</td><td>

Stores data on application categories used by Pattern Designer for managing pattern libraries.

</td></tr><tr><td>

Device Classification Category \[discovery\_category\_device\_class\]

</td><td>

Stores information on relationship between a device classifier and protocol used during horizontal discovery performed by Discovery.

</td></tr><tr><td>

Device Info Category \[discovery\_category\_device\_info\]

</td><td>

Stores information on device category used during horizontal discovery performed by Discovery.

</td></tr><tr><td>

Protocol Category \[discovery\_category\_protocol\]

</td><td>

Stores information on protocol category used during horizontal discovery performed by Discovery.

</td></tr><tr><td>

HTTP Classification \[discovery\_classy\_http\]

</td><td>

Stores the HTTP classification definition.

</td></tr><tr><td>

HTTP Classification Match \[discovery\_classy\_http\_match\]

</td><td>

Stores the HTTP classification conditions and the information about the pattern to launch if classification condition is matched.

</td></tr><tr><td>

Discovery Pattern Launcher \[discovery\_pattern\_launcher\]

</td><td>

Stores information about the pattern launcher mechanism.

</td></tr><tr><td>

Cloud Execution Pattern \[discovery\_ptrn\_cld\_lchr\]

</td><td>

Stores information about the pattern launcher mechanism for discovering cloud applications.

</td></tr><tr><td>

Serverless Execution Pattern \[discovery\_ptrn\_hostless\_lchr\]

</td><td>

Stores information about the pattern launcher mechanism for serverless discovery.

</td></tr><tr><td>

Discovery Pattern Parameters \[discovery\_ptrn\_lnch\_param\]

</td><td>

Stores parameters for serverless/cloud application execution.

</td></tr><tr><td>

Pattern Input Parameters \[discovery\_ptrn\_lnch\_param\_def\]

</td><td>

Stores the key parameters collected by patterns.

</td></tr><tr><td>

Applicative Credentials \[sa\_applicative\_credentials\]

</td><td>

Stores the applicative credentials.

</td></tr><tr><td>

Related CI Types \[sa\_ci\_to\_pattern\]

</td><td>

Stores related CIs within patterns.

</td></tr><tr><td>

Custom operation \[sa\_custom\_operation\]

</td><td>

Stores information on discovery pattern operations defined by users.

</td></tr><tr><td>

Custom operation parameters \[sa\_custom\_operation\_param\]

</td><td>

Stores custom operation parameters for discovery patterns.

</td></tr><tr><td>

Custom parsing strategy \[sa\_custom\_parsing\_strategy\]

</td><td>

Stores information on pattern parsing strategies that are defined by users.

</td></tr><tr><td>

Debug session \[sa\_debug\_session\]

</td><td>

Stores information collected from debug sessions.

</td></tr><tr><td>

Pattern Debugger Session Status for UI \[sa\_debug\_session\_status\]

</td><td>

Stores information on status of the debug session for the UI purposes.

</td></tr><tr><td>

Sa Deferred Service Discovery \[sa\_deferred\_service\_discovery\]

</td><td>

Contains information used for starting the top-down debug session when the relevant host is still not discovered.

</td></tr><tr><td>

Discovery log \[sa\_discovery\_log\]

</td><td>

The log of several discoveries.

</td></tr><tr><td>

Find Host Scripts \[sa\_find\_host\_scripts\]

</td><td>

Contains scripts for finding hosts in the CMDB based on the entry point information.

</td></tr><tr><td>

Host Class to Capability \[sa\_host\_class\_to\_capability\]

</td><td>

Contains information that maps the type of host to MID Server capabilities. For example, the Linux OS is mapped to the SSH WMI capability.

</td></tr><tr><td>

Mapping Discovery Commands \[sa\_mapping\_ext\_commands\]

</td><td>

Contains customizable operations for the Pattern Designer.

</td></tr><tr><td>

Horizontal Discovered Paged Payloads \[sa\_paged\_payload\]

</td><td>

Contains the IE output payload if the split mechanism is deployed.

</td></tr><tr><td>

Discovery Patterns \[sa\_pattern\]

</td><td>

Stores published patterns.

</td></tr><tr><td>

Service Mapping Draft Pattern \[sa\_pattern\_draft\]

</td><td>

Stores modified version of patterns.

</td></tr><tr><td>

Pattern Extensions \[sa\_pattern\_extension\]

</td><td>

Stores pattern extension sections.

</td></tr><tr><td>

Pattern Pre/Post Script \[sa\_pattern\_prepost\_script\]

</td><td>

Stores pre/post/pre execution scripts for patterns.

</td></tr><tr><td>

Horizontal Discovered Payloads Snapshot \[sa\_payload\_snapshot\]

</td><td>

Stores the IE output payload for the delete per main CI.

</td></tr><tr><td>

Tracked File Definition \[sa\_tracked\_file\_definition\]

</td><td>

Stores the definitions of the file tracking feature.

</td></tr><tr><td>

Uploaded File \[sa\_uploaded\_file\]

</td><td>

Stores scripts and files that are used by the pattern engine.

</td></tr></tbody>
</table>## Properties installed

<table id="table_mvw_tfb_pt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td></tr><tr><td>

sa.max\_relations\_in\_service

</td><td>

The maximum number of CI relations for a service. Exceeding the value automatically prohibits some services from displaying in the map view. Very large application services may cause performance issues. Instead of maps, users can view CI lists for large application services.-   **Type**: integer
-   **Default value**: 5000
-   **Limit**: 10000
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

best\_practice.check\_connectivity.expand\_listening\_port

</td><td>

This property controls which PIDs Service Mapping checks during the hop operation in the connectivity check. This property is true, then Service Mapping only checks connectivity on PIDs whose ports are in the **listening** state, not **connected**.-   **Type**: boolean
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.sw.mapping.reaper.checkpoints\_to\_keep

</td><td>

The maximum number of change marks maintained in the history timeline of the service. Setting the value to zero or any negative integer overrides the default setting and maintains all change marks for a three-month maximum. Using the property 'com.snc.sw.mapping.reaper.ignored\_services\_from\_optimization' allows the exclusion of specific services and returns to the removal of change marks based upon intervals.-   **Type**: integer
-   **Default value**: 1000

</td></tr><tr><td>

com.snc.sw.mapping.reaper.ignored\_services\_from\_optimization

</td><td>

This property contains the service IDs separated by commas. Instead of the number specified by the property 'com.snc.sw.mapping.reaper.checkpoints\_to\_keep' these services retain all change marks for a three-month maximum. **Type**: integer

</td></tr><tr><td>

com.snc.sw.mapping.reaper.max\_reap\_size

</td><td>

The maximum number of change marks deleted each time the system removes old and unused records from the history of changes to the service. Setting the value to zero or any negative integer overrides the limit and allows the removal of all unnecessary change marks.-   **Type**: integer
-   **Default value**: 100000

</td></tr><tr><td>

glide.service\_mapping.computation\_depth

</td><td>

This property controls the maximal depth of the service instance map.

 -   **Type**: integer
-   **Default value**: 25
-   **Other possible values**: any number higher than 1
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa\_ml.connection\_suggestions.active

</td><td>

Enable generation of the connection suggestions feature that is based on traffic-based discovery. Service Mapping generates connection suggestions using data analyzed by Predictive Intelligence. When this feature is enabled, you can [use connection suggestions to manage CI connections in application services](../task/add-remove-ci-connections-services.md).-   **Type**: boolean
-   **Default value**: true

**Note:** If traffic-based discovery was enabled in your deployment prior to Quebec and you used it to discover at least one application service, the default value is **false**.

-   **Other possible values**: false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa.debugger.max\_timeout

</td><td>

Maximum timeout \(in seconds\) since the last server activity during a Pattern Debugger run.-   **Type**: integer
-   **Default value**: 120
-   **Other possible values**: any number higher than 60
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

For more information, see [KB0854603: Pattern Debugger Session Timed Out](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0854603).

</td></tr><tr><td>

sa.discovery\_task\_timeout\_min

</td><td>

Maximum time for a Service Mapping task in minutes \(including waiting for execution in internal queues and ECC queue\).-   **Type**: string
-   **Default value**: 120
-   **Other possible values**: any number higher than 30
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa.enable\_gray\_out\_on\_resume\_discovery

</td><td>

Enable sub-tree to be grayed out after Service Mapping resumes discovery on an edge, or rerun discovery on the entire topology.-   **Type**: boolean
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa.excluded\_discovery\_sources

</td><td>

Add this property to exclude discovery sources during host detection.-   **Default value**: EventManagement
-   **Other possible values**: additional discovery sources, added after EventManagement, separated by a comma

</td></tr><tr><td>

sa.map.enable\_loops\_on\_service\_split

</td><td>

Enable you to connect a service instance to another, already existing, service instance even if the CI connection \(endpoint\) that you are connecting is part of this other service instance. This property helps to avoid loops or cycles in service maps.-   **Type**: boolean
-   **Default value**: false
-   **Other possible values**: true
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sa\_ml.connection\_suggestions.lb.routing.enabled

</td><td>

State if a target host is a load balancer member or not in the [Connection Suggestions list](connection-suggestions-list.md). -   **Type**: true/false
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: System Property \[sys\_properties\] table.

</td></tr><tr><td>

sa.network\_path\_calculation.arp\_enableadded per DOC 1074513 in Vancouver

</td><td>

Controls queries to the ARP table. Data is only calculated when the value is set to true. **Note:** For more information about querying the ARP table, see the [ARP property documentation for Service Mapping \[KB1311037\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1311037) article in the Now Support Knowledge Base.

-   **Type**: true/false
-   **Default value**: false
-   **Other possible values**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa.network\_path\_calculation.active

</td><td>

Enable network path calculation.-   **Type**: true/false
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sa.rediscovery.batch\_size

</td><td>

Number of discovery tasks executed in a single batch.-   **Type**: integer
-   **Default value**: 100
-   **Other possible values**: any number higher than 10
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sa.service\_history.max\_allowed\_bubbles

</td><td>

Number of changes that the history scale and the Changes tab display. -   **Type**: integer
-   **Default value**: 3000
-   **Other possible values**: any number higher than 3000

**Important:** Increasing the value for this property may cause performance issues with loading service instance maps.

-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sa.service.max\_ci\_service\_population

</td><td>

The maximum number of CI connections added to application services during the following operations: Converting manual services created in Event Management into application services with changes from the CMDB.-   **Type**: integer
-   **Default value**: 1000
-   **Limit**: 2000
-   **Location**: Add to System Properties \[sys\_properties\] table.

Increasing the default value may cause performance issues.


</td></tr><tr><td>

sa.storage\_path\_calculation.active

</td><td>

Enable storage path calculation. -   **Type**: true/false
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sa.topdown.mapping\_with\_acc\_mode

</td><td>

This property enables top-down discovery and service mapping using Agent Client Collector by defining the MID Server selection mode for top-down discovery. -   **Type:** integer
-   **Default value:** 0
-   **Other possible values:** 1,2

0: Top-down discovery runs using the MID Server exclusively.

1: Top-down discovery initially attempts to run using Agent Client Collector. If no agent is available, then it defaults to using the MID Server.

2: Top-down discovery runs using Agent Client Collector exclusively. If unsuccessful, the process terminates.

</td></tr><tr><td>

sa.traffic\_based\_discovery.active

</td><td>

Traffic-based discovery -   **Type**: true/false
-   **Default value**: false
-   **Other possible values**: true
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

**Note:** This property applies only to legacy traffic-based connections. If machine-learning \(ML\) connection suggestions are enabled, ensure that the property value remains set to `false`.

</td></tr><tr id="conn_aging_time"><td>

sa.traffic\_based\_discovery.conn\_aging\_time

</td><td>

Time period in hours for a Traffic Based Connection to remain active since last discovered. -   **Type**: integer
-   **Default value**: 72
-   **Other possible values**: any number higher than 24
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr id="ignored_ports"><td>

sa.traffic\_based\_discovery.ignored\_ports

</td><td>

Ports to ignore when found by traffic-based discovery. This property is available in the System Property \[sys\_properties\] table.

 Change this property to define ports that Service Mapping ignores while performing traffic-based discovery. It makes discovery more efficient since resources are not wasted on discovering irrelevant connections.

 -   **Type**: string
-   **Default value**: 445, 139, 111, 2049, 860, 3260, 135, 53
-   **Other possible values**: any relevant port numbers
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr id="max_connections"><td>

sa.traffic\_based\_discovery.max\_connections

</td><td>

Maximum number of traffic-based connections from a single CI.This property is available in the System Property \[sys\_properties\] table.

 This property helps to keep the map size reasonable by limiting the number of possible CI connections.

 -   **Type**: integer
-   **Default value**: 30
-   **Other possible values**: any number higher than 1
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sa.update\_paths\_in\_service\_model.active

</td><td>

Update network and storage paths in Service Model.-   **Type**: true/false
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

service\_watch.implied\_match.endpoint.black\_list

</td><td>

A list of endpoint types for which Service Mapping does not apply process matching logic utilized during the top-down pattern execution.-   **Type**: string
-   **Default value**: cmdb\_ci\_endpoint\_ssis\_mssql, cmdb\_ci\_endpoint\_ssas\_mssql
-   **Other possible values**: comma-separated list of endpoints
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.blacklist

</td><td>

Excludes these fields from the record in the service definition export file.-   **Type**: string
-   **Default value**: \[empty\]
-   **Other possible values**: comma-separated list of fields
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.blacklist.cmdb\_ci\_endpoint

</td><td>

Excludes these fields from the entry point record in the service definition export file.-   **Type**: string
-   **Default value**: \[empty\]
-   **Other possible values**: comma-separated list of fields
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.blacklist.cmdb\_ci\_service\_discovered

</td><td>

Excludes these fields from the application service record in the service definition export file. -   **Type**: string
-   **Default value**: discovery\_status,operational\_status,process\_status,work\_notes
-   **Other possible values**: comma-separated list of fields
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.blacklist.cmdb\_ci\_service\_group

</td><td>

Excludes these fields from the service group record in the service definition export file. Use comma to separate fields. -   **Type**: string
-   **Default value**: \[empty\]
-   **Other possible values**: comma-separated list of fields
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.max\_services\_limit

</td><td>

Defines the maximum allowed number of services to export. -   **Type**: integer
-   **Default value**: 100
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.skip\_empty\_fields

</td><td>

Excludes fields with an empty value from the record in the service definitions export file.-   **Type**: boolean
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.skip\_reference\_fields

</td><td>

Excludes reference fields from the record in the service definitions export file. -   **Type**: boolean
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.export.skip\_sys\_fields

</td><td>

Excludes fields beginning with “sys\_” from the record in the service definitions export file. -   **Type**: boolean
-   **Default value**: true
-   **Other possible values**: false
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sm.service.import.auto\_start\_discovery

</td><td>

Enable automatic discovery on all successfully imported entry points.-   **Type**: boolean
-   **Default value**: false
-   **Other possible values**: true
-   **Location**: **Service Mapping** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sn\_cloud\_migration.categories.inclusion\_list

</td><td>

A comma-separated allow list of categories for cloud migration. Only resources assigned to categories that are listed here can participate in the migration process.-   **Type**: string
-   **Default value**: Physical,VMware,HyperV,IBM HMC,OpenStack,Solaris,Nutanix,Amazon AWS,Microsoft Azure,Google Cloud,IBM Cloud
-   **Location**: **Cloud Migration** &gt; **Cloud Migration Workspace** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_cloud\_migration.server\_status.inclusion\_list

</td><td>

A comma-separated allow list of server status for cloud migration. Only servers with the listed here install status can participate in the migration process.-   **Type**: ?
-   **Default value**: 1
-   **Other possible value**: Installed=1, On Order=2, In Maintenance=3, Pending Install=4, Pending Repair=5, In Stock=6, Retired=7, Stolen=8, Absent=100
-   **Location**: **Cloud Migration** &gt; **Cloud Migration Workspace** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_cloud\_migration.os.exclusion\_list

</td><td>

A comma-separated deny list of operating systems for cloud migration. The servers whose operating system is listed here are excluded from the migration process.-   **Type**: String
-   **Default value**: ESX, Windows 2000,Windows XP.
-   **Location**: **Cloud Migration** &gt; **Cloud Migration Workspace** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_cloud\_migration.vm\_state.inclusion\_list

</td><td>

A comma-separated allow list of VM instance states for cloud migration. Only VMs with states that are listed here can participate in the migration process. -   **Type**: ??
-   **Default value**: on
-   **Other possible values**: on, off, paused, scheduled, starting, stopping, retired, terminated, error, cancelled, pausing, terminating
-   **Location**: **Cloud Migration** &gt; **Cloud Migration Workspace** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

 

</td><td>

The number of CI relations, exceeding which application service is not displayed automatically in the map view. Very large application services may cause performance issues. Instead of maps, users can view CI lists for large application services. Setting a negative value results in not limiting the number of added CI relations. Setting an invalid value, like a string, is equivalent to the default value, 5000.-   **Type**: Integer
-   **Default value**: 5000
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

svc\_by\_tags.classes.whitelist

</td><td>

This property contains the list of allowed CI classes separated by commas. Tag-based mapping includes the CIs belonging to these classes. An empty ‘value’ field indicates the inclusion of all CI classes.

</td></tr><tr><td>

svc\_by\_tags.install\_status.blacklist

</td><td>

This property contains the list of exclusions based upon the install status separated by commas. Tag-based mapping excludes any tagged CIs with the following install statuses:**Default value**: 7,100

 **Other possible values**:

 Installed=1, On order=2, In maintenance=3, Pending install=4, Pending repair=5, In stock=6, Retired=7, Stolen=8

</td></tr><tr><td>

svc\_by\_tags.max.categories.per.family

</td><td>

Set the maximum number of categories allowed per service family.-   **Type**: integer
-   **Default value**: 3

</td></tr><tr><td>

svc\_by\_tags.max.traversal.rules.active

</td><td>

Set the maximum allowed number of CI relationships that can be in the active state. Service Mapping uses only active CI relationships for tag-based discovery. -   **Type**: integer
-   **Default value**: 5
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

svc\_by\_tags.max\_ci\_limit

</td><td>

Set the maximum allowed number of CIs that a tag-based application service can contain.-   **Type**: integer
-   **Default value**: 1000
-   **Limit**: 2000
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sm.topdown.reuse\_mid\_from\_hd\_schedule

</td><td>

Use the MID Server configured during horizontal discovery for top-down discovery.-   **Type:** boolean
-   **Default value:** false
-   **Other possible values:** true
-   **Location:** **Service Mapping** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sm.network\_location.detect\_host\_by\_location

</td><td>

Select the subnetwork location to allow for the identification of the appropriate host and MID Server.**Important:** For best results, you must enable this property and sm.topdown.reuse\_mid\_from\_hd\_schedule concurrently.

-   **Type:** boolean
-   **Default value:** false
-   **Other possible values:** true
-   **Location:** **Service Mapping** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>