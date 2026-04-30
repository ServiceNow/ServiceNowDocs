---
title: Understanding Security Incident Response
description: With Security Incident Response \(SIR\), manage the life cycle of your security incidents from initial analysis to containment, eradication, and recovery. Security Incident Response enables you to get a comprehensive understanding of incident response procedures performed by your analysts, and understand trends and bottlenecks in those procedures with analytic-driven dashboards and reporting.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Understanding Security Incident Response

With Security Incident Response \(SIR\), manage the life cycle of your security incidents from initial analysis to containment, eradication, and recovery. Security Incident Response enables you to get a comprehensive understanding of incident response procedures performed by your analysts, and understand trends and bottlenecks in those procedures with analytic-driven dashboards and reporting.

An introduction to Security Incident Response, showing how to get started using the application. 

Watch this video to learn about the SIR process, using Security Incident Response to thwart attacks and viewing security activity in the Security Incident Response Explorer.

Built in integrations with third-party cyber security solutions and partner-developed integrations from the ServiceNow Store enable security automation and orchestration for efficient and accurate incident response.

To protect your investigations and keep security incidents private, Security Incident Response provides the means to restrict access to the system to specific security-related roles and ACLs. Non-security administrators can be restricted from access, unless you expressly allow them entry.

**Note:** IT System Administrators \[admin\] can impersonate ServiceNow users. However, when impersonating a user with an application admin role for Security Incident Response, an admin cannot access features granted by that role, including security incidents and profile information. Access to modules and applications in the navigation bar is also restricted. Also, admin cannot change the password of any user with an application admin role for Security Incident Response.

## Security Incident Response information flow

Security Incident Response employs the following flow of information, from integration through investigation, and then on to resolution and review.

**Note:** This is an interactive infographic, so you can try clicking on any of the icons or steps in the image to learn about that process or task.

![Security Incident Response flow of information](../../security-operations/image/flow-diagram.png)

## Discovery

Security incidents can be logged or created in the following ways.

-   From the Security Incident form
-   From events that are spawned internally, or created by external monitoring or vulnerability tracking systems via alert rules, or manually
-   From external monitoring or tracking systems
-   From the service catalog

## Analysis

Depending on the selected view, you are using \(default, Non-IT Security, Security ITIL, and so on\), the Security Incident form can show any combination of vulnerabilities, incidents, changes, problems, tasks on the affected CI and affected CI groups. The system can identify malware, viruses, and other areas of vulnerability by cross-referencing the National Institute of Standards and Technology \(NIST\) database, or other third-party detection software. As security incidents are resolved, you can use any incident to create a security knowledge base article for future reference.

Perform further analysis using a business service map to locate other affected systems or business services that can be infected.

## Containment, Eradication, and Recovery

As you monitor and analyze vulnerabilities, you can create and assign tasks to other departments. You can use a business service map to create tasks, problems, or changes for all affected systems, documents, activities, SMS messages, bridge calls, and so forth.

## Review

After the incident is resolved, other steps can take place before closure. You can perform a post incident review. Creating knowledge base articles can help with future similar incidents. Significant incidents may require a post-incident resolution review. This review can take several forms. For example:

-   Conduct a meeting to discuss the incident and gather responses.
-   Write and distribute to those teams who worked on an incident a list of resolution review questions designed for each category or priority of incident.
-   Incident managers can write the report and gather information on their own.

An incident resolution review report can be automatically generated that includes:

1.  a summary of what was done
2.  the time line
3.  the type of security incident encountered
4.  all related incidents, changes, problems, tasks, CI groups
5.  the details of the resolution

In addition, an automated security incident resolution review survey system is available. It gathers the names of all users assigned to a security incident, and sends out a customized survey to gather data about the handling of the incident. This data can then be made available in a generated security incident review report, which you can edit into a final draft. Similar data can be added to a knowledge base article to contain lessons learned and the steps to take to resolve similar issues in the future.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Security Incident Response Terminology

The following terms are used in Security Incident Response.

|Term|Definition|
|----|----------|
|Active|Any security incident not in the closed or cancelled state.|
|[Administrator lockdown](../task/t_ConfigureSIM.md#)|The ability to restrict Security Incident Response access to personnel with security-related roles and ACLs.|
|[Inbound security requests](manage-si-details.md)|Requests submitted for low-impact security demands, such as requesting a new electronic badge.|
|[Manage post incident activities](c_PostIncidentReview.md)|A review of the origins and handling of a security incident. The final product is a post incident report, which documents all actions performed and the reasons for doing them.|
|[Response tasks](../task/t_CreateResponseTask.md)|Tasks assigned to a security incident for tracking actions in response to the threat.|
|[Understanding security incident calculators](../reference/setup-assistant-reference.md#)|Calculators used to update record values when pre-configured conditions are met.|
|[Security incident treemaps](../task/t_AddTreemapsToSIRHomepage.md)|Chart type that hierarchically shows security incident data in the form of nested rectangles.|
|[Threat lookup](../../threat-intelligence/task/t_SubmitThrtScnReqFromCat.md)|A request submitted from the security incident catalog for scanning files, URLs, and IP addresses for malware.|
|[Vulnerability scan](../task/t_SubmitVScanReqFromSecInc.md)|A request initiated from the Security Incident form for scanning affected resources \(servers, computers, and other configuration items\) for vulnerabilities.|

