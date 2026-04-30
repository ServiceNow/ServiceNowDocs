---
title: Domain separation and Threat Intelligence
description: Domain separation is supported in the Threat Intelligence module that is available as part of Security Incident Response. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Understanding Threat Intelligence, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Domain separation and Threat Intelligence

Domain separation is supported in the Threat Intelligence module that is available as part of Security Incident Response. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic

-   Includes **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

In the Threat Intelligence module \(as part of the Security Incident Response application\), domain separation enables service providers \(SPs\) to create and manage the threat intelligence repository in the following ways:

-   Threat sources and Trusted Automated Exchange of Indicator Information \(TAXII\) profiles
-   Observables
-   Indicators of compromise
-   Threat attack modes / methods and case management across the customer base they serve with lowered operational costs and a higher quality of service

Having separate customer work spaces for workflows, dashboards, reports, and so on, ensures that customer data is separated and never exposed to other clients.

## Domain separation support in Threat Intelligence by version release

Domain separation for the Threat Intelligence module \(as part of the Security Incident Response application\) covers the following product functionality:

-   Security incident observables are directed to the appropriate domain of the user whose ID/ Credential/ Scope generates the incident. The observables extracted from the incident are stored in the domain of the security incident.
-   Setting up of TAXII service profiles to download one or more TAXII collections that offer cyber-threat information feeds. The configuration is stored in the domain under which the profile is being set up.
-   Setting up the download of threat feeds into the IOC repository in the domain under which the configuration is being performed.
-   Creation of attack mode/methods in the domain of the threat intelligence source that provides the information automatically or the domain under which a new attack mode/method is being added manually by the user
-   Creation of cases for long-term investigation of incidents, observables, CIs, users, and indicators of compromise \(IOC\) associated with the case. The case is stored in the domain created by the user.

**Note:** In all the above cases, the overarching principles of visibility in separated domains in the NOW Platform apply. As always, an incident in the parent domain can reference artifacts in the child domain, but not the other way around.

## How domain separation works in Threat Intelligence \(as part of Security Incident Response\)

Threat Intelligence is part of Security Incident Response in the Professional and Enterprise Tiers, but not with the Standard Tier. Therefore a separate plugin is needed. The Threat Intelligence module \(as part of the Security Incident Response application\) creates and manages the threat intelligence information associated with security incidents in an organization. The following use cases are domain-separation aware:

-   Creation of security incident observables at the time of incident creation
    -   From email parsers \(Platform-based, user-reported phishing, custom\)
    -   From applications in third-party Security Information and Event Management \(SIEM\) stores
    -   Manually keyed in by the SOC analyst
-   Collection of observables from threat feed sources - Threat intelligence sources from TAXII collections
-   Manage security incident observables
    -   Associate observables with related indicators
    -   Associate observables with security incidents
    -   Associate observables with child observables
    -   Associate observable to threat feed source
    -   Add security annotations to observables
-   Manage indicators of compromise
    -   Associate indicators with related observables
    -   Associate indicators with attack mode/method
    -   Associate indicators with indicator types
    -   Associate indicators to threat feed source
    -   Add security annotations to indicators
-   Manage cases
    -   Create case \(manually or from an incident\)
    -   Edit a new case to add details \(choose case type and severity, add incidents, observables, configuration items, users, indicators\)
    -   Delete a case

## Domain separation setup

Setting up domain separation for Threat Intelligence does not require any additional steps. All Threat Intelligence tables acquire the Domain column after the instance is domain separated.

## Domain-separated data

Data can be domain separated, which means:

-   Security incident observables in one domain cannot be viewed from the scope of other domains.
-   Indicators of compromise in one domain cannot be viewed from the scope of other domains.
-   Attack modes/methods associated with one domain cannot be viewed from the scope of other domains.
-   TAXII service profiles associated with one domain cannot be viewed from the scope of other domains.
-   Threat intelligence sources associated with one domain cannot be viewed from the scope of other domains.
-   Cases associated with one domain cannot be viewed from the scope of other domains.

Threat Intelligence properties are set at the global level and are not, therefore, domain-separated. The settings include:

-   The domain name to retrieve additional information for IP addresses/URLs
-   The API key to be used for retrieval
-   Lookup of local IoC tables before sending to remote scanner
-   Number of days local observables are considered
-   Marking an attack mode/method as inactive when not received from threat intel sources
-   Marking an indicator as inactive when not received from any source for a specified number of days

## Configuration

All aspects of the threat intelligence functionality configuration are self-contained in a domain-separated environment.

The following tasks can be configured per domain:

1.  Creation of TAXII service profiles
    -   Choose a Discovery service configuration
    -   Choose a Collection service configuration - Assign roles to users and groups of users
2.  Creation of threat intelligence sources
    -   Configure the REST service that supplies the threat intel information
    -   Schedule the download of threat intel information
    -   Choose threat details information to assign to the source
3.  Creation of attack mode/methods \(manual\)
    -   Source, malware type, attack mechanism, threat actor type, description, handling, intended effect, first seen, last seen
    -   Related indicators, child attack mode/method, associated security incidents

        **Note:** Attack modes/methods are auto-created from the threat feed sources as well.

4.  Setting default lists for the following threat information categories:
    -   Attack mechanisms
    -   Discovery methods
    -   Feeds
    -   Indicator types
    -   Intended effects
    -   Notifications
    -   Observable types
    -   Rate limit definitions
    -   Threat actor types
    -   Attack motivations
    -   Infrastructure types
    -   Malware capabilities
    -   Malware types
    -   Report types
    -   Threat actor roles
    -   Tool types

## How tenant domains manage their own application data

-   Tenant domain owners can create their own TAXII service profiles.
-   Tenant domain owners can create their own threat intelligence sources.
-   Tenant domain owners can create their own attack mode/methods.
-   Tenant domain owners can create their own default lists for threat information categories.

**Note:** Business logic and processes enable threat intelligence source download schedules to be domain separated by instance owner.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

