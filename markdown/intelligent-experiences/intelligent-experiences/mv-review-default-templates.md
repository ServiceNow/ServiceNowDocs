---
title: Review or create default template rules
description: Assign a default value template to each AI system category and vendor so that newly onboarded AI systems are mapped automatically.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 1
keywords: [default template rules, value template, AI Control Tower, vendor]
---

# Review or create default template rules

Assign a default value template to each AI system category and vendor so that newly onboarded AI systems are mapped automatically.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward

## About this task

AI Control Tower includes out-of-the-box templates so that each AI system category has a default template. When a new AI system is onboarded, AI Control Tower maps a default template to it based on the vendor and, for ServiceNow, the AI system category.

After you set up default rules, value templates are automatically assigned to new AI systems. When AI Discovery registers a new AI system, and the system reaches the **Deployed** state, AI Control Tower applies the matching default rule. This automation reduces manual setup by eliminating the need to map each new AI system individually.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Templates** &gt; **Default template rules**.

3.  Select an existing template from the list to review it.

4.  If the existing templates don't meet your requirements, create a new default template rule.

    1.  Select **Assign default templates**.

        The Assign default template dialog box appears.

    2.  From the **Template** list, select a template.

    3.  From the **Vendor** list, select a vendor.

    4.  If you selected **ServiceNow** as the Vendor list, select an AI system category.

    5.  Select **Assign as default**.


## Result

When AI Discovery registers a new AI system, it checks if it matches the asset type and vendor. If it does and reaches the "Deployed" state, AI Control Tower maps the default templates to that system.

