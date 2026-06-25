---
title: Create Contains relationships between domains
description: Create a "contains" relationship between domains to change the domain hierarchy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/t\_CrContRelBetDom.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View domain relationships, Setup and administration, Domain separation for service providers, Access Management]
---

# Create Contains relationships between domains

Create a "contains" relationship between domains to change the domain hierarchy.

## Before you begin

Role required: admin

## About this task

Domains in a contains relationship inherit the settings of the containing domain. The containing domain allows users to see data in the contained domain as well as any of its children. Processes are unaffected by a contains relationship.

## Procedure

1.  Navigate to the domain table.

2.  Select the domain record that is the parent \(container\) domain of the new contains relationship.

3.  [Toggle the domain scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainScope.md) to switch between the session scope and record scope, if necessary.

4.  From the Contains Domains related list, click **Edit**.

5.  Select the domain records that is the child \(contained\) domains of the contains relationship.

    Only child domains appear by default when the domain picker is set to Global. Toggle the domain scope to see all domains.

6.  Click **Save**, and then click **Update**.

    \[Omitted image "Contains\_domains.png"\] Alt text: Contains Domains


**Related topics**  


[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

