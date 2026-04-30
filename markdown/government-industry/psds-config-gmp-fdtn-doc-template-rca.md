---
title: Configure Restricted Caller Access \(RCA\) for Document Templates
description: Allow secure, controlled access for generating results letters.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-17"
reading_time_minutes: 1
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Restricted Caller Access \(RCA\) for Document Templates

Allow secure, controlled access for generating results letters.

## Before you begin

Role required: admin

**Note:** Set the application scope to **Document Templates** by selecting the application picker \(![](../../../reuse/icons/product-icons/globe-fill-24.svg)\) in the Unified Navigation bar, then **Application Scope** &gt; **Document Templates**. The default scope is Global.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Select **New**.

3.  On the form, fill in the fields with the following information.

    |Field|Entry|
    |-----|-----|
    |Source Scope|Grants Management Playbook|
    |Source Type|Script Include|
    |Source|GrantManagementUtilImpl|
    |Status|Allowed|
    |Target Scope|Document Templates|
    |Target Type|Table|
    |Target|Table: HTML Template|
    |Operation|Read|

4.  Select **Submit**.

5.  Select **New**.

6.  On the form, fill in the fields with the following information.

    |Field|Entry|
    |-----|-----|
    |Source Scope|Grants Management Playbook|
    |Source Type|Script Include|
    |Source|GrantManagementUtilImpl|
    |Status|Allowed|
    |Target Scope|Document Templates|
    |Target Type|Script Include|
    |Target|Script Include: HtmlTemplateUtils|
    |Operation|Execute API|

7.  Select **Submit**.


## Result

RCA access for Document Templates has now been configured.

## What to do next

You can now set up the grant program.

**Parent Topic:**[Configure Grants Management](../concept/psds-config-gmp-foundation.md)

**Previous topic:**[Configure Grants Management](../concept/psds-config-gmp-foundation.md)

**Next topic:**[Assign user personas, roles, groups, and responsibilities in Grants Management](../concept/psds-config-gmp-assign-user-roles-responsibilities.md)

