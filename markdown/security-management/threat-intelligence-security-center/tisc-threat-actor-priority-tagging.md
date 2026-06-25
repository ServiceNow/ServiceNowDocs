---
title: Automatic Threat Actor priority tagging
description: Learn how to enable automatic tagging of Threat Actors based on their origin locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-threat-actor-priority-tagging.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 2
keywords: [automatic tagging, threat actor priority tagging]
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Automatic Threat Actor priority tagging

Learn how to enable automatic tagging of Threat Actors based on their origin locations.

## Before you begin

Role required:

-   admin
-   sn\_sec\_tisc.admin

## About this task

When a relationship between a Threat Actor and a Location object is created or updated, and the relationship type is **originates-from**, a **Priority: Critical** tag is automatically added to the Threat Actor.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select the **Automatic Threat Actor priority tagging** link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following trigger:

    ```
    Object-Object Relationship Created or Updated where (Source Object Type is threat-actor, and Target Object Type is location, and Target Object . Name [Location] is one of China, North Korea, and Relationship Type is originates-from, and Source Object . TISC Tags [Threat Actor] does not contain Priority: Critical)
    ```

5.  If an Object-Object relationship is created or updated between a Threat Actor and a Location, and the relationship type is `originates-from`, add a `Priority: Critical` tag to the Threat Actor.

    \[Omitted image "tisc-automatic-priority-tagging.png"\] Alt text: Automatic Threat Actor priority tagging in TISC


**Parent Topic:**[Working with automated flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment]()

[Automated sharing of high-risk IOC's with trusted partners]()

[Automatically add threat intelligence to a TAXII collection]()

[Create vulnerability assessment for zero day]()

[Analyze, assess, and disseminate observables]()

[Analyze and assess threat IoC’s]()

[Vulnerability Management Support]()

[Zero-day vulnerability tracking]()

[Automated flows tables]()

