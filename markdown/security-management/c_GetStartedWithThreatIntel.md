---
title: Set up Threat Intelligence
description: Before you run Threat Intelligence in your instance, you must download it from the ServiceNow Store. You can also set up properties and define a threat source.Before you run Threat Intelligence in your instance, you must download it from the ServiceNow Store.Several types of components are installed with activation of the Threat Intelligence plugin, including tables and user roles.Threat Intelligence properties allow you to control how different aspects of the system function, including the setting of API keys.You can maintain a list of Threat Intelligence threat sources. Each source includes the ability to define how often a source is queried. You can also execute a threat source on demand to import the needed Structured Threat Information eXpression \(STIX\) data.You can maintain TAXII profiles for sharing STIX-formatted information. Each profile contains one or more TAXII collections or feeds.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 20
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Set up Threat Intelligence

Before you run Threat Intelligence in your instance, you must download it from the ServiceNow Store. You can also set up properties and define a threat source.

## Install Threat Intelligence

Before you run Threat Intelligence in your instance, you must download it from the ServiceNow Store.

### Before you begin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration.

<table id="table_sir_install_dependencies"><thead><tr><th>

Setup tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have the required ServiceNow roles for your instance.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   If not already assigned, the System Administrator \[admin\] installs the application and assigns the Threat Admin \[sn\_ti.admin\] role.
-   The Threat Admin \[sn\_ti.admin\] oversees configuration and verifies expected results.

</td></tr></tbody>
</table>Role required: admin

### Procedure

1.  Follow the instructions for [downloading an application from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).


### What to do next

[Set Threat Intelligence properties](c_GetStartedWithThreatIntel.md#).

### Components installed with Threat Intelligence

Several types of components are installed with activation of the Threat Intelligence plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

#### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Threat Administrator\[sn\_ti.admin\]

</td><td>

Has full control over all threat properties, SLAs, and notifications.

</td><td>

sn\_ti.write

</td></tr><tr><td>

Threat Reader\[sn\_ti.read\]

</td><td>

Has read access to threat information.

</td><td>

sn.sec\_cmn.int\_read

</td></tr><tr><td>

Threat Writer\[sn\_ti.write\]

</td><td>

Has write access to threat information.Cannot delete attack modes, indicators nor observables. Only a Threat Administrator can delete them.

</td><td>

-   sn\_sec\_cmn.int\_write
-   sn\_ti.read

</td></tr><tr><td>

MITRE Analyst

 \[sn\_ti.mitre\_analyst\]

</td><td>

This role enables read access to the MITRE-ATT&amp;CK modules in Threat Intelligence and to the SIR module.

</td><td>

-   sn\_ti.read
-   sn\_si.read

</td></tr></tbody>
</table>#### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attack mechanism\[sn\_ti\_attack\_mechanism\]

</td><td>

Organizes attack patterns hierarchically based on mechanisms that are frequently employed when exploiting a vulnerability. The categories that are members of this view represent the different techniques used to attack a system.

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Attack mode/method\[sn\_ti\_attack\_mode\]

</td><td>

Attack modes and methods are representations of the behavior of cyber adversaries. They characterize what an adversary does and how they do it in increasing levels of detail.

</td></tr><tr><td>

Discovery method\[sn\_ti\_discovery\_method\]

</td><td>

An expression of how an incident was discovered.

</td></tr><tr><td>

Feed\[sn\_ti\_feed\]

</td><td>

Used for configuring the Threat Feed \(RSS\) in the Threat Overview.

</td></tr><tr><td>

Indicator Attack mode/method\[sn\_ti\_m2m\_indicator\_attack\_mode\]

</td><td>

Used to map attack modes/methods to indicators.

</td></tr><tr><td>

Indicator of Compromise\[sn\_ti\_indicator\]

</td><td>

Used to convey specific observable patterns combined with contextual information intended to represent artifacts and/or behaviors of interest within a cyber security context.

</td></tr><tr><td>

Indicator of Compromise Metadata\[sn\_ti\_indicator\_metadata\]

</td><td>

Used to populate TAXII records.

</td></tr><tr><td>

Indicator Source\[sn\_ti\_m2m\_indicator\_source\]

</td><td>

Used to collect all the sources reporting the specific indicator.

</td></tr><tr><td>

Indicator Type\[sn\_ti\_indicator\_type\]

</td><td>

Characterizes a cyberthreat indicator made up of a pattern identifying certain observable conditions as well as contextual information about the patterns meaning, how and when it is acted on, and so on.

</td></tr><tr><td>

Associated Indicator Type\[sn\_ti\_m2m\_indicator\_indicator\_type\]

</td><td>

Links indicators with their applicable types

</td></tr><tr><td>

Incident count \[sn\_ti\_observable\]

</td><td>

Number of security incidents associated with an observable.

</td></tr><tr><td>

Intended effect\[sn\_ti\_intended\_effect\]

</td><td>

Used for expressing the intended effect of a threat actor.

</td></tr><tr><td>

IP Scan Result\[sn\_ti\_ip\_result\]

</td><td>

Used to show the results of an IP lookup.

</td></tr><tr id="row_rate-limit"><td>

Malware Rate limit\[sn\_ti\_rate\_limit\]

</td><td>

Defines a rate limit to be used on a lookup source.

</td></tr><tr id="row_scan"><td>

Malware Scan\[sn\_ti\_scan\]

</td><td>

A lookup. Contains what to look up, with what look up source, and a summary of the lookup results.

</td></tr><tr id="row_scan-queue"><td>

Malware Scan Queue Entry\[sn\_ti\_scan\_q\_entry\]

</td><td>

A lookup record queued for lookup or processing. Facilitates the requests within stated rate limits.

</td></tr><tr><td>

Malware Scan Result\[sn\_ti\_scan\_result\]

</td><td>

Displays the result of a lookup.

</td></tr><tr><td>

Malware Scanner\[sn\_ti\_scanner\]

</td><td>

Defines third-party lookup sources to use in performing lookups.

</td></tr><tr><td>

Malware Scanner Rate Limit\[sn\_ti\_scanner\_rate\_limit\]

</td><td>

Associates a lookup source with a rate limit.

</td></tr><tr><td>

Malware Type\[sn\_ti\_malware\_type\]

</td><td>

Used for expressing the types of malware instances.

</td></tr><tr><td>

Observable\[sn\_ti\_observable\]

</td><td>

Observables in STIX represent stateful properties or measurable events pertinent to the operation of computers and networks.

</td></tr><tr><td>

Observable Context Type\[sn\_ti\_observable\_context\_type\]

</td><td>

Stores the context \(source, destination of an IP address, and so forth\) for an observable.

</td></tr><tr><td>

Observable Indicator\[sn\_ti\_m2m\_observable\_indicator\]

</td><td>

Used to relate observables to indicators.

</td></tr><tr><td>

Observable Source\[sn\_ti\_observable\_source\]

</td><td>

Used to relate observables to threat sources.

</td></tr><tr><td>

Observable Type\[sn\_ti\_observable\_type\]

</td><td>

Lists the various types of observables, such as IP addresses.

</td></tr><tr><td>

Observable Type Category\[sn\_ti\_observable\_type\_category\]

</td><td>

Stores the first categorization of observables \(for example, IP addresses and URLs\). It is used for more accurately determining observable types.

</td></tr><tr><td>

Related attack mode/method\[sn\_ti\_m2m\_attack\_mode\_attack\_mode\]

</td><td>

Used to relate attack modes to each other.

</td></tr><tr><td>

Related Observables\[sn\_ti\_m2m\_observables\]

</td><td>

Used to relate observables to each other.

</td></tr><tr><td>

Scan type\[sn\_ti\_scan\_type\]

</td><td>

The definition of a lookup type, with initial records for File, URL, and IP.

</td></tr><tr><td>

Security Case\[sn\_ti\_case\]

</td><td>

Stores security case records created using Case Management.

</td></tr><tr><td>

Security Case IoC\[sn\_ti\_case\_ioc\]

</td><td>

Used to manage the relationship between observables and cases.

</td></tr><tr><td>

Security Case Related Task\[sn\_ti\_m2m\_case\_task\]

</td><td>

Used to manage the relationship between tasks \(security incidents, change requests, and so forth\) with security cases.

</td></tr><tr><td>

Security Case Relationship Exclusion\[sn\_ti\_case\_relationship\_exclusion\]

</td><td>

Provides the definition of inclusion and exclusion of related records in security cases.

</td></tr><tr><td>

Sighting\[sn\_ti\_sighting\]

</td><td>

The m2m link between the observable and the Sightings Search detail result used in the execution of a Sighting Search request.

</td></tr><tr><td>

Sighting Configuration Items\[sn\_ti\_m2m\_sighting\_ci\]

</td><td>

Maps configuration items to a Sightings Search.

</td></tr><tr><td>

Sighting Search Detail\[sn\_ti\_sighting\_search\_detail\]

</td><td>

Details of a Sighting Search for example the number of internal external items found.

</td></tr><tr><td>

Sighting Search Result\[sn\_ti\_sighting\_search\]

</td><td>

The header for a Sightings Search execution.

</td></tr><tr><td>

Supported Observable Types\[sn\_ti\_m2m\_ind\_type\_obs\_type\]

</td><td>

Relates indicator types to valid observable types.

</td></tr><tr><td>

Supported Scan Type\[sn\_ti\_supported\_scan\_type\]

</td><td>

Maps the lookup type to a lookup source/vendor-specific implementation. Indicates that a specific lookup source supports the type.

</td></tr><tr><td>

Task Attack mode/method\[sn\_ti\_m2m\_task\_attack\_mode\]

</td><td>

Relates attack modes to tasks.

</td></tr><tr><td>

Task Indicator\[sn\_ti\_m2m\_task\_indicator\]

</td><td>

Relates indicators to tasks.

</td></tr><tr><td>

Task Observable\[sn\_ti\_m2m\_task\_observable\]

</td><td>

Relates observables to tasks.

</td></tr><tr><td>

Task Sighting\[sn\_ti\_m2m\_task\_sighting\]

</td><td>

Stores task records \(security incidents and cases\) related to a sighting record.

</td></tr><tr><td>

TAXII Collection\[sn\_ti\_taxii\_collection\]

</td><td>

Defines a cyber-risk intelligence feed that can be imported by a TAXII server.

</td></tr><tr><td>

TAXII Profile\[sn\_ti\_taxii\_profile\]

</td><td>

Defines a repository for sharing cyber-risk intelligence. Contains TAXII collections.

</td></tr><tr><td>

Threat Actor type\[sn\_ti\_threat\_actor\_type\]

</td><td>

Provides characterizations of malicious actors \(or adversaries\) representing a cyber attack threat, including presumed intent and historically observed behavior.

</td></tr><tr><td>

Threat Intelligence Source\[sn\_ti\_source\]

</td><td>

Defines a source for importing threat data.

</td></tr><tr><td>

Associated Attack Motivation \[sn\_ti\_stix2\_m2m\_object\_attack\_motivation\]

</td><td>

Collects all attack motivations associated with a STIX Object.

</td></tr><tr><td>

Associated Infrastructure Type \[sn\_ti\_stix2\_m2m\_infra\_type\]

</td><td>

Links infrastructure with their types.

</td></tr><tr><td>

Associated Kill Chain Phase\[sn\_ti\_stix2\_m2m\_indicator\_kill\_chain\_phase\]

</td><td>

Links kill chain phases to indicators.

</td></tr><tr><td>

Associated Kill Chain Phase\[sn\_ti\_stix2\_m2m\_object\_kill\_chain\_phase\]

</td><td>

Links kill chain phases to STIX objects.

</td></tr><tr><td>

Associated Malware Capability\[sn\_ti\_stix2\_m2m\_malware\_capability\]

</td><td>

Links malware with their capabilities.

</td></tr><tr><td>

Associated Malware Type\[sn\_ti\_stix2\_m2m\_malware\_malware\_type\]

</td><td>

Links malware with their types.

</td></tr><tr><td>

Associated Observable\[sn\_ti\_stix2\_m2m\_malware\_observable\]

</td><td>

Collects all observables associated with a malware.

</td></tr><tr><td>

Associated Observable\[sn\_ti\_stix2\_m2m\_observed\_data\_observable\]

</td><td>

Collects all observables associated with an observed data.

</td></tr><tr><td>

Associated Report Type\[sn\_ti\_stix2\_m2m\_report\_report\_type\]

</td><td>

Links threat reports with their types.

</td></tr><tr><td>

Associated Threat Actor Role\[sn\_ti\_stix2\_m2m\_threat\_actor\_threat\_actor\_role\]

</td><td>

Links threat actors with their roles.

</td></tr><tr><td>

Associated Threat Actor Type\[sn\_ti\_stix2\_m2m\_threat\_actor\_threat\_actor\_type\]

</td><td>

Links threat actors with their types.

</td></tr><tr><td>

Associated Tool Type\[sn\_ti\_stix2\_m2m\_tool\_tool\_type\]

</td><td>

Links tools with their types.

</td></tr><tr><td>

Attack Motivation\[sn\_ti\_stix2\_attack\_motivation\]

</td><td>

Attack Motivation shapes the intensity and the persistence of an attack. Threat Actors and Intrusion Sets usually act in a manner that reflects their underlying emotion or situation, and this informs defenders of the manner of attack.

</td></tr><tr><td>

Attack Pattern\[sn\_ti\_stix2\_attack\_pattern\]

</td><td>

A TTP type that describes methods that adversaries use to attempt to compromise targets.

</td></tr><tr><td>

Campaign\[sn\_ti\_stix2\_campaign\]

</td><td>

A grouping of adversarial behaviors that describe a set of malicious activities or attacks \(sometimes named as waves\) that occur over a period against a specific set of targets.

</td></tr><tr><td>

Course of Action\[sn\_ti\_stix2\_course\_of\_action\]

</td><td>

A recommendation from a producer of intelligence to a consumer on the actions that they might take in response to intelligence.

</td></tr><tr><td>

External Reference\[sn\_ti\_stix2\_external\_reference\]

</td><td>

Pointers to information represented outside of STIX.

</td></tr><tr><td>

Identity Sighting\[sn\_ti\_stix2\_m2m\_sighting\_identity\]

</td><td>

Collects all Identities associated with a Sighting.

</td></tr><tr><td>

Identity\[sn\_ti\_stix2\_identity\]

</td><td>

Actual individuals, organizations, or groups \(example ACME, Inc.\) as well as classes of individuals, organizations, systems, or groups \(example the finance sector\).

</td></tr><tr><td>

Indicator External Reference\[sn\_ti\_stix2\_indicator\_external\_reference\]

</td><td>

Represents external references associated with indicators.

</td></tr><tr><td>

Indicator Sighting\[sn\_ti\_stix2\_indicator\_sighting\]

</td><td>

Represents sightings of indicators.

</td></tr><tr><td>

Infrastructure Type\[sn\_ti\_stix2\_infrastructure\_type\]

</td><td>

Represents the various infrastructure types.

</td></tr><tr><td>

Infrastructure\[sn\_ti\_stix2\_infrastructure\]

</td><td>

A TTP type that describes any systems, software services, and any associated physical or virtual resources, intended to support some purpose \(example C2 servers used as part of an attack, device, or server that are part of defense, database servers targeted by an attack, and the like\).

</td></tr><tr><td>

Installed software\[sn\_ti\_stix2\_m2m\_malware\_analysis\_sw\]

</td><td>

Collects all software \(SCO software types\) associated with a malware analysis.

</td></tr><tr><td>

Intrusion Set\[sn\_ti\_stix2\_intrusion\_set\]

</td><td>

A grouped set of adversarial behaviors and resources with common properties that is believed to be orchestrated by a single organization.

</td></tr><tr><td>

Kill Chain Phase\[sn\_ti\_stix2\_kill\_chain\_phase\]

</td><td>

Represents kill chain phases associated with a kill chain.

</td></tr><tr><td>

Kill Chain\[sn\_ti\_stix2\_kill\_chain\]

</td><td>

Represents various kill chains.

</td></tr><tr><td>

Location\[sn\_ti\_stix2\_location\]

</td><td>

Represents a geographic location provided through STIX.

</td></tr><tr><td>

Malware Analysis\[sn\_ti\_stix2\_malware\_analysis\]

</td><td>

The metadata and results of a particular static or dynamic analysis performed on a malware instance or family.

</td></tr><tr><td>

Malware Capability\[sn\_ti\_stix2\_malware\_capability\]

</td><td>

Represents common capabilities that a malware family or instance exhibits.

</td></tr><tr><td>

Malware Operating System\[sn\_ti\_stix2\_m2m\_malware\_operating\_system\]

</td><td>

Collects all Operating Systems \(SCO software types\) associated with malware.

</td></tr><tr><td>

Malware\[sn\_ti\_stix2\_malware\]

</td><td>

A TTP type that represents malicious code.

</td></tr><tr><td>

Marking Definition\[sn\_ti\_stix2\_marking\_definition\]

</td><td>

Represents handling or sharing requirements for STIX Objects.

</td></tr><tr><td>

Object Sighting\[sn\_ti\_stix2\_object\_sighting\]

</td><td>

Represents sightings of STIX Objects.

</td></tr><tr><td>

Object-Indicator Relationship\[sn\_ti\_stix2\_m2m\_object\_indicator\]

</td><td>

Collects all relationships between STIX objects and STIX indicators.

</td></tr><tr><td>

Object-Object Relationship\[sn\_ti\_stix2\_m2m\_object\]

</td><td>

Collects all relationships between STIX Objects and other STIX objects excluding the indicators.

</td></tr><tr><td>

Object-Observable Relationship\[sn\_ti\_stix2\_m2m\_object\_observable\]

</td><td>

Collects all relationships between STIX observables and STIX objects.

</td></tr><tr><td>

Observed Data Sighting\[sn\_ti\_stix2\_m2m\_sighting\_observed\_data\]

</td><td>

Collects all the observed data objects associated to a sighting.

</td></tr><tr><td>

Observed Data\[sn\_ti\_stix2\_observed\_data\]

</td><td>

Conveys information about cyber security-related entities such as files, systems, and networks using the STIX Cyber-Observable Objects \(SCOs\).

</td></tr><tr><td>

Report Type\[sn\_ti\_stix2\_report\_type\]

</td><td>

Represents primary purpose or subject of Threat Reports.

</td></tr><tr><td>

Reported Observable\[sn\_ti\_stix2\_m2m\_malware\_analysis\_observable\]

</td><td>

Collects all observables associated to Malware Analysis.

</td></tr><tr><td>

STIX V2 Object\[sn\_ti\_stix2\_object\]

</td><td>

Common parent table for STIX Object.

</td></tr><tr><td>

STIX V2 Sighting\[sn\_ti\_stix2\_sighting\]

</td><td>

Common parent table for STIX sighting tables.

</td></tr><tr><td>

Threat Actor Role\[sn\_ti\_stix2\_threat\_actor\_role\]

</td><td>

Represents roles that can be played by threat actors.

</td></tr><tr><td>

Threat Actor\[sn\_ti\_stix2\_threat\_actor\]

</td><td>

Threat Actors are actual individuals, groups, or organizations believed to be operating with malicious intent.

</td></tr><tr><td>

Threat Grouping\[sn\_ti\_stix2\_threat\_grouping\]

</td><td>

Groups all the STIX Objects that share some common context.

</td></tr><tr><td>

Threat Note\[sn\_ti\_stix2\_threat\_note\]

</td><td>

Provides context and additional analysis not contained in the corresponding STIX Object.

</td></tr><tr><td>

Threat Opinion\[sn\_ti\_stix2\_threat\_opinion\]

</td><td>

Provides assessment of accuracy of information in a STIX object produced by a different entity.

</td></tr><tr><td>

Threat Report\[sn\_ti\_stix2\_threat\_report\]

</td><td>

Reports are collections of threat intelligence focused on one or more topics, such as a description of a threat actor, malware, or attack technique, including context and related details. They are used to group-related threat intelligence together to publish as a comprehensive cyber threat story.

</td></tr><tr><td>

Tool Type\[sn\_ti\_stix2\_tool\_type\]

</td><td>

The categories of tools that can be used to perform attacks.

</td></tr><tr><td>

Tool\[sn\_ti\_stix2\_tool\]

</td><td>

Tools are legitimate software that is used by threat actors to perform attacks.

</td></tr><tr><td>

Vulnerability\[sn\_ti\_stix2\_vulnerability\]

</td><td>

Represents weakness or defect in the requirements, designs, or implementations of the computational logic \(example code\) found in software and some hardware components \(example firmware\). They can be directly exploited to negatively impact the confidentiality, integrity, or availability of that system.

</td></tr></tbody>
</table>## Set Threat Intelligence properties

Threat Intelligence properties allow you to control how different aspects of the system function, including the setting of API keys.

### Before you begin

Role required: sn\_ti.admin

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Administration** &gt; **Properties**.

2.  Set the following properties, as needed.

<table id="table_jrc_rhf_zt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

The domain name to retrieve additional information for IP addresses/URLssn\_ti.ip\_lookup.web\_site

</td><td>

The domain name to use for retrieving additional information into your IoC database. This property is used by the `ThreatAdditionalInfo` script include to populate additional information on the Observables form.

 Default value: http://api.ipinfodb.com/v3/ip-country/

 **Note:** The pinfodb.com third-party API is available at no extra charge and used in many commercial software programs. If you replace it with a different domain name, you must also provide the API key in the next field.

</td></tr><tr><td>

The API key to be used for the domain, if anysn\_ti.ip\_lookup.api\_key

</td><td>

The API key to use for retrieving additional information into your IoC database. This property is used \(along with the sn\_ti.ip\_lookup.web\_site property\) by the `ThreatAdditionalInfo` script include to populate additional information on the Observables form.

</td></tr><tr><td>

Do not run automated threat lookup on an observable when the observable is associated with an IoC or found to be malicious. sn\_ti.scan\_ioc\_before\_sending

 **Note:** You need to define the duration in the next property \(sn\_ti.scan\_ioc\_num\_days\).

</td><td>

Option to stop running the automated threat lookup on an observable when the observable is found to be malicious or associated with an IoC for the configured duration \(in days\). If you still need to run the threat look up for the observable, you can do it manually.

 Default value: Yes

</td></tr><tr><td>

Duration \(in days\)sn\_ti.scan\_ioc\_num\_days

</td><td>

Option to define the duration until which the automated threat lookup of the observable is skipped.

 Default value \(in days\): 30

</td></tr><tr><td>

Do not run automated threat lookup on an observable if already run. sn\_ti.enable\_threat\_lookup\_bypass

 **Note:** You need to define the duration in the next property \(sn\_ti.threat\_lookup\_bypass\_times\).

</td><td>

If there is a threat lookup result for an observable already available, then you have an option to skip the rerun of the automated threat lookup for the same observable until the configured duration has passed.

 Default value: No

**Note:** If you're enabling this property, make sure that you are adding an appropriate value.

</td></tr><tr><td>

Duration \(in minutes\)sn\_ti.threat\_lookup\_bypass\_time

</td><td>

Option to define the duration after which the automated threat lookup of the observable can be rerun.

 Default value \(in minutes\): 0

</td></tr><tr><td>

Set a validity duration for user overrides on observable finding. sn\_ti.enable\_observable\_finding\_system\_override

 **Note:** You need to define the validity in the next property \(sn\_ti.observable\_finding\_override\_expiry\).

</td><td>

Option to set a validity duration for user overrides on the observable findings. Threat lookup finding of the observable will not be changed by the base system during this validity duration.Default value: No.

**Note:** If you're enabling this property, make sure that you are adding an appropriate value.

</td></tr><tr><td>

Validity \(in minutes\)sn\_ti.observable\_finding\_override\_expiry

</td><td>

Option to define the validity period of the observable finding.Default value \(in minutes\): none

</td></tr><tr><td>

When an attack mode/method has not been received from any source for the specified number of days, mark it as inactivesn\_ti.attack\_mode\_inactivate\_days

</td><td>

Number of days from when an attack mode/method was last received for the record to be marked inactive.

 Default value: 360

 **Note:** The **Active** check box is not visible on the **Attack mode/method** form by default. However, you can add it. When attack modes/methods are inactive, they cannot be selected on other forms.

</td></tr><tr><td>

When an indicator has not been received from any source for the specified number of days, mark it as inactivesn\_ti.indicator\_inactivate\_days

</td><td>

Number of days from when an indicator was last received for the record to be marked inactive.

 Default value: 180

 **Note:** The **Active** check box is not visible on the **Indicator** form by default. However, you can add it. When indicators are inactive, they cannot be selected on other forms.

</td></tr><tr><td>

The maximum payload size \(in MB\) for a STIX attachment that can be parsed.sn\_ti.stix.max\_payload\_size

</td><td>

Specifies the maximum payload size for the STIX attachment that you can parse.

 Default value: none

 Maximum allowed value: No limit.

</td></tr><tr><td>

Maximum time in seconds an outbound HTTP connection waits to fetch TAXII collection datasn\_ti.taxii.http.max\_timeout

</td><td>

Specifies the maximum amount of time an outbound HTTP connection waits before fetching the next packet of TAXII collection data.

 Default value: 300

</td></tr><tr><td>

Maximum number of objects retrieved in one REST call from a TAXII server \(Applicable only for TAXII versions 2.0 and 2.1\)sn\_ti.taxii.max\_page\_size

</td><td>

Specifies the maximum number of objects retrieved in one REST call from the TAXII server for one page.

 Default value: 5000

 Maximum allowed value: 50000

</td></tr><tr><td>

Maximum number of retries for a failed TAXII 2.X REST callsn\_ti.taxii2.retry\_count

</td><td>

Specifies the maximum number of retries for a failed TAXII REST call.

 Default value: 3

</td></tr></tbody>
</table>3.  Click **Save**.


## Define a threat source

You can maintain a list of Threat Intelligence threat sources. Each source includes the ability to define how often a source is queried. You can also execute a threat source on demand to import the needed Structured Threat Information eXpression \(STIX\) data.

### Before you begin

Role required: sn\_ti.admin

### About this task

Threat Intelligence employs two technologies for importing threat-related information: STIX and Trusted Automated Exchange of Indicator Information \(TAXII\).

STIX provides a standardized, structured language for representing an extensive set of cyberthreat information that includes indicators of compromise \(IoC\) activity \(for example, IP addresses and file hashes\), as well as contextual information regarding threats, such as attack modes/methods, that together more completely characterize the motivations, capabilities, and activities of a cyber adversary. As such, STIX data provides valuable information on how your organization can best to defend against cyberthreats.

Trusted Automated Exchange of Indicator Information \(TAXII\) is used to facilitate automated exchange of cyberthreat information. TAXII defines a set of services and message exchanges that enable sharing of actionable cyberthreat information across organization and product/service boundaries for the detection, prevention, and mitigation of cyberthreats. TAXII profiles can be set up as repositories for sharing STIX-formatted information. Each profile contains one or more TAXII collections or feeds.

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Sources** &gt; **Threat Sources**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the threat source.|
    |Application|The application that contains this record.|
    |Active|Select this check box to activate the threat source.|
    |Advanced|Select this check box to display the scripts in the **Integration factory script** and **Report processor** fields.|
    |Description|A description of this threat source.|

4.  Fill in the fields in the **Schedule** section, as appropriate.

<table id="table_mxf_tmz_w5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

The frequency you want the integration to run, Daily, Weekly, Periodically, and so on. As noted, subsequent fields are displayed based on the setting of this field.

</td></tr><tr><td>

Day

</td><td>

The day you want the integration to run.-   If you selected **Weekly** in the **Run** field, this field displays the days of the week.
-   If you selected **Monthly** in the **Run** field, this field displays the days of the month.


</td></tr><tr><td>

Time

</td><td>

The time you want the integration to start.

</td></tr><tr><td>

Repeat Interval

</td><td>

If you selected **Periodically** in the **Run** field, this field displays the number of days, and hours before the integration runs again.

</td></tr><tr><td>

Starting

</td><td>

If you selected **Periodically** in the **Run** field, this field displays the dates, and time to be used as the starting point for periodic updates.

</td></tr><tr><td>

Conditional

</td><td>

Select this field if you want to add conditional parameters.

</td></tr><tr><td>

Condition

</td><td>

If you selected the **Conditional** check box, enter the conditions here.

</td></tr></tbody>
</table>5.  Fill in the fields in the **Threat Details** section, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Indicator|The indicator to use when the data doesn’t explicitly provide one. For blocklists, if empty, a new indicator is created for each observable.|
    |Indicator type|The indicator type to use for indicators that are created and the data doesn’t explicitly provide an indicator type.|
    |Attack Mode/Method|The attack mode/method to use when the data doesn’t explicitly provide one.|
    |Observable Type|The observable type to use for observables that are created and the data doesn’t explicitly provide an observable type.\[SI1\]|
    |Weight|Enter a weight value for this source to be used in the confidence calculation.|

    **Note:** The usage of the **Indicator**, **Indicator Type**, **Attack Mode/Method**, and **Observable Type** fields are implementation-specific. The default processor, SimpleBlocklistProcessor, behaves as the tooltips describe. However, a TAXII threat source is fully data driven. Any custom threat source processor would be able to use its own strategy. These fields are basically items to expose to the integration/processor and the implementation decides how to use them.

6.  Fill in the fields in the **Source Details** section, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Endpoint|Enter the web service endpoint URL where the threat source is accessed by Threat Intelligence. Click the lock icon to lock the URL.|
    |Use REST Message|If you need a REST message to access the threat source, select this check box. The **REST message** and **REST method** fields become required.|
    |REST message|Click the lookup icon, and select the REST message from the list or click **New** to [define a new REST message](https://www.servicenow.com/docs/access?context=t_ConfiguringARESTMessage&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).|
    |REST method|Click the lookup icon, and select the REST method from the list or click **New** to define a new REST method.|
    |Integration script|The default integration script is **SimpleRESTSecurityDataIntegration**. It runs a simple REST call, saves the response as an attachment, and then returns the attachment to the processor. This script meets the needs of most organizations. But if you want, you can click the lookup icon, and select a different integration script or define a new one.|
    |Integration factory script|If the **Advanced** check box is selected, this field displays the actual script for constructing the integration script. You can edit the script as needed. This ability is useful for custom implementations. Integrations in the base system usually don’t need any custom constructor logic.|
    |Report processor|The default integration script is **SimpleBlocklistProcessor**. This script is a simple processor that accepts a simple blocklist \(simple, meaning a single column document with observables such as URLs or IP addresses\) and creates observables. It uses the various **Threat Details** fields to determine which fields to set when observables are created.|
    |Processor factory script|If the **Advanced** check box is selected, this field displays the actual script for constructing the processor. You can edit the script as needed. This script is generally useful for custom implementations. The integrations in the base system usually don’t need custom constructor logic.|

7.  Click **Submit**.

    **Note:** For more information on how to configure the threat source's pagination, see [KB1213825](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1213825) article.


## Create a TAXII profile

You can maintain TAXII profiles for sharing STIX-formatted information. Each profile contains one or more TAXII collections or feeds.

### Before you begin

Role required: sn\_ti.admin

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Sources** &gt; **TAXII Profiles**.

2.  Click **New**.

3.  Complete the following fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of the TAXII profile|
    |**Application**|The application that contains this record.|
    |**Use REST messages as template**|If you require a REST message to access the TAXII profile, select this check box.|
    |**TAXII Version**|Specify the TAXII version. The supported STIX versions are 1.1, 2.0, and 2.1.|
    |**Description**|A description of this TAXII profile.|

4.  Fill in the fields in the **Discovery Service Configuration** section, as appropriate.

    |Field|Description|
    |-----|-----------|
    |**Discovery Service endpoint**|Discovery Endpoint authorizes clients to obtain information about a TAXII Server and get a list of API Roots.|
    |**Use REST message**|Select this option if you require a REST message to access the TAXII profile. The **Discovery Service REST message** and **Discovery Service REST method** fields become required.|
    |**Discovery Service REST message**|Click the lookup icon, and select the REST message from the list or click **New** to define a new REST message.|
    |**Discovery Service REST method**|Click the lookup icon, and select the REST message from the list or click **New** to define a new REST method.|

5.  Fill in the fields in the **Collection Service Configuration** section, as appropriate.

<table id="choicetable_fn4_l4l_wmb"><thead><tr><th align="left" id="d70005e2662">

Field

</th><th align="left" id="d70005e2665">

Description

</th></tr></thead><tbody><tr><td id="d70005e2671">

**Collection Info Service endpoint**

</td><td>

A TAXII Collection is an interface to a logical repository of CTI objects provided by a TAXII Server and is used by TAXII Clients to send information to the TAXII Server or request information from the TAXII Server. A TAXII Server can host multiple Collections per API Root, and Collections are used to exchange information in a request–response manner.

</td></tr><tr><td id="d70005e2683">

**Use REST message**

</td><td>

Select this option if you require a REST message to access the TAXII profile. The **Collection Info Service REST message** and **Collection Info Service REST method** fields become required.

</td></tr><tr><td id="d70005e2698">

**Collection Info Service REST message**

</td><td>

Click the lookup icon, and select the REST message from the list or click **New** to define a new REST message.

</td></tr><tr><td id="d70005e2710">

**Collection Info Service REST method**

</td><td>

Click the lookup icon, and select the REST message from the list or click **New** to define a new REST method.

</td></tr></tbody>
</table>6.  Click **Submit**.


