---
title: Avoiding domain path in scripts
description: Domain paths can cause the values of your script to change or even break, so don't use them in scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-no-domain-path-in-scripts.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Avoiding domain path in scripts

Domain paths can cause the values of your script to change or even break, so don't use them in scripts.

Your script should not depend on the domain path because if you ever change the domain hierarchy, the domain path recalculates and its value changes. When this happens, your scripts are useless or can throw errors or break. The best strategy is not to write your scripts based on domain paths.

Use the **sys\_domain** field in your scripts rather than depending on the domain path. If you ever change the domain hierarchy, the domain path recalculates and its value changes, which can cause your scripts to be useless, throw errors, or break. Look for base system business rules, which use the **sys\_domain** field, to get some ideas before creating your own scripts.

The ServiceNow platform does not capture the sys\_domain\_path values in an update set in order to avoid issues with differences in the domain hierarchy for each instance. Therefore, you should validate the domain hierarchy after you import an update set to ensure that the domain path values for your records are correct.

To learn more about domain path, see [Request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ActivateDomainSeparation.md) and [Domain Separation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separation-center.md).

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

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

