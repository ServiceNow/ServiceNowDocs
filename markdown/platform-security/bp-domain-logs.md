---
title: Checking domain logs for errors and warnings
description: Check the domain logs to find errors or warnings in your domain path processes and hierarchy configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-logs.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Checking domain logs for errors and warnings

Check the domain logs to find errors or warnings in your domain path processes and hierarchy configurations.

You can find the domain logs in the Domain Log \[syslog\_domain\] table. When the domain hierarchy updates, the system triggers a scheduled job to recalculate the domain paths. The domain logs table captures the results.

Look for any errors and warnings in this table. After reviewing this table, you need to resolve these errors and run the domain path validator again.

In this example of a log, the system has detected ten orphan records in the sys\_ui\_list table. The errors in these records must be fixed before the domain path can run successfully.

\[Omitted image "bp-domain-logs.png"\] Alt text: Domain logs showing errors

To learn more about domain-separation errors, see [Troubleshoot domain separation errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_TroubleshootDomainSeparationError.md).

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Domain separation hierarchies]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

[Domain separation terms]()

[Domain-separate a custom table]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

