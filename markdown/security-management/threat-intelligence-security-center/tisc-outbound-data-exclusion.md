---
title: Configuring Outbound Intel Data Exclusion Rule
description: Use this section to create exclusion rules, which can be configured by TISC admin to restrict sharing of records that match the defined criteria.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Outbound Intel Data Exclusion Rule

Use this section to create exclusion rules, which can be configured by TISC admin to restrict sharing of records that match the defined criteria.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

You can share certain entities while excluding specific records within those entities. You can share specific types of entities while excluding particular records based on their sensitivity. For example, you might want to share domain names but exclude those with a TLP \(Traffic Light Protocol\) rating that restricts sharing. This approach helps prevent sensitive domain names from being shared within the organization or with external organizations.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Outbound Intel Sharing**.

2.  Select **Outbound Intel Data Exclusion Rules**.

    The **Data Exclusion Rule** is the default Outbound Intel Data Exclusion Rule for outbound sharing provisioned within the base system.

3.  **Editing Outbound Intel Data Exclusion Rules:**
4.  Select **Edit** button to modify the exclusion rules defined for each table under **Exclusion Rules** tab.

    A warning message is displayed indicating that any automation flows based on these settings may fail if you proceed without disabling them first.

    If you acknowledge this risk and want to proceed, you may modify the exclusion rules by selecting **Edit** button.

5.  **Modifying Outbound Intel Data Exclusion Rules:**
6.  Go to **Exclusion Rules** section.

    The **Exclusion Rules** lists displays all the rules that are provisioned within the base system. The list provides the details of each exclusion rule including the entity, entity type, and specific exclusion conditions.

    When the conditions are matched, the records that meet these specified criteria won’t be shared.

7.  Select any exclusion rule that you want to modify or add additional conditions, and **Save** the rule.

8.  After you make the necessary changes to the Global Data Exclusion Rule, then select **Publish** button to apply the updated exclusion rule.

    Every action performed on the exclusion rules is recorded, and a work note showing the previous and current values for each condition is posted in the Activity Stream.

    **Note:**

    -   Enabling templates or sharing from GUI is not allowed while the Outbound Intelligence Data Exclusion Rule is in the edit mode.
    -   The automated sharing and automatic addition of records to TAXII collections will also fail while the exclusion rule remains in edit mode.

**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Sharing Profiles](tisc-outbound-sharing-profiles.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

[Working on the Redaction Library](tisc-redaction-library.md)

