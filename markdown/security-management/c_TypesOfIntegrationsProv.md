---
title: Types of ServiceNow integrations provided
description: The Security Operations applications \(Security Incident Response, Threat Intelligence, and Vulnerability Response\) can be seamlessly integrated with other ServiceNow applications to enhance their functionality.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Types of ServiceNow integrations provided

The Security Operations applications \(Security Incident Response, Threat Intelligence, and Vulnerability Response\) can be seamlessly integrated with other ServiceNow applications to enhance their functionality.

The following integrations are provided in the Security Operations base system.

## Security Incident Response – Event Management integration

The capabilities of the Event Management application have been expanded to support Security Incident Response. The Security Incident Response Event Management support plugin automatically parses the contents of events in Event Management to populate fields in security incidents.

Use case covered:

Creation of security events in the Event Management system from Security Information and Event Management \(SIEM\) tools

Useful capabilities provided:

-   Event management functionality – event correlation, event rules, and alert rules
-   Automatic mapping of additional\_information values to resulting security incident

Resources:

[Security Incident event management support documentation](../../security-incident-response/concept/c_ScIncdUseAlrts.md)

[Event Management documentation](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)

## Security Incident Response - Import Set API integration

In addition to using Event Management to push security-related events, the Security Incident Response application provides an Import Set API that allows direct creation of security incidents. The REST endpoint for the Security Incident Import Set is http://localhost:8080/api/now/import/sn\_si\_incident\_import.

This integration technique is useful when a\) Event Management is not installed, or b\) it is desired to simply create Security Incidents without going through the event &gt; alert &gt; Security Incident flow that is required when using Event Management.

Use case covered:

Creation of security incidents directly from SIEM tools.

Useful capabilities provided:

Automatic CI matching on Security Incident creation based on IP, NetBIOS, or fully qualified domain name.

Resources:

[Platform Import Set API documentation](https://www.servicenow.com/docs/access?context=c_ImportSetAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Security Incident Web Service Import Set documentation](../../security-incident-response/concept/c_3rdPartyAlertMonToolInteg.md)

## Threat Intelligence - lookup source integration

Lookup sources provide the ability to send data to external lookup sources to determine if that data is malicious. Generally, that data is an IP address, URL, file, or file hash.

Use case covered:

Lookup an IP address, URL, file, or hash with an external lookup service.

Useful capabilities provided:

-   Consistent way to request lookups from catalog items and security incidents.
-   Rate limiting and throttling capabilities provided with little/no coding.
-   Automatic creation of Indicators of Compromise \(IoC\) observable entries for any issues found by lookup sources.

## Threat Intelligence - threat source integration

Threat Sources provide the ability to pull in data from external threat intelligence repositories. This data is then imported into the various Indicators of Compromise tables that exist within the system. TAXII collections and simple blocklists are supported natively. To add new TAXII collections \(or profiles based on a discovery or collection management service\), it is as simple as adding an entry. Similarly, adding a new simple, single column blocklist is a matter of entering a new record and providing the URL of the blocklist. For more complicated sets of data, a custom integration can be provided to make a call to a URL and parse the response.

Use case covered:

Retrieve data from a threat intelligence source to load into IoC tables.

Useful capabilities provided:

-   Support for simple blocklists and TAXII collections with no coding.
-   Simple mechanism for executing REST messages for retrieving data.
-   Decoupled data retrieval/processing for integration component reusability.
-   Native support for processing passing data returned to data sources \(and import sets/transform maps\).
-   Supports multiple data requests per integration \(for paginated calls\) with the ability to pass context to subsequent calls

Resources:

[Define a threat source](../../threat-intelligence/concept/c_GetStartedWithThreatIntel.md#)

## Vulnerability Response - scanner invocation integration

Vulnerability Scanner Invocation is a lightweight integration entry point that supports invoking vulnerability scans from the instance. A third-party vulnerability scanner is called asynchronously to schedule a scan for configuration items or IP addresses.

Use case covered:

Make request to third-party scanner to scan a CI \(using host information derived from CI\) or IP address/IP addresses.

Useful capabilities provided:

-   Simple framework for defining scanner implementations.
-   Consistent way to request scans from catalog items, security incidents, and vulnerable items.
-   Automatic updating of tasks with result of scan invocation.

## Vulnerability Response - data integration

Vulnerability data integrations are intended to retrieve vulnerability data from third-party vulnerability systems. The expected outputs from these integrations are vulnerability entries and vulnerable items. This integration allows third-party vulnerability scanners to function independently, with the expectation that vulnerabilities can be worked and tracked within the instance.

Use cases covered:

-   Retrieve vulnerability libraries
-   Retrieve vulnerability/CI pairings
-   Synchronize CIs with vulnerability management system

Useful capabilities provided:

-   Decoupled data retrieval/processing for integration component reusability.
-   Native support for processing passing data returned to data sources \(and import sets/transform maps\).
-   Supports multiple data requests per integration \(for paginated calls\) with the ability to pass context to subsequent calls.

Resources:

[Vulnerability data integration documentation](../../vulnerability-response/concept/c_VulnerabilityIntegrations.md)

**Parent Topic:**[ServiceNow Security Operations integration development guidelines](c_IntegrationWritingGuidelines.md)

**Related topics**  


[Security Operations Integration Configurations](../../security-operations-common/concept/third-party-integrations.md)

[Tips for writing integrations](c_BestPractisesIntegrations.md)

[Integration troubleshooting](c_IntegrationTroubleshooting.md)

