---
title: Shared data transformation
description: The Security Incident Response, Vulnerability Response, and Threat Intelligence plugins share common features, for relationship data and duplication rules, used to import external and internal information into Security Operations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Shared data transformation

The Security Incident Response, Vulnerability Response, and Threat Intelligence plugins share common features, for relationship data and duplication rules, used to import external and internal information into Security Operations.

Email Parsing, Duplication Rules, and Field Mapping take input data \(an email, JSON or XML file, or a record\) and transform that data into the correct format to create a new record. Each of these features pulls data in their own way but, it is transformed into the new record using many of the same processes.

## Relationship data

When you add information to a related list \(such as an associated observable in a security incident\), you can create a relationship record consisting of an m2m table. Sometimes, there is additional data on that relationship record to set. For example, an observable being a Source IP \(as opposed to a destination IP\). That information goes in the **Relationship data** field in the **Field Transform** form used by **Email Parsing** or a **Field Mapping Fields** related list in the **Field Mapping** form.

The **Relationship data** field is usually empty. It is most commonly used for IP addresses on observables in **Email Parsing**.

You can transform data from any ServiceNow record to any other ServiceNow record using **Field Mapping Fields** in the **Field Mapping** feature. For example, to transform data from an incident to a security incident, or a security incident to a PRB.

## Security Operations duplication rules

Use Duplication Rules to handle duplicate records for security, vulnerability, IoCs, and so on.

Duplication rules have two purposes. They prevent too many duplicate records from being created and, when a duplicate is detected, they specify which fields in the record are updated. Only active duplicates are looked for. If the record is not active, for example, if the incident is closed, then any new identical problem becomes a new incident.

Duplication rules are used by **Email Parsing**, **Field Mapping**, and **Enrichment Data Mapping**.

-   **[Create duplication rules in Security Operations](../task/create-duplication-rules.md)**  
You can use Duplication Rules to identify new email, enrichment data, or field maps with active duplicate records and process them appropriately.

**Parent Topic:**[Security Operations common functionality](sec-ops-common-functionality.md)

**Related topics**  


[Create email parsers in Security Operations](../task/parsing-emails.md)

[Map tables to tables with Security Operations field mapping](../task/create-field-mapping.md)

