---
title: Define a Product Model for License and Permit Playbook
description: A product model record is required in a license/permit case application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Define a Product Model for License and Permit Playbook

A product model record is required in a license/permit case application.

## Before you begin

Role required: admin

## About this task

For a license/permit case, a product model is used to represent a specific type of license/permit. Having a specific product model can help support multiple aspects of the permitting process implementation, such as defining the product, associating multiple services with it, delivering specific product instances, enabling additional workflows, etc.

Additional fields to describe the permit product can be added if required. For example, for a drivers license, you may add a choice field for license class with choices A, B, or C, then create three records, one per class. For a commercial fishing permit, you may add a field that captures whether or not a boat inspection is required before the permit can be granted.

If there are multiple types of permits with unrelated fields, you can extend specific product model classes from the permit model base class. For example, if your agency offers bird taxidermy and wildlife import/export permits out of the same organization, consider whether you need specific permit model classes that would help define different attributes on each permit product.

## Procedure

1.  Navigate to **All** &gt; **Constituent Service** &gt; **Products** &gt; **Permit Models**.

2.  Select **New**.

3.  Select **Form Header** &gt; **Configure** &gt; **Form Layout**.

4.  Select **Edit this section in Expanded Model and Asset Classes**.

5.  Select the checkbox next to the **Cost** and **Customer Visible** fields.

    These fields must be set to true in order for the constituent or businesses contact to determine their pre-eligibility.

6.  Add any additional fields to collect additional information from the user for the permit model.

    For example, for a commercial fishing permit, you may add a field that captures whether or not a boat inspection is required before the permit can be granted.

7.  On the Configuring Permit model form, fill in the fields.

8.  Select **Submit**.


