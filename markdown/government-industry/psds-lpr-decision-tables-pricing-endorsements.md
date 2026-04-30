---
title: Pricing endorsements in License and Permit Playbook
description: Pricing endorsements are selections made on an application that affect which fees are charged by a government agency to process and issue a license/permit.Pricing endorsements are selections made on an application that affect which fees are charged by a government agency to process and issue a license/permit. As an admin, you can add one or more pricing endorsements to an existing pricing configuration decision table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a pricing configuration decision table, Configure decision tables, License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Pricing endorsements in License and Permit Playbook

Pricing endorsements are selections made on an application that affect which fees are charged by a government agency to process and issue a license/permit.

Applicants can customize their permit by selecting one or more permit endorsements. Each endorsement represents a subtype of the main permit model, and are stored as fields in a License Permit extended table. Each endorsement maps to a specific fee in the Decision Table for Pricing.

## Example of Endorsements for an Extended License Permit Case Type

An applicant can select as many endorsements as desired. Driver’s license endorsements are special permissions added to a driver’s license that allow the holder to operate specific types of vehicles or carry out specific driving-related tasks not covered under the standard license. The following table contains some examples of endorsements that can be added to the pricing decision table of a driver's license permit request case.

![Endorsement examples.](../image/psds-lpr-endorsement-examples.png)

## Add an endorsement field to a pricing configuration decision table in License and Permit Playbook

Pricing endorsements are selections made on an application that affect which fees are charged by a government agency to process and issue a license/permit. As an admin, you can add one or more pricing endorsements to an existing pricing configuration decision table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**, and select the pricing decision table.

2.  Select **New** to create a new field/column.

3.  On the form, fill in the fields.

    In the **Type** field, enter **True/False**.

4.  Select **Save**.


### Result

The pricing endorsement is now created, and can be added as a condition in the pricing decision table.

