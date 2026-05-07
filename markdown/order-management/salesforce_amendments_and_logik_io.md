---
title: Salesforce amendments and CPQ
description: A brief look at the Logik amendments feature, which adds and updates fields in existing objects.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ integration with Salesforce B2B Commerce, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Salesforce amendments and CPQ

A brief look at the Logik amendments feature, which adds and updates fields in existing objects.

The CPQ amendments feature follows the standard CPQ amendment model by adding additional fields to existing objects as well as triggers to update these fields appropriately.

## Prerequisites

The Logik Extension for Salesforce CPQ must be installed in the org.

## How the amendments feature works

When an amendment is created from a contract, generating a CPQ quote and CPQ quote lines, a CPQ trigger on the CPQ quote line automatically populates the Committed Configuration ID from the related subscription record and sets the Action Context to Amend.

When a reconfiguration of the quote line is saved, the configuration line item includes the prior quantity and price.

When the standard Salesforce CPQ amendment process is completed, the contract is updated with subscriptions using the new quantities and terms as expected.

The following fields are added to facilitate this functionality.

|Object|Field|
|------|-----|
|ConfigurationLineItem c|LGK CommittedConfigurationId c|
|ConfigurationLineItem c|LGK PriorQuantity c|
|ConfigurationLineItem c|LGK PriorPrice c|
|ConfigurationLineItem c|LGK ActionContext c|
|SBQQ QuoteLine c|LGK CommittedConfigurationId c|
|SBQQ QuoteLine c|LGK ActionContext c|
|SBQQ Subscription c|LGK ConfigurationId c|
|SBQQ Subscription c|LGK BomData c|

You can disable this functionality in Setup &gt; Custom Settings &gt; Manage Logik Tenant &gt; Edit &gt; Disable Amendment Triggers.

