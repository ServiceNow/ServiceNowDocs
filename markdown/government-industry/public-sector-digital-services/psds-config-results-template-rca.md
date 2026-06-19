---
title: Configure Restricted Caller Access for a results letter
description: Once the Grant Program Manager is ready to release the results letters for the applicants, the letters can be configured using Restricted Caller Access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-results-template-rca.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Create a results letter template, Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Restricted Caller Access for a results letter

Once the Grant Program Manager is ready to release the results letters for the applicants, the letters can be configured using Restricted Caller Access.

## Before you begin

Role required: admin

Verify that the scope is set to **Document Templates**.

## Procedure

1.  Navigate to **System Application** &gt; **Application Restricted Caller Access Privileges**

2.  Select **New**.

3.  On the form, fill in the fields with the following information.

    | | |
    |---|---|
    |Source Scope|Grants Management Playbook|
    |Source Type|Script Include|
    |Source|Script Include: GrantManagementUtilImpl|
    |Status|Allowed|
    |Target Scope|Document Templates|
    |Target Type|Table|
    |Target|Table: HTML Template|
    |Operation|Read|

4.  Select **Submit**.

5.  Select **New**.

6.  On the form, fill in the fields with the following information.

    | | |
    |---|---|
    |Source Scope|Grants Management Playbook|
    |Source Type|Script Include|
    |Source|Script Include: Script Include: GrantManagementUtilImpl|
    |Status|Allowed|
    |Target Scope|Document Templates|
    |Target Type|Script Include|
    |Target|Script Include: HtmlTemplateUtils|
    |Operation|Execute API|


**Parent Topic:**[Create a Grants Program results letter template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-configure-results-template.md)

