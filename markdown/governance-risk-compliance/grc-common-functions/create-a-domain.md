---
title: Create a domain
description: You can create a domain by creating a record in the \[domain\] table.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Domain separation in GRC, Common GRC features, Governance, Risk, and Compliance]
---

# Create a domain

You can create a domain by creating a record in the \[domain\] table.

## Before you begin

Role required: admin

## About this task

When creating a new domain, keep the following in mind:

-   Only one domain can be the default domain.
-   Only one domain can be the primary domain.

## Procedure

1.  Navigate to **All** &gt; **Domain Admin** &gt; **Domains**.

2.  Click **New**.

3.  Fill in the necessary fields \(see table\).

4.  Click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the domain.|
    |Type|Select a domain type that describes the domain. By default the domain types are Vendor, Customer, and MSP. You can also add your own choices.|
    |Primary|Select the check box if this domain is to be the top-level domain in the hierarchy. The top-level domain only has child domains and no parent domains.|
    |Default|Select if this domain is to be the default domain for your hierarchy.|
    |Parent|Select the name of the domain higher in the hierarchy that contains this domain. This field must have a value for the domain to appear in the domain map.|
    |Active|Select the check box to make the domain available for use. You must select this option for this domain to appear in the domain map.|
    |Description|Enter a description for the domain.|

    Each domain record can also have several related records:

    -   Companies
    -   Contains Domains
    -   Contained By

## What to do next

To change the domain hierarchy, go to the Contains Domains related list and select the domain records that is the child \(contained\) domains of the contains relationship.

**Parent Topic:**[Domain separation in GRC](../concept/grc-domain-separation.md)

