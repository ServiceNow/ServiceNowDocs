---
title: Security Operations email parsing
description: Generate new Security Operations records from external detection systems using Email Parsing. This feature provides a method for integrating information from external tools such as malware detection, vulnerability detection, firewalls, threat intelligence, and more.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Security Operations email processing, Security Operations common functionality, Security Operations]
---

# Security Operations email parsing

Generate new Security Operations records from external detection systems using Email Parsing. This feature provides a method for integrating information from external tools such as malware detection, vulnerability detection, firewalls, threat intelligence, and more.

**How emails are parsed**

Any system that can send an email, can create Security Operations records, for example, security incidents, requests, vulnerable items, vulnerabilities, security incident observables, attack methods, and more.

All Security Operations plugins \(Security Incident Response, Threat Intelligence, and Vulnerability Response\) have a property \(**email\_to**\) that defines the email address where external integrations should send emails to, to be parsed by the email parsers. See **Email Processing** &gt; **Properties** for more information.

Email sent to any of the Security Operations email addresses is stored in an email events table. These emails are processed to determine whether they match any email parser.

Emails that have a match are flagged and the transform and duplication rules create or update a Security Operations record. The email is linked to that record and flagged as `matched`.

Emails that do not match are listed in Unmatched Emails as a Security Operations record. They can be reviewed to help build email parsers to handle these emails. A Reprocess action allows you to run the unmatched email through the parsers again. The original email log is linked to that record.

The duplication rules for the email transform manage multiple emails relating to the same issue. These rules define what makes a duplicate record and can prevent duplicate records from being created. When a duplicate is detected, the rule specifies what action to take: no action \(do not create a new record\), create the new record as a child record of the existing record, or update the existing record. When updating the duplicate rule specifies which fields in the existing record are updated.

**Note:** A Security Operations email parser works in conjunction with platform inbound actions and does not replace them. It does not support setting values on indirect fields for example, **sys\_journal\_field** entries.

By default, email events are deleted after 30 days.

**Multiple records**

External detection systems \(malware detectors, vulnerability, and so on\) can send emails that report on multiple items at one time. The email parser supports separators within the email.

For example, a malware detector could send you an email report about all systems within your network infected by one particular malware with information about the malware first, followed by a list of the systems affected.

![Malicious email example](../image/EvilBunnyEmail.png "Sample malicious email")

In this example, when the **Record Separator** is set within your **Email Transform**as **=================**, it splits the email into four sections that are evaluated separately. This creates a Security Incident for each of the three affected systems.

**Note:** The header section is detected but does not have any affected systems so, it is used in all three records and does not create a fourth record.

**Field Transforms** pull in data from each section. If something in the header or footer of the email applies to all records, such as Malware Hash, Malware Name, and Type in this example, the field transform for them should set **Search for value** to a value that searches within the email body either **At the start of a line in the email body** or **Anywhere in the email body**.

**Field Transform**s must be set to search **At the start of a line within the record section** or **Sec** for data that is defined within each section, such as System, IP address, or Status. The record section options are only available when there is a record separator defined within the email transform.

When parsing an email with a separator defined, records are only created for sections with at least one piece of section-specific data.

In this example, three records are created, even though there are four sections defined. The first section is a header, and it lacks anything specific to only one system. If any of the fields within the first section were filled in \(System, IP, or Status\), then a record would be created for that section, as well.

-   **[Create email parsers in Security Operations](../task/parsing-emails.md)**  
Email Parsing creates Security Operations records from your email for security, vulnerability, and observables to expedite threat response and remediation.
-   **[Edit email records in Security Operations](../task/edit-email-records.md)**  
Add or create transforms in your existing email event records.

**Parent Topic:**[Security Operations email processing](email-processing.md)

**Related topics**  


[Create email parsers in Security Operations](../task/parsing-emails.md)

[Security Operations enrichment data mapping](enrichment-data-mapping.md)

[Security Operations field mapping](field-mapping.md)

